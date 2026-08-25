# Mage: The Ascension — Cross-Book Index

## Books in this collection

**M20 line** (20th Anniversary Edition, modern-day retrospective,
published 2015-2016):
- `m20-core/` — Mage: The Ascension 20th Anniversary Edition (core rulebook), 698 pages
- `m20-how-do-you-do-that/` — Mage 20: How Do You DO That? — A Practical Guide to Sphere Magick, 143 pages

**Classic-era, 2nd Edition line** (Renaissance-setting, published 1998):
- `mage-sorcerers-crusade/` — Mage: The Sorcerers Crusade, 317 pages

**Classic-era, Revised Edition line** (modern-day "Final Nights"
metaplot, published 2004):
- `blood-treachery/` — Blood Treachery, 96 pages

## How to use this file
This file synthesizes themes across the four books above. For
details on any single book, read that book's own `book_index.md` in
its subdirectory. For exact quotes/facts, query that book's
`book_chunks.db`, or use `scripts/query_library.py` to search across
all four databases at once (see usage below).

## A note on editions — read this before cross-referencing

This library spans **three distinct editions/eras** of *Mage: The
Ascension*, not one continuous canon:

1. **M20** (`m20-core`, `m20-how-do-you-do-that`) — a 2015-2016
   *20th Anniversary retrospective* line: a consolidated, updated
   synthesis of modern-day Mage. `m20-how-do-you-do-that` is an
   explicit, subordinate rules companion to `m20-core`.
2. **Classic, 2nd Edition** (`mage-sorcerers-crusade`) — a 1998
   *prequel* sourcebook set roughly 500 years before the modern
   setting (Renaissance Europe), synced to the 1996 Second Edition
   ruleset. Standalone and playable on its own.
3. **Classic, Revised Edition** (`blood-treachery`) — a 2004
   sourcebook set in the *same modern-day period* `m20-core` itself
   describes (post-Doissetep, pre-Time-of-Judgment "Final Nights"),
   synced to the 2000 Revised ruleset — 11 years *before* M20 existed,
   telling its own version of that period's metaplot.

**Practical implication:** `blood-treachery` and `m20-core` are the
closest pair in this library — same in-fiction period, same core
mechanics (Paradox, Quintessence, the Nine Spheres essentially
unchanged), largely the same underlying design lineage. But
`blood-treachery` is a *contemporary* account written when its
events were being treated as fixed, ongoing continuity, while
`m20-core` is a *later retrospective* written specifically to make
that same era's metaplot optional (see "Points of disagreement"
below for a concrete case where M20 quietly did not carry a
Revised-era development forward). `mage-sorcerers-crusade` sits apart
from both — a different century, a different core punishment
mechanic (the Scourge, not Paradox), and a genuinely different
Council-of-Nine roster, but the same deep-history setting all three
other books ultimately point back to.

## Cross-cutting themes

### The Massasa War, told at both ends: origin and renewal
- **mage-sorcerers-crusade** (Ch. II, p.53-54) documents the *first*
  Massasa War's opening moves in its Convocation Period timeline:
  House Tremere's betrayal of House Diedne, the 1201-1325 war of
  attrition against the newly-undead House, and the 1210 Fall of
  Mistridge — explicitly dated as "the official beginning of the
  Ascension War" — caused in part by a Tremere-loyalist traitor
  (Grimgroth) inside the besieged Covenant.
- **blood-treachery** picks up the *same* named war roughly 800 years
  later: its own "What Happened to House Tremere?" sidebar (p.55)
  recaps the identical origin (Tremere's betrayal of House Diedne,
  the founder's own transformation, the war's eventual quiet
  stalemate) before telling the story of the war's violent renewal —
  a second, modern-day **Wizards' March** formally declared against
  House Tremere on January 21, 2000 (Act One, p.27).
- The two books' figures for "how long ago" line up closely:
  `mage-sorcerers-crusade` dates the war's start to ~1201-1210;
  `blood-treachery`, writing from a ~2000 present, repeatedly says
  "800 years" (Introduction, p.13; the Former Tremere character,
  Act Two, p.38) — arithmetic that lands almost exactly on
  `mage-sorcerers-crusade`'s own dates.

### Mistridge: the Order's one shared trauma, invoked across all three modern/prequel books
- **mage-sorcerers-crusade** establishes Mistridge as a major
  Hermetic Covenant with a violent history (a Craftmason siege ending
  in betrayal, Ch. I's Crays/Covenants table, Ch. II's Convocation
  timeline) and as the site the Ascension War is dated from.
- **blood-treachery** invokes it twice as a moral touchstone rather
  than a place: a Former Tremere sparing a cornered Hermetic cabal
  tells them to "save your Mistridge" (Act Two, p.40) as shorthand for
  everything worth protecting, and the same figure's later monologue
  (Act Three, p.52-53) reveals *he personally* destroyed Mistridge
  eight centuries earlier, out of disgust with his own pride — using
  the site's fall as his own cautionary example to the Order.
