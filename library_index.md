# Mage: The Ascension — Cross-Book Index

## Books in this collection

**M20 line** (20th Anniversary Edition, modern-day retrospective,
published 2015-2017):
- `m20-core/` — Mage: The Ascension 20th Anniversary Edition (core rulebook), 698 pages
- `m20-how-do-you-do-that/` — Mage 20: How Do You DO That? — A Practical Guide to Sphere Magick, 143 pages
- `m20-book-of-secrets/` — Mage 20: The Book of Secrets, 301 pages

**Classic-era, 2nd Edition line** (Renaissance-setting, published 1998):
- `mage-sorcerers-crusade/` — Mage: The Sorcerers Crusade, 317 pages

**Classic-era, Revised Edition line** (modern-day "Final Nights"
metaplot, published 2004):
- `blood-treachery/` — Blood Treachery, 96 pages

## How to use this file
This file synthesizes themes across the five books above. For
details on any single book, read that book's own `book_index.md` in
its subdirectory. For exact quotes/facts, query that book's
`book_chunks.db`, or use `scripts/query_library.py` to search across
all five databases at once (see usage below).

## A note on editions — read this before cross-referencing

This library spans **three distinct editions/eras** of *Mage: The
Ascension*, not one continuous canon:

1. **M20** (`m20-core`, `m20-how-do-you-do-that`,
   `m20-book-of-secrets`) — a 2015-2017 *20th Anniversary
   retrospective* line: a consolidated, updated synthesis of
   modern-day Mage. `m20-how-do-you-do-that` and
   `m20-book-of-secrets` are both explicit, subordinate companions to
   `m20-core` — the former a Sphere-magick rules expansion, the
   latter a miscellany of cut material (character options, optional
   rules, expanded Focus content, and a chapter on inter-faction
   justice/influence). Neither introduces a competing continuity;
   both assume and build on `m20-core`'s own.
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

### Porthos Fitz-Empress and Doissetep, across four books and roughly 550 years
This is the single richest individual-character throughline in the
library, now spanning all three narrative-driven books plus a fourth,
non-narrative cameo:
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
- **m20-book-of-secrets** adds two small but genuine touches rather
  than new narrative: its Introduction (p.11) opens with an unnamed
  mage exploring ruins still saturated with "Archmaster Porthos"'s
  lingering presence — an atmospheric coda consistent with, but not
  adding facts to, `m20-core`'s account of his death — and its
  Wonders chapter (p.163-164) attributes an in-setting Primer/game
  called *Oracle: The Essence* to Porthos "by rumor," calling it
  "Porthos' final enterprise" after his prior publication *The
  Fragile Path* (itself a title shared with a real M20 sourcebook).
  This is worldbuilding texture, not confirmed fact — the book itself
  flags it as rumor. Separately, this book's own author FAQ (Chapter
  Five, p.260) states in the author's voice that he has "never said
  that... you must kill off Porthos or detonate Doissetep in your own
  chronicle" — direct authorial confirmation that this entire
  throughline is a Storyteller-optional "Future Fate," not
  mandatory canon (see "Points of disagreement" below).

### Voormas: a rumor in one book, a resolution in another
- **m20-core** (Ch. 1, p.51, and Ch. 5's "Fallen Traditions?" sidebar,
  p.140) raises Voormas only as an unresolved rumor: an infamous
  "death-mage" whose name mages invoke as a cautionary example of
  corruption, and one of the pieces of circumstantial evidence
  offered (alongside Doissetep's implosion and the Ascension
  Warrior) for the theory that Nephandi may have infiltrated the
  Traditions' own leadership. The chapter deliberately leaves the
  theory unconfirmed.
- **m20-book-of-secrets** (Ch. 4, p.216, p.219) treats Voormas's
  corruption as settled past history rather than live rumor: "the
  atrocities of Voormas" are cited as the reason the Traditions no
  longer let Thanatoic mages handle executions by default, and
  Voormas and his rogue cabal are confirmed to have been formally
  **Interdicted** (an in-absentia death sentence), then "hunted down
  and destroyed by their fellow Euthanatoi."
