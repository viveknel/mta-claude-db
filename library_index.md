# Mage: The Ascension — Cross-Book Index

## Books in this collection

**M20 line** (20th Anniversary Edition, modern-day retrospective,
published 2015-2016):
- `m20-core/` — Mage: The Ascension 20th Anniversary Edition (core rulebook), 698 pages
- `m20-how-do-you-do-that/` — Mage 20: How Do You DO That? — A Practical Guide to Sphere Magick, 143 pages

**Classic-era line** (original, pre-M20, published 1998):
- `mage-sorcerers-crusade/` — Mage: The Sorcerers Crusade, 317 pages

## How to use this file
This file synthesizes themes across the three books above. For
details on any single book, read that book's own `book_index.md` in
its subdirectory. For exact quotes/facts, query that book's
`book_chunks.db`, or use `scripts/query_library.py` to search across
all three databases at once (see usage below).

## A note on editions — read this before cross-referencing

This library spans **two distinct editions/eras** of *Mage: The
Ascension*, and they are not simply the same continuity at different
dates — they're separate publication lines, written 17 years apart,
describing different centuries of the same fictional history.

1. **M20** (`m20-core`, `m20-how-do-you-do-that`) is a 2015-2016
   *20th Anniversary retrospective* line: a consolidated, updated
   synthesis of modern-day (present-day-set) Mage, aimed at both new
   and returning players. `m20-how-do-you-do-that` is an explicit,
   subordinate rules companion to `m20-core` by the same author — see
   below.
2. **Mage: The Sorcerers Crusade** (`mage-sorcerers-crusade`) is a
   *classic-era, pre-M20* sourcebook from 1998, synced to the 1996
   Second Edition ruleset — not an M20 product at all. It's a
   standalone, playable-on-its-own core rulebook set roughly 500 years
   *before* `m20-core`'s modern setting (Renaissance Europe, c.
   1400s-1500s), functioning as Mage's counterpart to Vampire: The
   Dark Ages — the same setting's own deep past, not a competing
   version of the present.

**Practical implication:** `mage-sorcerers-crusade` and `m20-core`
describe the *same* fictional world centuries apart, written by
overlapping creative teams (Phil Brucato leads both) who deliberately
carried specific names, dates, and even individual characters forward
across that gap — several of which are genuinely remarkable and
verified below. But they are not mechanically or terminologically
identical: the further into a topic's specific rules or faction
roster you go, the more you should expect real, documented divergence
rather than assume seamless continuity. Where the two disagree, that's
usually because roughly 500 in-fiction years and 17 real-world years
of design evolution sit between them — not an error in either book.

## Cross-cutting themes

### Pride and consequence as the constant, across 500 years and two very different punishment mechanics
- **m20-core** frames pride/hubris as its explicit central thesis (see
  its own Cross-cutting themes) and mechanizes magickal overreach
  through **Paradox** — a reality-consensus backlash tied to how
  blatantly a mage's act violates the Masses' belief in what's
  possible (Ch. 2, p.56-65).
- **mage-sorcerers-crusade** tells the *identical* moral story — magick
  as a burden that punishes the proud — through **the Scourge** (Ch. I,
  p.42; full system Ch. VIII, p.232-237), but the mechanism is
  explicitly Divine/moral rather than consensus-based: Boons and Banes
  are keyed directly to Christian Cardinal/Theological Virtues, Pagan
  Virtues, and the Seven Deadly Sins, not to how "vulgar" an effect
  looks to onlookers.
- `m20-core` itself is aware of this lineage — its own Chapter Two
  explicitly describes a historical Scourge that "once punished vain
  magick before Paradox took over that role" (see `m20-core/book_index.md`).
  Reading `mage-sorcerers-crusade` Ch. VIII is the only way to see that
  predecessor system in its full, playable, mechanically distinct
  form — it is a genuinely different game system serving the same
  thematic role, not a simplified early draft of Paradox.

### The Council of Nine's membership is not fixed across 500 years — it's a documented, dated turnover
- **mage-sorcerers-crusade** (Ch. II, p.56) gives the Council's exact
  1466 founding roster: Akashic Brotherhood, **Ahl-i-Batin**,
  Chakravanti/Euthanatoi, Celestial Chorus, Dream-speakers, Order of
  Hermes, Seers of Chronos/Sahajiya, **Solificati**, and Verbena — nine
  seats, two of which (Ahl-i-Batin and Solificati) are held by groups
  that `m20-core` lists only as **Disparate Crafts**, not Traditions
  (see `m20-core/book_index.md`, Ch. 5 Part IV).
