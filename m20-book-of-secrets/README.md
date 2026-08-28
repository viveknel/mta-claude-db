# Mage 20: The Book of Secrets — Searchable Index Bundle

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

Book: Mage 20: The Book of Secrets — 301 pages (source PDF page
count), indexed 2026-08-28.

## Important: page numbers are PDF pages, not printed pages

This PDF has one unnumbered cover page before the printed page
numbering starts, so **PDF page = printed page + 1**, consistently,
across the entire book (verified from the Table of Contents through
the back matter — the front matter also briefly uses roman numerals
for a two-page fiction Prelude, but this doesn't disturb the +1
offset once the book moves into Arabic-numbered content). This
matches the offset used by the other M20-line books in this library
(`m20-core` and `m20-how-do-you-do-that`), since all three share the
same production. Every page number in `book_index.md` and every
`page` value in `book_chunks.db` refers to the page's position in the
source PDF — **not** the number printed in the book's own footer. If
you're working from the physical/PDF book and want to find a page
cited here, add 1 to the number printed on the page. If you're only
using this bundle (reading `book_index.md` or querying
`book_chunks.db`), the numbers already agree with each other and no
conversion is needed.

## For a future Claude session: how to use this bundle

1. Read `book_index.md` in full — it's small and gives you orientation
   plus answers to most broad/thematic questions directly.
2. For precise facts, exact numbers, or verifying a quote, query the
   chunk database instead of guessing from the summary:

   ```bash
   python3 scripts/query_chunks.py book_chunks.db "search terms here"
   python3 scripts/query_chunks.py book_chunks.db --page 219
   python3 scripts/query_chunks.py book_chunks.db --chapter "Chapter Four: Justice and Influence"
   ```

   Full-text search supports phrase queries (`"exact phrase"`), boolean
   operators (`term1 AND term2`, `term1 NOT term2`), and prefix matching
   (`term*`). Hyphens and apostrophes in unquoted multi-word queries
   can trigger an FTS5 syntax error (e.g. `Fitz-Empress`, `God's Left
   Hand`) — if that happens, drop the punctuation or wrap the phrase
   in escaped double quotes and retry.
3. Cite page numbers from the chunk results when quoting or referencing
   specific facts — this is the audit trail back to the source PDF
   (remember the +1 offset above if cross-referencing against a
   physical copy).
4. Only fall back to the original PDF if both files fail to answer the
   question (e.g. the question is about a piece of interior artwork,
   a Wonder illustration, or a chart layout that text extraction
   wouldn't have captured).

## Notes on this book's structure

Unlike a typical sourcebook, *The Book of Secrets* is a grab-bag
companion with no throughline plot — it collects material cut from
the M20 core rulebook for space. Its five chapters are genuinely
independent:

- **Chapter One (pp. 13-100)** is almost entirely a Merits/Flaws/
  Archetypes/secondary-Abilities catalog — mechanically dense with
  comparatively little narrative content. `book_index.md` summarizes
  it by category with notable standouts flagged rather than listing
  every Trait; query `book_chunks.db` directly for a specific Trait's
  exact cost or rules text.
- **Chapter Two (pp. 101-166)** is optional expanded rules (combat,
  certámen, computers, Resonance, Wonder-crafting) — also mechanical,
  but includes the book's most substantial worldbuilding subsystem
  (Resonance and Synergy).
- **Chapter Three (pp. 167-210)** is genuine setting/character-design
  content: expanded Focus paradigms/practices/instruments plus six
  fully worked example characters, useful as ready-made NPCs or build
  templates.
- **Chapter Four (pp. 211-252)** is the book's richest durable setting
  lore: how each faction (Traditions, Technocracy, Disparate Alliance,
  Nephandi, Marauders) administers internal justice and exerts
  influence on the unawakened world.
- **Chapter Five (pp. 253-300)** is a first-person author miscellany —
  an FAQ on Mage 20's design choices, a Storytelling/genre guide, a
  set of standalone real-world essays, and a personal bibliography.
  It carries an explicit disclaimer that its opinions are the
  author's own, not official canon — worth keeping in mind if quoting
  it as settled setting fact.

## Part of a library

This book is part of the `m20-lib` Mage: The Ascension (M20) library,
alongside `m20-core`, `m20-how-do-you-do-that`, `mage-sorcerers-crusade`,
and `blood-treachery`. See the top-level `README.md` and
`library_index.md` for cross-book synthesis and search across the
whole collection. This bundle is also fully self-contained and can be
used standalone if copied out of the library.