- `m20-core` does not focus on Mistridge specifically, but its own
  Doissetep-focused version of the same "a Hermetic stronghold falls
  because of internal pride" story (see below) is structurally the
  same cautionary shape repeated at a different Covenant, centuries
  later.

### Porthos Fitz-Empress and Doissetep, across three books and roughly 550 years
This is the single richest individual-character throughline in the
library, now spanning all three narrative-driven books:
- **mage-sorcerers-crusade** (Ch. II, p.56) places "young Porthos
  Fitz-Empress" at the 1448 Siege of Doissetep, where Hermetic magi
  shift the besieged Covenant into the Otherworlds to save it.
- **blood-treachery**, set roughly 550 years later, twice references
  Doissetep's destruction and "the death of Porthos Fitz-Empress"
  (Act One, p.19-20) as recent, already-settled history that has left
  the Order — House Flambeau especially — reeling.
- **m20-core** (Ch. 1, p.51) supplies the full account joining the two:
  the same named Hermetic Archmaster, now elderly and renowned,
  sacrifices his own life in 1997 to contain Doissetep's catastrophic
  implosion — the exact event `blood-treachery` treats as recent past
  only a few years later, and the far-future echo of the young man
  present at the Covenant's near-fall in `mage-sorcerers-crusade`.

### The Council of Nine's membership: three data points across three centuries
- **mage-sorcerers-crusade** dates the Council's 1466 founding roster
  precisely, with **Ahl-i-Batin** and **Solificati** as two of the
  original nine Traditions.
- **blood-treachery** (Act One, p.21) adds a third data point from
  roughly 2000: the Solificati's descendant Craft, **the Children of
  Knowledge**, "surprised everyone" by formally rejoining the Order of
  Hermes as its **tenth House**, resolving the 1500-era schism
  `mage-sorcerers-crusade` documents.
- **m20-core**, however — the *latest* retrospective account,
  published 2015 — describes the Children of Knowledge as still an
  independent **Disparate Craft**, not a House of the Order, with no
  mention of the 2000-era reunification `blood-treachery` describes.
  This is the clearest concrete case in this library of a Revised-era
  metaplot development that M20's own retrospective simply did not
  carry forward — worth flagging directly if a question turns on
  Solificati/Children of Knowledge status, since the honest answer is
  "it depends which book's continuity you're using," not a single
  fixed fact.

### Mechanics: Blood Treachery and m20-core share a lineage that Sorcerers Crusade doesn't
- **blood-treachery** and **m20-core** use essentially the same core
  systems — Paradox (not the Scourge), Quintessence, Gilgul, and the
  same Nine Spheres — because both descend from the same
  post-Revised-Edition rules lineage, 11 years apart.
- **mage-sorcerers-crusade** is the outlier: its Scourge system (moral/
  virtue-based backlash) is a genuinely different mechanic from
  Paradox, not just an early or simplified version of it — see that
  book's own `book_index.md` and the existing note on this below.
- Practical implication: a rules question about Paradox, Quintessence
  costs, or Sphere mechanics can usually be answered consistently from
  either `blood-treachery` or `m20-core`; a rules question sourced
  from `mage-sorcerers-crusade` needs its own Scourge-specific
  treatment and shouldn't be assumed to carry over.

