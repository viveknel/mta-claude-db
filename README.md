# Mage: The Ascension (M20) — Searchable Library

A searchable index of *Mage: The Ascension* sourcebooks, built so that
questions about the setting can be answered without re-reading the
original PDFs. Each book has its own self-contained bundle (thematic
index + full-text search database). This library currently holds one
book; it's set up as a library from the start because more M20
sourcebooks are expected to be added over time.

## Before you use this library

**This is a fresh library with only one book in it so far.** There is
no `library_index.md` yet — that file synthesizes themes *across*
multiple books, and with a single book there's nothing to cross-
reference. Once a second M20 book is added, `library_index.md` and
`scripts/query_library.py`'s cross-book search become genuinely useful;
until then, just use `m20-core/`'s own bundle directly (see Quick start
below).

## What's in here

| Book | Folder | Pages |
|---|---|---|
| Mage: The Ascension 20th Anniversary Edition (core rulebook) | `m20-core/` | 698 |

```
.
├── README.md                ← you are here
├── scripts/
│   └── query_library.py      ← search several books' databases at once
│                                 (ready for when a second book joins)
└── m20-core/
    ├── book_index.md         ← thematic index (read this for broad questions)
    ├── book_chunks.db        ← full-text search database (query for exact facts/quotes)
    ├── README.md              ← usage instructions for this book's bundle
    └── scripts/
        └── query_chunks.py    ← search this book's database alone
```

Every book folder is a complete, self-contained bundle — `m20-core/`
can be copied out and used entirely on its own, with its own README
explaining how.

## Quick start

**Broad or thematic question about the core rulebook** ("what does M20
say about the Nephandi", "how are the nine Traditions organized") —
read `m20-core/book_index.md` directly; it's small enough to load in
full and answers most questions without any querying.

**Exact quote, precise fact, or page-number lookup** — query the
core rulebook's chunk database:

```bash
python3 m20-core/scripts/query_chunks.py m20-core/book_chunks.db "Doissetep"
python3 m20-core/scripts/query_chunks.py m20-core/book_chunks.db --page 148
python3 m20-core/scripts/query_chunks.py m20-core/book_chunks.db --chapter "Chapter Five: Ascension Warriors"
```

**Note on page numbers:** the core rulebook's PDF has two unnumbered
cover pages before its printed numbering starts, so throughout that
book, PDF page = printed page + 1. See `m20-core/README.md` for
details — this matters if you're cross-referencing against the
physical/PDF book rather than just this bundle.

**Once a second book is added**, a cross-book question can be answered
by reading `library_index.md` (once it exists) and then, if needed,
searching across books at once:

```bash
python3 scripts/query_library.py m20-core/book_chunks.db <other-book>/book_chunks.db "search terms"
```

Full-text search (both scripts) supports phrase queries (`"exact
phrase"`), boolean operators (`term1 AND term2`, `term1 NOT term2`),
and prefix matching (`term*`).

## Requirements

Python 3 with the standard library only (`sqlite3` is built in — no
extra packages to install).

## Notes on scope

- This bundle contains **summaries and short paragraph-level excerpts**
  for search/citation purposes, not the original book's full text. It's
  a research aid for someone who already owns the source PDF, not a
  substitute for it.
- Mechanically dense chapters (character creation Traits, dice-pool
  rules, combat systems) are noted in `m20-core/book_index.md` as
  reference material rather than summarized power-by-power — query
  `m20-core/book_chunks.db` directly for that content.

## Adding another related book later

Bring the new PDF plus this repo's existing `m20-core/book_index.md`
(the chunk database and original PDF aren't needed again). Run the
book-indexer skill's indexing workflow on just the new book to produce
its own `<slug>/` bundle (e.g. `m20-lore-something/`), add it alongside
`m20-core/` in this library folder, then write `library_index.md` and
this README's "Before you use this library" section to reflect the
now-real cross-book synthesis. Re-zip and re-verify the whole library
before presenting it again — see `references/cross_book_index.md` in
the book-indexer skill for the exact packaging steps.
