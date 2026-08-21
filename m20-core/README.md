# Mage: The Ascension 20th Anniversary Edition — Searchable Index Bundle

This bundle lets Claude answer questions about this book without
re-reading the original PDF.

## Files

- **`book_index.md`** — thematic index: chapter summaries, themes, key
  terms, cross-cutting arguments. Read this first, in full, for any
  broad/thematic question.
- **`book_chunks.db`** — SQLite database of paragraph-level chunks with
  full-text search, for precise fact lookup, exact figures, or quote
  verification. Query it, don't load it in full.
- **`scripts/query_chunks.py`** — command-line helper for querying the DB.

Book: Mage: The Ascension 20th Anniversary Edition (core rulebook) —
698 pages (source PDF page count), indexed 2026-08-21.

## Important: page numbers are PDF pages, not printed pages

This PDF has two unnumbered cover pages before the printed page
numbering starts, so **PDF page = printed page + 1**, consistently,
across the entire book (verified at multiple points from the front
matter through the back-of-book index). Every page number in
`book_index.md` and every `page` value in `book_chunks.db` refers to
the page's position in the source PDF — **not** the number printed in
the book's own footer. If you're working from the physical/PDF book
and want to find a page cited here, add 1 to the number printed on the
page. If you're only using this bundle (reading `book_index.md` or
querying `book_chunks.db`), the numbers already agree with each other
and no conversion is needed.

## For a future Claude session: how to use this bundle

1. Read `book_index.md` in full — it's small and gives you orientation
   plus answers to most broad/thematic questions directly.
2. For precise facts, exact numbers, or verifying a quote, query the
   chunk database instead of guessing from the summary:

   ```bash
   python3 scripts/query_chunks.py book_chunks.db "search terms here"
   python3 scripts/query_chunks.py book_chunks.db --page 148
   python3 scripts/query_chunks.py book_chunks.db --chapter "Chapter Five: Ascension Warriors"
   ```

   Full-text search supports phrase queries (`"exact phrase"`), boolean
   operators (`term1 AND term2`, `term1 NOT term2`), and prefix matching
   (`term*`).
3. Cite page numbers from the chunk results when quoting or referencing
   specific facts — this is the audit trail back to the source PDF
   (remember the +1 offset above if cross-referencing against a
   physical copy).
4. Only fall back to the original PDF if both files fail to answer the
   question (e.g. the question is about a figure, chart, illustration,
   or Tarot-card artwork that text extraction wouldn't have captured).

Note: Chapters Six, Eight, and Nine are almost entirely game mechanics
(character creation Traits/Merits/Flaws catalogs, dice-pool rules,
combat/dramatic systems) with comparatively little narrative/setting
content — `book_index.md` flags these as such rather than padding out
a Trait-by-Trait or power-by-power summary. Chapter Ten is a hybrid:
its casting rules are pure mechanics, but its "Focus and the Arts"
section (the twelve Common Mage Paradigms and the Practices/Instruments
catalog) is genuine setting lore and is summarized accordingly. Query
`book_chunks.db` directly for specific mechanical rules text, Merit/Flaw
costs, or spell/rote write-ups.

## Part of a library

This book is the seed volume of a planned Mage: The Ascension (M20)
library — more M20 sourcebooks are expected to be added over time. Once
a second book is added, this bundle will move into its own `m20-core/`
subdirectory inside a top-level library folder, alongside a
`library_index.md` and `scripts/query_library.py` for cross-book
search. For now, this bundle is fully self-contained and works
standalone.
