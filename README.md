# Mage: The Ascension — Searchable Library

A searchable index of *Mage: The Ascension* sourcebooks, built so that
questions about the setting can be answered without re-reading the
original PDFs. Each book has its own self-contained bundle (thematic
index + full-text search database), plus a cross-book synthesis layer
on top for questions that span multiple books.

## What's in here

**M20 line** (20th Anniversary Edition, modern-day, 2015-2016):

| Book | Folder | Pages |
|---|---|---|
| Mage: The Ascension 20th Anniversary Edition (core rulebook) | `m20-core/` | 698 |
| Mage 20: How Do You DO That? — A Practical Guide to Sphere Magick | `m20-how-do-you-do-that/` | 143 |

**Classic-era line** (pre-M20, Renaissance-setting, 1998):

| Book | Folder | Pages |
|---|---|---|
| Mage: The Sorcerers Crusade | `mage-sorcerers-crusade/` | 317 |

```
.
├── README.md                       ← you are here
├── library_index.md                 ← cross-book synthesis (read for broad/comparative questions)
├── scripts/
│   └── query_library.py             ← search all three books' databases at once
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
└── mage-sorcerers-crusade/
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

This library spans **two distinct editions/eras**, not one continuous
canon:

- `m20-core` and `m20-how-do-you-do-that` are the **M20 line** —
  modern-day-set, 2015-2016, and `m20-how-do-you-do-that` is an
  explicit, subordinate rules companion to `m20-core` (same author,
  same rules edition, no independent lore of its own).
- `mage-sorcerers-crusade` is a **classic-era, pre-M20 book from
  1998**, set roughly 500 years earlier in the same fictional world
  (Renaissance Europe) — Mage's counterpart to Vampire: The Dark Ages.
  It is fully standalone and playable on its own, and it is **not**
  mechanically or terminologically identical to the M20 books, even
  though the two eras share real history, several named characters,
  and a surprising number of direct textual echoes.

See `library_index.md` for the full picture — it documents both the
genuine connections (a named character who appears young in one book
and dies centuries later in another; exact matching founding dates for
the Order of Hermes and the Technocracy's predecessor; the literal
origin of the "Future Fates" mechanic) and the genuine differences
(the Council of Nine's membership changes over the centuries; the
Scourge and Paradox are different game mechanics serving the same
narrative role; Avatar Essence types don't use the same taxonomy)
rather than smoothing either over.

## Quick start

**Broad or thematic question about a single book** ("what does M20 say
about the Nephandi", "how was the Council of Nine founded") — read
that book's own `book_index.md` directly; it's small enough to load in
full and answers most questions without any querying.

**Question that spans eras or books** ("is Ahl-i-Batin a Tradition or
a Disparate Craft", "how did the Technocracy's Conventions change over
time") — read `library_index.md` first; it's built specifically for
this and will often tell you the answer depends on which century you
mean.

**Exact quote, precise fact, or page-number lookup within one book** —
query that book's chunk database directly:

```bash
python3 m20-core/scripts/query_chunks.py m20-core/book_chunks.db "Doissetep"
python3 mage-sorcerers-crusade/scripts/query_chunks.py mage-sorcerers-crusade/book_chunks.db "Convocation"
```

**Search across multiple books at once**:

```bash
python3 scripts/query_library.py m20-core/book_chunks.db mage-sorcerers-crusade/book_chunks.db "search terms"
```

Full-text search (all scripts) supports phrase queries (`"exact
phrase"`), boolean operators (`term1 AND term2`, `term1 NOT term2`),
and prefix matching (`term*`).

**Note on page numbers:** all three books' PDFs have front-matter
offsets between the PDF's own page count and the book's printed page
footers (a small +1 offset for the two M20 books, a larger +19 offset
for `mage-sorcerers-crusade`, which opens with an unnumbered 16-page
fiction Prelude). See each book's own README.md for the exact offset —
this matters if you're cross-referencing against a physical/PDF copy
rather than just this bundle.

## Requirements

Python 3 with the standard library only (`sqlite3` is built in — no
extra packages to install).

## Notes on scope

- This bundle contains **summaries and short paragraph-level excerpts**
  for search/citation purposes, not the original books' full text.
  It's a research aid for someone who already owns the source PDFs,
  not a substitute for them.
- Mechanically dense sections (character creation Traits, dice-pool
  rules, combat systems, spellcasting systems) are noted as reference
  material in each book's own `book_index.md` rather than summarized
  rule-by-rule — query the relevant `book_chunks.db` directly for that
  content.

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