- **m20-core**'s modern Nine swaps those same two seats for **Sons of
  Ether** and **Virtual Adepts** — neither of which could have existed
  in 1466: `mage-sorcerers-crusade` itself (Ch. V, p.142-143) narrates
  their origin as 17th-century Order of Reason splinter groups
  (Electrodyne Engineers and Difference Engineers) who defect to the
  Council centuries later.
- `mage-sorcerers-crusade` also tracks the Solificati's own exit in
  real time: broken by internal betrayal in 1470, the last 12 members
  rename themselves **the Children of Knowledge** in 1500 (Ch. II,
  p.57) and refuse to rejoin the Council — which is exactly the
  Disparate Craft `m20-core` describes under that same name (see
  `m20-core/book_index.md`, Ch. 5 Part IV). Ahl-i-Batin's own path from
  full Tradition to Disparate Craft isn't narrated in either book in
  this library; treat it as an open thread rather than an error.
- **Practical implication**: a question like "is Ahl-i-Batin a
  Tradition or a Disparate Craft" has a *different correct answer
  depending on the century* — check which book's timeframe the
  question actually concerns before answering from just one source.

### The Technocracy's five Conventions, traced back to their own named ancestors
- **m20-core** (Ch. 5, Part III) describes the five modern Technocratic
  Conventions — Iteration X, New World Order, Progenitors, Syndicate,
  Void Engineers — as settled fact, with only brief gestures at their
  deeper history.
- **mage-sorcerers-crusade** supplies the missing chapter: the Order of
  Reason's 1325 founding roster (Ch. II, p.54-55) names **seven**
  Conventions — Artificers, Cabal of Pure Thought/Gabrielites, Celestial
  Masters, Craftmasons, High Guild, Hippocratic Circle, Void Seekers —
  plus a secret eighth group, the Ksirafai ("Razors"), unlisted among
  the Conventions. A single passage (Ch. V, p.142-143) then explicitly
  narrates the consolidation into M20's familiar five: Artificers become
  Iteration X; Celestial Masters absorb Void Seekers to become Void
  Engineers; High Guild becomes the Syndicate; Hippocratic Circle
  becomes the Progenitors; and the Cabal of Pure Thought's collapse,
  alongside the Ksirafai's hidden hand, gives rise to the New World
  Order.
- This is presented in `mage-sorcerers-crusade` as connective lore
  `m20-core` doesn't itself contain in this much depth, not as a
  contradiction — a genuinely valuable case where reading both books
  together produces a fuller picture than either alone.

### A named character who ages across five centuries: Porthos Fitz-Empress
- **mage-sorcerers-crusade** (Ch. II, p.56) places "young Porthos
  Fitz-Empress" at the 1448 Siege of Doissetep, where Hermetic magi
  shift the besieged Covenant into the Otherworlds to save it.
- **m20-core** (Ch. 1, p.51) describes the same named Hermetic
  Archmaster — now elderly and renowned — sacrificing his own life to
  contain Doissetep's catastrophic implosion in 1997, roughly 550
  fictional years later.
- This is the single clearest individual-character throughline in the
  library: the same named mage present at his stronghold's near-fall
  as a young man, and its actual fall as an old one, confirmed in two
  books written 17 years apart by overlapping authors.

### Otherworld cosmology: elaborated, not contradicted, over five centuries
- **mage-sorcerers-crusade** (Ch. III, p.79) describes a three-layer
  Otherworldly cosmology — the Penumbra, a middle layer called
  **Veshaya**, and Horizon, collectively "L'umbra Haute," with the
  Contrarium as its shadow-underside.
- **m20-core** (Ch. 4) describes a considerably more elaborate system
  — Penumbra, Astral/High Umbra, Middle Umbra, Low Umbra/Underworld,
  Horizon, the Digital Web, and the Second Horizon/Etherspace — and
  the term "Veshaya" does not appear to survive into M20's vocabulary
  at all.
- Read as five centuries of setting elaboration (and, per `m20-core`'s
  own account, an Avatar Storm and Reckoning-era metaplot reshaping the
  Otherworlds in between) rather than a contradiction — but don't
  assume "Veshaya" means anything to an M20-only reader, and don't
  assume M20's Digital Web or Second Horizon have any equivalent in
  the Renaissance-era book.

### Shared vocabulary roots, openly acknowledged
Several `m20-core` terms are direct, traceable descendants of
`mage-sorcerers-crusade` terminology, not independent coinages:
- **Vain Magick** (`mage-sorcerers-crusade`, Introduction Lexicon, p.13)
  → **Vulgar Magick** (`m20-core`).
- **Casual Magick** (same Lexicon entry) → **Coincidental Magick**
  (`m20-core`).