### Shared vocabulary roots, openly acknowledged
(Carried forward from the two-book synthesis; still accurate.)
Several `m20-core` terms are direct, traceable descendants of
`mage-sorcerers-crusade` terminology: **Vain Magick** → **Vulgar
Magick**; **Casual Magick** → **Coincidental Magick**; **Daemon** →
**Avatar** (though the two books' Essence taxonomies for that inner
power don't match — see `mage-sorcerers-crusade/book_index.md`).
`blood-treachery` does not introduce comparably traceable new
vocabulary of its own — its terms (**massasa** for vampires, the
**Wizards' March** itself) appear to be local to the Revised-era
Hermetic-vampire-war material and are not picked up in `m20-core`'s
own text.

## Points of agreement
- **Core chronology matches exactly where books overlap**: the Order
  of Hermes' founding (767 CE) and the Convention of the White Tower
  (1325) match exactly between `mage-sorcerers-crusade` and `m20-core`
  (see the prior two-book synthesis below); the Massasa War's rough
  dating and Doissetep/Porthos Fitz-Empress's fate match across all
  three narrative books (see above).
- **`blood-treachery` and `m20-core` agree on every event they both
  touch** — Doissetep's fall, Porthos's death, the general shape of
  "the Order in crisis" — they simply differ in how *fixed* that
  crisis is treated as being (see below).
- **`m20-how-do-you-do-that` and `m20-core` remain in full agreement**
  with each other (see the existing pairwise note below) — unaffected
  by either of the other two books' addition to this library.

## Points of disagreement or tension
- **Solificati/Children of Knowledge's status** — full House of the
  Order (`blood-treachery`, ~2000) vs. independent Disparate Craft
  (`m20-core`, 2015) — see above. The clearest concrete continuity
  break in this library.
- **How fixed is "the Reckoning"/Doissetep's fall?** `blood-treachery`
  (2004) treats these events as settled, non-optional canonical
  history — it has no equivalent of M20's own "Future Fates" device.
  `m20-core` (2015) explicitly reframes the *same* events as one of
  three Storyteller-optional interpretations. Interestingly, the
  "Future Fates" mechanic itself originates even earlier, in
  `mage-sorcerers-crusade` (1998) — so the tool for making this era's
  events optional existed years before `blood-treachery` was written,
  but `blood-treachery` doesn't use it; only `m20-core`, later,
  retroactively applies that same optionality to the era
  `blood-treachery` treated as fixed.
- **Council of Nine membership** and **the Scourge vs. Paradox** and
  **Avatar Essence taxonomy** and **Otherworld cosmology terminology**
  — all carried forward unchanged from the prior two-book synthesis;
  see below and each book's own `book_index.md`.
- **No disagreement identified between `m20-core` and
  `m20-how-do-you-do-that`** — unaffected by this update.

## Chronology / influence
- **In fictional time**: `mage-sorcerers-crusade` (c. 1400s-1500s)
  comes first by roughly five centuries; `blood-treachery` (~2000) and
  `m20-core`/`m20-how-do-you-do-that` (present-day, written 2015) are
  set within a few years of each other, in the same broad "post-
  Doissetep, pre-Time-of-Judgment" period.
- **In real-world publication order**: `mage-sorcerers-crusade` (1998)
  → `blood-treachery` (2004) → `m20-core` and `m20-how-do-you-do-that`
  (2015-2016). `m20-core` is the *latest* book in this library despite
  being set in roughly the same period as `blood-treachery` — it is a
  retrospective consolidation, not a sequel, and per the point above,
  it doesn't treat everything `blood-treachery` describes as
  automatically still true.
- **Reading order recommendation**: start with `m20-core` for the
  modern-day baseline (best-documented, most current). Read
  `mage-sorcerers-crusade` for the deep-history version of the same
  setting. Read `blood-treachery` as a snapshot of how the modern-day
  "Final Nights" period was being told *before* M20's retrospective
  consolidation — useful for exactly the kind of "how did this
  metaplot thread actually play out" questions M20 itself glosses
  over, but treat any specific development it describes (like the
  Solificati reunification) as belonging to that snapshot rather than
  automatically true of `m20-core`'s own continuity unless confirmed
  there too.

## m20-core and m20-how-do-you-do-that: existing pairwise notes
(Retained from the original two-book synthesis — still fully
accurate; neither newer book changes this relationship.)

`m20-how-do-you-do-that` is an explicit, subordinate companion to
`m20-core`, by the same author, written to extend that book's Chapter
Nine and Chapter Ten rather than to stand alone. It assumes
`m20-core`'s cosmology, factions, and core rules system without
re-explaining them, and its own text says to default to `m20-core`
whenever the two might seem to disagree. The clearest concrete link
between them is a shared example cast: **Lee Ann Milner** and **Jinx**
(played by "Camille" in `m20-core`'s own Chapter Seven worked example)
both recur throughout `m20-how-do-you-do-that` as its default
worked-example mages. Coincidental vs. vulgar magick, Focus
(paradigm+practice+instrument), and Quintessence/Resonance are all
introduced as cosmology in `m20-core` and operationalized as granular
mechanics in `m20-how-do-you-do-that` — see `m20-core/book_index.md`
and `m20-how-do-you-do-that/book_index.md` for the full detail on each.

## Cross-book query examples
```bash
python3 scripts/query_library.py m20-core/book_chunks.db mage-sorcerers-crusade/book_chunks.db blood-treachery/book_chunks.db "Mistridge"
```
```bash
python3 scripts/query_library.py m20-core/book_chunks.db blood-treachery/book_chunks.db "Porthos Fitz Empress"
```
```bash
python3 scripts/query_library.py mage-sorcerers-crusade/book_chunks.db blood-treachery/book_chunks.db "Massasa War Tremere"
```
```bash
python3 scripts/query_library.py m20-core/book_chunks.db blood-treachery/book_chunks.db "Solificati Children of Knowledge"
```
(Replace the slug paths with whichever subset of books is relevant to
the question — the slug names shown above are what appears in the
grouped results, so use them as written.)

**A query-syntax gotcha worth knowing:** these scripts pass your query
straight to SQLite FTS5, which gives special meaning to hyphens and
apostrophes in unquoted multi-word queries (e.g. `Fitz-Empress` or
`Wizards' March` can throw a syntax error rather than searching for
that text). If a query errors out, drop the hyphen/apostrophe
(`Fitz Empress`) or wrap the exact phrase in escaped double quotes
(`'"Wizards March"'`) and try again.
