# Mage: The Sorcerers Crusade — Searchable Index Bundle

This bundle lets Claude answer questions about this book without
re-reading the original PDF.

## Files

- **`book_index.md`** — thematic index: chapter summaries, themes, key
  terms, cross-cutting notes. Read this first, in full, for any
  broad/thematic question.
- **`book_chunks.db`** — SQLite database of paragraph-level chunks with
  full-text search, for precise fact lookup, exact dates/names, or
  quote verification. Query it, don't load it in full.
- **`scripts/query_chunks.py`** — command-line helper for querying the DB.

Book: *Mage: The Sorcerers Crusade* (1998), by Phil Brucato et al. —
317 pages (source PDF page count), indexed 2026-08-22.

## What this book is — and isn't

This is **not** an M20 (20th Anniversary Edition) book. It's a
classic-era (1998) sourcebook synced to the 1996 Mage: The Ascension
Second Edition ruleset, set roughly 500 years before M20 core's modern
setting — a standalone, playable-on-its-own core rulebook for a
Renaissance-era (c. 1400s-1500s) Mage chronicle. It's included in this
library because it's thematically and historically connected to
`m20-core` (same fictional setting, centuries earlier), not because
it uses the same rules edition. See this library's top-level
`README.md` and `library_index.md` for a full account of how this book
relates to, agrees with, and differs from `m20-core` — the differences
are real (different mechanics for the Scourge/Paradox punishment
system, a different roster for the Council of Nine, a different Avatar
Essence taxonomy) and are documented there rather than smoothed over.

## Important: page numbers are PDF pages, not printed pages

This PDF opens with an unnumbered 16-page fiction Prelude before the
book's own printed page-numbering begins, so **PDF page = printed page
+ 19** throughout the rest of the book (verified at multiple points
from the credits page through the back-of-book index). Every page
number in `book_index.md` and every `page` value in `book_chunks.db`
refers to the page's position in the source PDF — **not** the number
printed in the book's own footer. If you're working from the
physical/PDF book, add 19 to the printed page number. If you're only
using this bundle, the numbers already agree with each other.

## For a future Claude session: how to use this bundle

1. Read `book_index.md` in full — it's small and gives you orientation
   plus answers to most broad/thematic questions directly.
2. For precise facts, exact dates, or verifying a quote, query the
   chunk database instead of guessing from the summary:

   ```bash
   python3 scripts/query_chunks.py book_chunks.db "search terms here"
   python3 scripts/query_chunks.py book_chunks.db --page 56
   python3 scripts/query_chunks.py book_chunks.db --chapter "Chapter II: The Mortal World"
   ```

   Full-text search supports phrase queries (`"exact phrase"`), boolean
   operators (`term1 AND term2`, `term1 NOT term2`), and prefix matching
   (`term*`).
3. Cite page numbers from the chunk results when quoting or referencing
   specific facts — this is the audit trail back to the source PDF
   (remember the +19 offset above if cross-referencing against a
   physical copy).
4. Only fall back to the original PDF if both files fail to answer the
   question (e.g. a chart/table whose layout matters, or artwork).

## Part of a library

This book is part of the M20 library alongside `m20-core/` (the
modern-day core rulebook) and `m20-how-do-you-do-that/` (a rules
companion to `m20-core`). Unlike that pair, this book is a genuinely
independent, differently-authored-era source describing an earlier
point in the same fictional timeline — see the library's top-level
`README.md` and `library_index.md` for the full cross-book picture,
including several remarkable direct continuity threads (a named
character who appears as a young mage in this book and dies centuries
later in `m20-core`'s own backstory; the exact founding dates of the
Order of Hermes and the Technocracy's predecessor both matching
exactly between the two books) alongside the real differences.
