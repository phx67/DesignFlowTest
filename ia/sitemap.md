<!-- filled by /dsf:ia — start from this skeleton, do not restructure it -->

# Sitemap

Four sections, in this order: **Entities · Screens · Navigation · Traceability**.
Every screen serves a job. A screen with no job and a job with no screen are the same defect,
caught by the same matrix at the bottom of this file.

Jobs are referenced by their ids in `people/jtbd.md`: **Main**, **R1–R5**, **E1–E3**, **S1/S3**,
and **HJ1–HJ5** for the hypothesis jobs. Personas: **P1** (Даня, primary), **P2** (Валя),
**P3** (the author, entirely `[?]`).

---

## Entities

Objects before screens. The main things a person deals with in order to close their jobs.

| Entity | Fields and parts it contains | Which job produces it (`jtbd.md` reference) | Related to |
|---|---|---|---|
| **Work** | Title · images (1..n) · **unit type: `screen` \| `case`** (both first-class, brief 2026-08-07) · reality status + link to the live product · publication date · the task(s) it answers · author ref · breakdown ref | **Main** (the thing being read), **R2** (its realness is a field, not a separate object). Supply side is `[?]` — **HJ1/HJ2**, hypotheses | Author, Breakdown, Task, Collection |
| **Breakdown** | **Colour** — role + value + usage note · **Typography** — named scale + ratio · **Third axis** — base unit / density / spacing `[?]` *(the column grid was cut; the rename is this phase's job)* · each field carries **`confirmed` / `unconfirmed`** · plus **Intent** | **Main.** The one object the whole product exists to carry | Work (1:1), Facet value, Intent |
| **Intent** — *annotation* | **Form decided at the sitemap gate, 2026-08-07: intent is an annotation anchored to the work's own material.** The author points at a region of the image and says why it is that way. Fields: anchor (the region) · the reason · the breakdown field it touches, if any. Progression: **absent → present** (at least one annotation) **→ case** (annotations plus a narrative running across a multi-screen case) | **Main** (the half the market does not close, `[RES]` H1) · **R5**, **S1** read a single annotation as a quotable argument | Breakdown, Work. Never a form: this satisfies the gate's three constraints — carried by the material, optional, progressive, and **no compulsory "justify it" field anywhere** |
| **Facet value** | The value itself · the field it belongs to · **a live count of works carrying it** | **R1**, **Main.** The breakdown *is* the index — a value is a browsable object, not a string. Model: Fonts In Use, where every value is a link with its count (`fontsinuse-use-detail.png`) | Breakdown, Task |
| **Task** | Name · synonyms · count of works | **R1.** The named thing a person arrives with — "екран реєстрації", "кошик" `[INT · Даня · B1 Q6]`. This is the entry surface (H7, confirmed) | Work, Facet value |
| **Collection** | Name · owner · items (Work refs) · optional personal tags · **`[?]` a view that reads to a non-designer** | **R3** (get back to it), **E2** (P2: the eye grows). The `[?]` view is the **R4** question this phase was handed | Work, Author |
| **Author** — *attribution only* | Name · link | **No job produces it, and the gate ruled accordingly (2026-08-07): attribution stays, the screen goes.** The author appears as a **byline on `Work`**, not as a destination. R2 is closed by reality status and the live link; **follow is deferred to v2** | Work |

**Two entities are rendered inside a screen, never addressed as one** — stated here so phase 4 does
not go looking for a screen that was never intended (added at the critique gate, 2026-08-07):

- **Task** renders inside `Search`, as the named-task index. Promoting it to its own screen would
  split one entrance into two and cost a tap on the main job.
- **Facet value** renders inside `Results`, as the facet rail and as the count beside each value.
  A "facet value screen" would be `Results` with one filter pre-applied — the same screen, not a
  new one.

### Questionable

<!-- entities with no job behind them. They stay here until a job claims them or they are cut. -->

- **Quality mark** — **stays here by the gate's decision, 2026-08-07. `[RES]` H5 is therefore
  UNCONFIRMED in this version, and that is recorded, not quietly dropped.** H5 asked in as many
  words: *"Test in phase 3: the quality state and who may set it exist as objects in the IA."* They
  do not. The reason is that **no job in `jtbd.md` demands it** — it arrived from the benchmark
  (Discogs / Stack Overflow: the right to mark is earned by contributing), not from a person's
  stated need. **What carries the quality signal instead:** completeness on intent (*absent →
  present → case*) and the **confirmed / unconfirmed** state of the extracted values. No separate
  curation object is added. If the pool ever grows past the point where those two signals hold,
  this row is where the answer starts.
- **Tag** — assumed because the brief keeps tags as "optional personal context inside your own
  collections". **Closes no job**: R1 is closed by the Task taxonomy, and tags were cut as a
  retrieval mechanism at the MVP gate. Survives only as a field on Collection, never as an object
  with a screen.
- **Like** and **Follow** — **cut at the MVP gate**, listed here so their absence reads as a
  decision rather than an oversight.
- **Comment / discussion** — never asked in the interview, no job, no research finding demanding
  it. `[?]` — not proposed.

---

## Screens

**An indented text tree.** Next to every screen, the job it serves. `[P]` primary persona,
`[S]` secondary. States — empty, error, loading — are **not** screens; they belong to
`wireframes/_screens.md` in phase 4.

Derived from the jobs, not from a competitor's menu. The one structural debt to the market is
deliberate and recorded: the **entry is a task taxonomy with facets refining inside it** (H7 +
chosen pattern 1), because that is what the primary persona described doing.

**Confirmed at the sitemap gate, 2026-08-07** (`.design/decisions.md`). Six screens, no orphans.

```
Search  (Main, R1, E1, E3)                                        [P]
│   the entry: a search field over the declared fields, plus the named-task index
├── Results  (R1, Main, E1, R2)                                   [P]
│   │   facet rail over the breakdown fields; every card carries reality status,
│   │   confirmed/unconfirmed, and how far intent has got — R2 without a click
│   └── Work  (Main, R2, R5, S1)                                  [P]
│           the work AND its breakdown on one screen — the breakdown travels with
│           the work, so it is not a second screen. Holds 1..n images for a case.
│           ├─ values, each with its confirmed / unconfirmed state
│           ├─ intent as annotations on the material — absent / present / case
│           ├─ reality status + link to the live product
│           └─ author byline (attribution, not a destination — gate 2026-08-07)
│
Collections  (R3, E2)                                             [P]
└── Collection  (R3, E2, R4)                                      [P]
        one set, searchable by the breakdown fields — the thing no competitor
        does (Eagle does it privately and desktop-only, [RES · Re-research · Q3])
        └─ shared view: a MODE of this screen, not a screen (R4, gate 2026-08-07)
           hides designer-only chrome so a non-designer can read it

Publish  (HJ1, HJ2 — hypotheses only)  [HYPOTHESIS]                [S]
└── Confirm the extraction  (HJ1)     [HYPOTHESIS]                [S]
        marked at the critique gate: every job reaching this cluster is a
        hypothesis. It exists on the brief's success criterion 3, not on evidence.
        the machine's values come back as a draft; the author confirms or corrects.
        Intent is invited here and stays addable later — never compulsory.
```

**Three things this tree says out loud rather than hiding:**

1. **`Work` is one screen, not two.** Putting the breakdown on its own screen would add a tap to
   the main job and contradict the spine — the breakdown *travels with* the work.
2. **`Author` is not a screen.** Ruled at the gate: attribution stays as a byline on `Work`,
   the destination goes, follow waits for v2. The object had no job behind it and now has no
   screen either.
3. **The whole `Publish` cluster rests on hypothesis jobs.** HJ1 and HJ2 are unevidenced, and the
   supply side is the project's main risk. The screens exist because the brief's success criterion
   3 demands them, not because a person was observed needing them. **That is the weakest joint in
   this structure and it is load-bearing** — if HJ1 fails, this cluster is the first thing that
   changes.

---

## Navigation

**Global navigation — three items.** Three, not five: every candidate fourth item was either a
mode of an existing screen or a cut feature. An empty slot is cheaper than a slot filled "because
everyone has it".

| Item | Job cluster it opens | Why it earns a global slot |
|---|---|---|
| **Search** | Main · R1 · E1 · E3 | The brief fixes it: "the main screen is **search and filters, not a feed**". It is also the only entrance to the main job, and `[RES]` market pattern 1 says every competitor demotes search behind a feed — this is the deliberate inversion |
| **Collections** | R3 · E2 · R4 | R3 is MVP core job 3. The primary persona's loudest pain is losing his own saves — "90% моїх збережень це мертвий груз" `[INT · Даня · B3 Q3]` — and a cluster he cannot reach in one tap reproduces it |
| **Publish** | HJ1 · HJ2 · brief criterion 3 | The supply side. **The weakest of the three**: it opens hypothesis jobs only. It holds a global slot because a pool with no way in is not a product, not because a person was observed reaching for it |

**Rejected global items, so the absences read as decisions:** *Author / profile* — no job, ruled
out at the gate. *Following feed* — follow was cut at the MVP gate. *Tasks* — the task index lives
**inside** Search; promoting it would split one entrance into two. *Inbox / notifications* — no job,
no research finding.

**Tap-depth budget.** Taps from the first screen to the **main job**, for the **primary persona**.
Budget: **≤ 3**.

| Path (screen → screen → screen) | Taps | Within budget? |
|---|---|---|
| `Search` → type a query → `Results` → `Work` *(breakdown is on it)* | **2** | ✅ |
| `Search` → tap a named task → `Results` → `Work` | **2** | ✅ — the R1 entry, same depth |
| `Search` → `Results` → `Work` → an intent annotation *(R5, S1)* | **3** | ✅ at the edge |
| `Collections` → `Collection` → `Work` *(R3, returning)* | **2** | ✅ |
| `Publish` → `Confirm the extraction` → published *(HJ1)* | **2** | ✅ |

**Budget spent: 2 of 3 for the main job.** The one spare tap is deliberate and is spent in phase 4
on whatever the Work screen cannot hold at once — most likely the case narrative for a multi-screen
work. Later phases are held to this number.

**Why it stays at 2:** the breakdown is on the `Work` screen rather than behind it. Splitting them
would cost the third tap and buy nothing — and it would contradict the spine.

**Levels**

| Level | Screens | Why here |
|---|---|---|
| Global — always visible | `Search`, `Collections`, `Publish` | The three job clusters. Each is one tap from anywhere |
| Contextual — appears inside a flow | the facet rail on `Results`; `Confirm the extraction`; the shared **mode** of `Collection`; the annotation layer on `Work` | None of these makes sense outside the flow that produces it. The facet rail in particular is meaningless before a result set exists |
| Deep — rare actions | editing a published breakdown; correcting a confirmed value after the fact | Rare by definition — done once per work, usually right after publishing. Phase 4 decides where the entrance sits; it does not get a global slot |

---

## Traceability

Rows: all functional, emotional and social jobs from `jtbd.md`. Columns: the six screens plus
`Confirm the extraction`. The shared view is a **mode** of `Collection`, so it is not a column.

I read this matrix twice — once naming the job for every screen, once naming the screen for every
job — before reporting the orphans. **It has three, and that is the honest number.** A first-pass
matrix with none would have meant the ticks were placed to make it clean.

| Job \ Screen | Search | Results | Work | Collections | Collection | Publish | Confirm |
|---|---|---|---|---|---|---|---|
| **Main** — build from reasons | ✓ | ✓ | ✓ | | | | |
| **R1** — enter by the task name | ✓ | ✓ | | | | | |
| **R2** — know it is real | | ✓ | ✓ | | | | |
| **R3** — get back to it | | | ✓ | ✓ | ✓ | | |
| **R4** — shared picture with the client | | | | ✓ | ✓ | | |
| **R5** — defend a decision fast | | | ✓ | | | | |
| **E1** — the time bought something | ✓ | ✓ | | | | | |
| **E2** — the eye grows | | | | ✓ | ✓ | | |
| **E3** — stay oriented | ✓ | ✓ | | | | | |
| **S1** — read as grounded | | | ✓ | | | | |
| **S3** — collect alongside peers | | | | | | | |

**Hypothesis jobs, shown separately** — they are the *only* thing covering the last two columns:

| Job \ Screen | Search | Results | Work | Collections | Collection | Publish | Confirm |
|---|---|---|---|---|---|---|---|
| **HJ1** — proof of craft that survives inspection | | | ✓ | | | ✓ | ✓ |
| **HJ2** — the case page falls out of describing once | | | ✓ | | | ✓ | ✓ |

**ORPHAN SCREENS** — columns with no `✓` from an evidenced job.

| Screen | Why does it exist? | Resolution |
|---|---|---|
| **Publish** | The brief's success criterion 3 — "the publish + deconstruct flow completes end to end without abandonment". No evidenced job reaches it: its only rows are **HJ1 and HJ2, both hypotheses** | **Keep, with the weakness recorded.** A pool with no way in is not a product, and the brief demands the screen. But it is the first thing that changes if HJ1 fails, and it is the reason the supply risk is the project's main risk |
| **Confirm the extraction** | Same criterion, same two hypothesis rows | **Keep, same reasoning.** It also carries the `confirmed / unconfirmed` state that R2 reads on `Results` — so it produces a signal an evidenced job consumes, even though no evidenced job visits it |

**ORPHAN JOBS** — rows with no `✓`.

| Job | Where is the person supposed to do this? | Resolution |
|---|---|---|
| **S3** — collect alongside peers (P2 only) | **Nowhere.** There is no shared or multi-author collection in this structure | **Deliberately unserved, recorded not hidden.** S3 belongs to P2, the persona this product is explicitly not built for, and it is the only mention of collaboration in the whole transcript `[INT · Валя · B2 Q5]`. Serving it would mean multi-author collections — new scope for a non-target persona. **To the backlog when one exists; until then this row is the record** |

**Two `✓` worth defending, because they look generous:**

- **R3 → `Work`.** Returning to something means arriving *at the work*, not at a list. The job is
  not closed until the person is looking at the thing again.
- **E3 → `Search`.** "Stay oriented" is served by the task-named entry bounding the session — the
  brief's refusal of a feed is what closes this job, and `Search` is where that refusal lives.

**Not the target.** Two orphan screens and one orphan job remain, each with a stated reason. The
target of "no empty row and no empty column" is **not met**, deliberately: closing the Publish
columns would mean inventing an evidenced job that does not exist, and closing S3 would mean
building for the wrong persona.
