# Blood Treachery — Searchable Index Bundle

This bundle lets Claude answer questions about this book without
re-reading the original PDF.

## Files

- **`book_index.md`** — thematic index: act-by-act summaries, themes,
  key terms, cross-cutting notes. Read this first, in full, for any
  broad/thematic question.
- **`book_chunks.db`** — SQLite database of paragraph-level chunks with
  full-text search, for precise fact lookup, exact dates/names, or
  quote verification. Query it, don't load it in full.
- **`scripts/query_chunks.py`** — command-line helper for querying the DB.

Book: *Blood Treachery* (2004), by Scott Cohen and Steven Michael
DiPesa — 96 pages (source PDF page count), indexed 2026-08-25.

## What this book is — and isn't

This is a **Revised Edition** (2000 ruleset) sourcebook from White
Wolf's "Year of Revelations" line — neither an M20 book nor part of
the same classic-2nd-Edition era as `mage-sorcerers-crusade` already
in this library. It's a Mage/Vampire crossover written almost
entirely as a five-act interactive drama (a literal theatrical
script, not conventional prose chapters), telling the story of a
renewed war between the Order of Hermes and House Tremere. It's
included in this library because it directly continues and
cross-references lore from both other books already here — see this
library's top-level `README.md` and `library_index.md` for the full
three-era picture and the specific connections (the *first* Massasa
War is documented in `mage-sorcerers-crusade`; Doissetep's fall and
Porthos Fitz-Empress's death, referenced here as recent history, get
their full account in `m20-core`).

## Important: page numbers are PDF pages, not printed pages

This PDF has 5 unnumbered front-matter pages (cover, blanks, title/
credits, Table of Contents) before the book's own printed
page-numbering begins, so **PDF page = printed page + 1** throughout
the rest of the book (verified at every chapter transition). Every
page number in `book_index.md` and every `page` value in
`book_chunks.db` refers to the page's position in the source PDF —
**not** the number printed in the book's own footer. If you're
working from the physical/PDF book, add 1 to the printed page number.
If you're only using this bundle, the numbers already agree with
each other.

## For a future Claude session: how to use this bundle

1. Read `book_index.md` in full — it's small and gives you orientation
   plus answers to most broad/thematic questions directly.
2. For precise facts, exact dates, or verifying a quote, query the
   chunk database instead of guessing from the summary:

   ```bash
   python3 scripts/query_chunks.py book_chunks.db "search terms here"
   python3 scripts/query_chunks.py book_chunks.db --page 52
   python3 scripts/query_chunks.py book_chunks.db --chapter "Act Three: Blood Treachery"
   ```

   Full-text search supports phrase queries (`"exact phrase"`), boolean
   operators (`term1 AND term2`, `term1 NOT term2`), and prefix matching
   (`term*`).
3. Cite page numbers from the chunk results when quoting or referencing
   specific facts — this is the audit trail back to the source PDF
   (remember the +1 offset above if cross-referencing against a
   physical copy).
4. Only fall back to the original PDF if both files fail to answer the
   question (e.g. artwork, or a chart whose layout matters).

## Part of a library

This book is part of the Mage: The Ascension library alongside
`m20-core`, `m20-how-do-you-do-that`, and `mage-sorcerers-crusade`.
See the library's top-level `README.md` and `library_index.md` for
the full cross-book picture — this library now spans three distinct
publication eras (classic 2nd Edition, classic Revised Edition, and
M20), and `library_index.md` documents both the real connections
between them (shared named characters and events, matching dates)
and the real differences (terminology, mechanics, and editorial
stance toward "fixed" versus optional continuity).