- **Practical implication:** read together, the two books tell a
  clean before-and-after story — m20-core shows Voormas as a live
  question mark used to fuel Fallen-infiltration paranoia, and
  Book of Secrets confirms the case was eventually closed, with
  consequences (changed Tradition execution customs) that persist
  into the present day both books share. Book of Secrets does not
  resolve the broader "are the Traditions secretly Nephandi-run?"
  question m20-core raises — it only confirms this one specific,
  named case.

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
- **`m20-book-of-secrets` and `m20-core` agree on every case they
  both touch, and one of them (Voormas) moves from open rumor to
  confirmed history** — see "Voormas" above. Book of Secrets also
  shares `m20-core`'s and `blood-treachery`'s core mechanical
  lineage outright: its Gilgul Rite, Wonder-crafting rules, and
  Resonance system all use the same Paradox/Quintessence/Gilgul/Nine
  Spheres framework, not `mage-sorcerers-crusade`'s Scourge-based one
  (see "Mechanics" above).

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
  `blood-treachery` treated as fixed. `m20-book-of-secrets` (2017)
  confirms this reading directly and in the author's own voice — its
  Chapter Five FAQ states outright that Porthos's death, Doissetep's
  fall, and even the Avatar Storm itself are deliberately left
  Storyteller-optional so as not to force one "Reckoning vs. Avatar
  Storm" camp's preferred metaplot onto the other (see "Porthos
  Fitz-Empress and Doissetep" above).
- **Council of Nine membership** and **the Scourge vs. Paradox** and
  **Avatar Essence taxonomy** and **Otherworld cosmology terminology**
  — all carried forward unchanged from the prior two-book synthesis;
  see below and each book's own `book_index.md`.
- **No disagreement identified between `m20-core` and
  `m20-how-do-you-do-that`, or between `m20-core` and
  `m20-book-of-secrets`** — unaffected by this update.

## Chronology / influence
- **In fictional time**: `mage-sorcerers-crusade` (c. 1400s-1500s)
  comes first by roughly five centuries; `blood-treachery` (~2000) and
  `m20-core`/`m20-how-do-you-do-that`/`m20-book-of-secrets`
  (present-day, written 2015-2017) are set within a few years of each
  other, in the same broad "post-Doissetep, pre-Time-of-Judgment"
  period. `m20-book-of-secrets` doesn't add new fictional-timeline
  events of its own (its two short fiction vignettes are undated
  mood pieces, not metaplot markers).
- **In real-world publication order**: `mage-sorcerers-crusade` (1998)
  → `blood-treachery` (2004) → `m20-core` (2015) →
  `m20-how-do-you-do-that` (2016) → `m20-book-of-secrets` (2017).
  `m20-book-of-secrets` is the *newest* book in this library; it is a
  companion/miscellany to `m20-core` (explicitly built from material
  cut from that book) rather than a sequel or a rival retrospective,
  and per the point above, its own author FAQ explicitly declines to
  add new mandatory metaplot on top of `m20-core`'s.
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
  there too. Read `m20-book-of-secrets` last and treat it as
  supplementary rather than foundational — it's the right place to
  look for expanded character-creation options, optional rules
  (Resonance, Wonder-crafting, certámen), inter-faction justice
  systems, and the author's own design commentary, but it assumes
  `m20-core`'s setting throughout and doesn't stand alone the way the
  other four books do.

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

`m20-book-of-secrets` uses the same shared cast far more lightly: Lee
Ann Milner turns up twice, both times as a generic stand-in name in
rules-example text (a hypothetical Time-Sphere Effect, p.273; a
hypothetical torture victim used to illustrate that Ordeal punishments
on prominent mages won't stay "internal," p.217) rather than as a
worked-example character in her own right — this book has its own
separate cast of six original Examples in Play characters for that
purpose (see its own `book_index.md`). The connection is real but
thin; don't expect Book of Secrets to develop Lee Ann's arc the way
`m20-how-do-you-do-that` does.

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
```bash
python3 scripts/query_library.py m20-core/book_chunks.db m20-book-of-secrets/book_chunks.db "Voormas"
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
