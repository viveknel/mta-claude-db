# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this repo is

Not a software project: it is a searchable knowledge base of *Mage: The Ascension* sourcebooks, built (by the `book-indexer` skill) so setting/rules questions can be answered without re-reading the original PDFs. There is no build, lint, or test step. The only code is two small stdlib-only Python query scripts. The source PDFs are not in the repo.

## Layout

Each book is a self-contained bundle (`m20-core`, `m20-how-do-you-do-that`, `m20-book-of-secrets`, `mage-sorcerers-crusade`, `blood-treachery`) containing:
- `book_index.md` — thematic index; small enough to read in full
- `book_chunks.db` — SQLite with paragraph-level chunks (`chunks` table: `chunk_id`, `page`, `chapter`, `text`) and an FTS5 table `chunks_fts` joined on `chunks_fts.rowid = chunks.chunk_id`
- `README.md` — book-specific notes, including its page-number offset
- `scripts/query_chunks.py` — identical copy per book (keep them in sync if you change one)

Top level: `library_index.md` (cross-book synthesis) and `scripts/query_library.py` (searches several DBs at once, showing top matches per book rather than a merged ranking).

## Answering questions (which source to use)

- Broad/thematic, one book → read that book's `book_index.md`.
- Spans books or eras → read `library_index.md` first. The books cover three distinct editions/eras (M20 2015–17; Sorcerers Crusade 1998, Renaissance; Blood Treachery 2004, Revised modern-day), **not one continuous canon**. Where they conflict, say which book's continuity an answer comes from rather than smoothing it over.
- Exact quote, figure, or page → query the book's chunk DB, and cite the page.

## Commands

Run from the repo root (use whichever of `python3`/`python`/`py` works on this machine):

```bash
python3 <slug>/scripts/query_chunks.py <slug>/book_chunks.db "search terms"
python3 <slug>/scripts/query_chunks.py <slug>/book_chunks.db --page 148
python3 <slug>/scripts/query_chunks.py <slug>/book_chunks.db --chapter "Chapter Five: Ascension Warriors"
python3 <slug>/scripts/query_chunks.py <slug>/book_chunks.db --range 40 45
python3 scripts/query_library.py m20-core/book_chunks.db blood-treachery/book_chunks.db "search terms" [--limit N]
```

FTS5 syntax applies (`"phrase"`, `AND`/`NOT`, `prefix*`). Unquoted hyphens or apostrophes (`Fitz-Empress`, `Wizards' March`) cause an FTS5 syntax error; drop the punctuation or wrap the phrase in escaped double quotes. The `--` separator shown in `query_library.py`'s docstring is not needed; the README's form (no `--`) is the one to use.

## Gotchas

- **Page numbers are PDF pages, not printed pages.** Offset (PDF = printed + N): +1 for `m20-core`, `m20-how-do-you-do-that`, `m20-book-of-secrets`, `blood-treachery`; +19 for `mage-sorcerers-crusade`. Cite the DB's numbers and mention the offset when the user is working from a physical or PDF copy.
- Chunks are summaries/short excerpts, not full book text. Mechanics-heavy chapters are deliberately not summarized in `book_index.md`; query the DB for those.
- `*.db` files are binary and tracked in git; don't regenerate or hand-edit them.

## Adding a book

Run the book-indexer skill's workflow on the new PDF to produce a new `<slug>/` bundle, then update `library_index.md` and the README's tables, tree, and "Before you use this library" section (see `references/cross_book_index.md` → "Adding a book later" in the skill). The "five books" wording is hardcoded in `library_index.md` and `README.md`, so update it too.
