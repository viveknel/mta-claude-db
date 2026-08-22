# Mage 20: How Do You DO That? — Searchable Index Bundle

This bundle lets Claude answer questions about this book without
re-reading the original PDF.

## Files

- **`book_index.md`** — thematic index: section summaries, themes, key
  terms, cross-cutting notes. Read this first, in full, for any
  broad/thematic question.
- **`book_chunks.db`** — SQLite database of paragraph-level chunks with
  full-text search, for precise fact lookup, exact Sphere/success
  numbers, or quote verification. Query it, don't load it in full.
- **`scripts/query_chunks.py`** — command-line helper for querying the DB.

Book: *Mage 20: How Do You DO That? — A Practical Guide to Sphere
Magick for Mage 20th Anniversary Edition*, by Satyros Phil Brucato —
143 pages (source PDF page count), indexed 2026-08-22.

## What this book is

A rules-expansion companion to the M20 core rulebook, not a lore/
setting book. It gives granular Sphere/Rank/success-count guidance for
dozens of specific magickal feats, organized by *what a player wants
to accomplish* (shapechanging, elemental blasts, teleportation,
necromancy, mind control, etc.) rather than by Tradition or Sphere.
Expect very little narrative content — `book_index.md` reflects that
directly rather than padding out summaries that aren't there.

## Important: page numbers are PDF pages, not printed pages

Like the M20 core rulebook, this PDF has an unnumbered cover page
before its printed numbering starts (which itself begins in Roman
numerals before switching to Arabic), so **PDF page = printed page +
1** throughout. Every page number in `book_index.md` and every `page`
value in `book_chunks.db` refers to the page's position in the source
PDF — **not** the number printed in the book's own footer. If you're
working from the physical/PDF book, add 1 to the printed page number.
If you're only using this bundle, the numbers already agree with each
other.

## For a future Claude session: how to use this bundle

1. Read `book_index.md` in full — it's small and gives you orientation
   plus answers to most broad/thematic questions directly.
2. For precise facts, exact Sphere/Rank numbers, or verifying a quote,
   query the chunk database instead of guessing from the summary:

   ```bash
   python3 scripts/query_chunks.py book_chunks.db "search terms here"
   python3 scripts/query_chunks.py book_chunks.db --page 91
   python3 scripts/query_chunks.py book_chunks.db --chapter "Uncanny Influence"
   ```

   Full-text search supports phrase queries (`"exact phrase"`), boolean
   operators (`term1 AND term2`, `term1 NOT term2`), and prefix matching
   (`term*`).
3. Cite page numbers from the chunk results when quoting or referencing
   specific facts — this is the audit trail back to the source PDF
   (remember the +1 offset above if cross-referencing against a
   physical copy).
4. Only fall back to the original PDF if both files fail to answer the
   question (e.g. a chart/table whose layout matters, or artwork).

## Part of a library

This book is part of the M20 library alongside `m20-core/` (the core
rulebook). See the library's top-level `README.md` and
`library_index.md` for cross-book context — in particular, this book
reuses the core rulebook's own example characters (Lee Ann Milner,
Jinx) rather than inventing its own cast, so the two books read as
directly continuous rather than independent.