- **Daemon** (`mage-sorcerers-crusade` Ch. I) → **Avatar** (`m20-core`)
  — though the two books' four-part *Essence* taxonomies for that same
  inner power don't match: Castellum/Furo/Mare/Susurro (four classical
  elements, `mage-sorcerers-crusade`) versus Dynamic/Pattern/Questing/
  Primordial (four archetypal drives, `m20-core`). Same structural idea
  — a fourfold Essence typology — different specific system; don't
  treat them as interchangeable.
- **Gilgul**, **Quintessence**, **Tass**, **Resonance**, and the **Nine
  Spheres**' governing principles (Correspondence/Connection, Entropy,
  Forces, Life, Matter, Mind, Prime, Spirit, Time) are stable across
  both books almost unchanged — these are the parts of the system that
  genuinely didn't need updating.

## Points of agreement
- **Core chronology matches exactly where both books cover the same
  event**: the Order of Hermes' founding (767 CE) and the Convention of
  the White Tower founding the Order of Reason (1325) are dated
  identically in both `mage-sorcerers-crusade` (Ch. II) and `m20-core`
  (Ch. 5, Part I) — genuine cross-book consistency, not just thematic
  echo.
- **The Great Betrayer**: both books name the same individual, **Heylel
  Teomim**, a Solificati representative, as the betrayer of the First
  Cabal — `mage-sorcerers-crusade` (Ch. II, p.56-57) gives the full
  1466-1470 event in detail; `m20-core` (Ch. 1, Ch. 5) references it as
  established, centuries-old history.
- **`m20-how-do-you-do-that` and `m20-core` remain in full agreement**
  with each other (see that pair's existing synthesis below) — the
  addition of `mage-sorcerers-crusade` doesn't change anything about
  that relationship, since it's a different book entirely from a
  different era.

## Points of disagreement or tension
- **Council of Nine membership** (Ahl-i-Batin and Solificati as full
  Traditions in `mage-sorcerers-crusade`'s 1466 vs. Disparate/departed
  status in `m20-core`'s modern day) — see above; a dated turnover, not
  a contradiction, but the single most practically important
  divergence to flag if a question doesn't specify an era.
- **The Scourge vs. Paradox** — see above; genuinely different game
  mechanics (moral/virtue-based vs. consensus-based) even though
  `m20-core` explicitly frames one as the historical predecessor of
  the other.
- **Avatar Essence taxonomy** (four classical elements vs. four
  archetypal drives) — see above.
- **Otherworld cosmology terminology** ("Veshaya" and the simpler
  Three-Rings model vs. M20's much more elaborate multi-layer Umbra) —
  see above.
- **No disagreement identified between `m20-core` and
  `m20-how-do-you-do-that`** — see that pair's existing note below;
  this remains true regardless of what else is in the library.

## Chronology / influence
Fictional chronology and real-world publication order point in
opposite directions here, and both matter:
- **In fictional time**, `mage-sorcerers-crusade` (c. 1400s-1500s) comes
  first by roughly five centuries; `m20-core` and
  `m20-how-do-you-do-that` are set in the present day.
- **In real-world publication order**, `mage-sorcerers-crusade` (1998)
  predates `m20-core` (2015) by 17 years — meaning the "prequel" was
  written first, and several of `m20-core`'s own devices (the Future
  Fates sidebar mechanic, most visibly) were carried forward from it
  rather than invented fresh.
- **Reading order recommendation**: start with `m20-core` for the
  modern-day baseline (it's the line's flagship and best-documented
  book), then read `mage-sorcerers-crusade` for the deep-history
  version of the same setting — treat it as *Mage's* answer to Vampire:
  The Dark Ages, not as a simpler early draft of `m20-core`.
  `m20-how-do-you-do-that` only makes sense after `m20-core` (see
  below) and has no real relationship to `mage-sorcerers-crusade` at
  all — the two don't overlap in era or content.

## m20-core and m20-how-do-you-do-that: existing pairwise notes
(Retained from before `mage-sorcerers-crusade` was added — still fully
accurate; that book doesn't change this relationship.)

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
python3 scripts/query_library.py m20-core/book_chunks.db mage-sorcerers-crusade/book_chunks.db "Doissetep"
```
```bash
python3 scripts/query_library.py m20-core/book_chunks.db mage-sorcerers-crusade/book_chunks.db "Ahl-i-Batin"
```
```bash
python3 scripts/query_library.py m20-core/book_chunks.db mage-sorcerers-crusade/book_chunks.db "Scourge Paradox"
```
```bash
python3 scripts/query_library.py m20-core/book_chunks.db m20-how-do-you-do-that/book_chunks.db "Quintessence"
```
(Replace the slug paths with whichever subset of books is relevant to
the question — the slug names shown above are what appears in the
grouped results, so use them as written.)
