# Mage: The Ascension — Searchable Library

A searchable index of *Mage: The Ascension* sourcebooks, built so that
questions about the setting can be answered without re-reading the
original PDFs. Each book has its own self-contained bundle (thematic
index + full-text search database), plus a cross-book synthesis layer
on top for questions that span multiple books.

## What's in here

**M20 line** (20th Anniversary Edition, modern-day, 2015-2017):

| Book | Folder | Pages |
|---|---|---|
| Mage: The Ascension 20th Anniversary Edition (core rulebook) | `m20-core/` | 698 |
| Mage 20: How Do You DO That? — A Practical Guide to Sphere Magick | `m20-how-do-you-do-that/` | 143 |
| Mage 20: The Book of Secrets | `m20-book-of-secrets/` | 301 |

**Classic era, 2nd Edition line** (Renaissance-setting, 1998):

| Book | Folder | Pages |
|---|---|---|
| Mage: The Sorcerers Crusade | `mage-sorcerers-crusade/` | 317 |

**Classic era, Revised Edition line** (modern-day "Final Nights," 2004):

| Book | Folder | Pages |
|---|---|---|
| Blood Treachery | `blood-treachery/` | 96 |

```
.
├── README.md                       ← you are here
├── library_index.md                 ← cross-book synthesis (read for broad/comparative questions)
├── scripts/
│   └── query_library.py             ← search all five books' databases at once
├── m20-core/
│   ├── book_index.md                ← thematic index (read this for broad questions about this book)
│   ├── book_chunks.db               ← full-text search database
│   ├── README.md
│   └── scripts/
│       └── query_chunks.py          ← search this book's database alone
├── m20-how-do-you-do-that/
│   ├── book_index.md
│   ├── book_chunks.db
│   ├── README.md
│   └── scripts/
│       └── query_chunks.py
├── m20-book-of-secrets/
│   ├── book_index.md
│   ├── book_chunks.db
│   ├── README.md
│   └── scripts/
│       └── query_chunks.py
├── mage-sorcerers-crusade/
│   ├── book_index.md
│   ├── book_chunks.db
│   ├── README.md
│   └── scripts/
│       └── query_chunks.py
└── blood-treachery/
    ├── book_index.md
    ├── book_chunks.db
    ├── README.md
    └── scripts/
        └── query_chunks.py
```

Every book folder is a complete, self-contained bundle — any one of
them can be copied out and used entirely on its own, with its own
README explaining how.

## Before you use this library — read this first

This library spans **three distinct editions/eras**, not one
continuous canon:

- `m20-core`, `m20-how-do-you-do-that`, and `m20-book-of-secrets` are
  the **M20 line** — modern-day-set, 2015-2017, and the latter two
  are explicit, subordinate companions to `m20-core` (a Sphere-magick
  rules expansion and a miscellany of cut material, respectively).
- `mage-sorcerers-crusade` is a **classic-era, 2nd Edition book from
  1998**, set roughly 500 years earlier in the same fictional world
  (Renaissance Europe) — fully standalone.
- `blood-treachery` is a **classic-era, Revised Edition book from
  2004**, set in essentially the *same modern-day period* `m20-core`
  itself describes — but written 11 years earlier, when that period's
  metaplot was still being treated as fixed, ongoing continuity
  rather than the optional retrospective M20 later made it.

See `library_index.md` for the full picture — it documents both
genuine connections (a named character who appears young in one book
and dies decades later in another, confirmed across all three
narrative books, with a fourth book adding atmospheric texture and
the author's own confirmation that this throughline is optional; the
exact same "Massasa War" referenced by name 800 years apart; a named
rogue mage who's an open rumor in one book and a confirmed, resolved
case in another; the literal origin of the "Future Fates" mechanic)
and genuine differences (a Solificati/Children of Knowledge plot
development in `blood-treachery` that `m20-core`'s own later
retrospective doesn't carry forward; the Scourge and Paradox are
different game mechanics; Avatar Essence types don't share a
taxonomy) rather than smoothing any of it over.

## Quick start

**Broad or thematic question about a single book** ("what does M20 say
about the Nephandi", "how does the Wizards' March get declared") —
read that book's own `book_index.md` directly; it's small enough to
load in full and answers most questions without any querying.

**Question that spans eras or books** ("is Solificati a House of the
Order or a Disparate Craft", "what happened to Porthos Fitz-Empress
across the setting's history") — read `library_index.md` first; it's
built specifically for this and will often tell you the answer
depends on which book's continuity you mean.

**Exact quote, precise fact, or page-number lookup within one book** —
query that book's chunk database directly:

```bash
python3 m20-core/scripts/query_chunks.py m20-core/book_chunks.db "Doissetep"
python3 blood-treachery/scripts/query_chunks.py blood-treachery/book_chunks.db "Wizards' March"
python3 m20-book-of-secrets/scripts/query_chunks.py m20-book-of-secrets/book_chunks.db "Voormas"
```

**Search across multiple books at once**:

```bash
python3 scripts/query_library.py m20-core/book_chunks.db blood-treachery/book_chunks.db "search terms"
```

Full-text search (all scripts) supports phrase queries (`"exact
phrase"`), boolean operators (`term1 AND term2`, `term1 NOT term2`),
and prefix matching (`term*`). Hyphens and apostrophes in unquoted
multi-word queries can trigger an FTS5 syntax error (e.g.
`Fitz-Empress`, `Wizards' March`) — if that happens, drop the
punctuation or wrap the phrase in escaped double quotes and retry.

**Note on page numbers:** every book's PDF has a small front-matter
offset between the PDF's own page count and the book's printed page
footers (+1 for `m20-core`, `m20-how-do-you-do-that`,
`m20-book-of-secrets`, and `blood-treachery`; +19 for
`mage-sorcerers-crusade`, which opens with an unnumbered 16-page
fiction Prelude). See each book's own README.md for its exact offset
— this matters if you're cross-referencing against a physical/PDF
copy rather than just this bundle.

## Requirements

Python 3 with the standard library only (`sqlite3` is built in — no
extra packages to install).

## Notes on scope

- This bundle contains **summaries and short paragraph-level excerpts**
  for search/citation purposes, not the original books' full text.
  It's a research aid for someone who already owns the source PDFs,
  not a substitute for them.
- Mechanically dense sections (character creation Traits, dice-pool
  rules, combat systems, spellcasting systems, ghoul-mage rules) are
  noted as reference material in each book's own `book_index.md`
  rather than summarized rule-by-rule — query the relevant
  `book_chunks.db` directly for that content.

## Adding another related book later

Bring the new PDF plus this repo's existing `library_index.md` and
each existing book's `book_index.md` (the chunk databases and original
PDFs aren't needed again). Run the book-indexer skill's indexing
workflow on just the new book to produce its own `<slug>/` bundle, add
it alongside the existing book folders in this library directory, then
refresh `library_index.md` and this README's tables/tree/"Before you
use this library" section to fold the new book in — see
`references/cross_book_index.md` → "Adding a book later" in the
book-indexer skill for the exact update pattern and the required
re-zip-and-verify packaging steps.
