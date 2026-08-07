# Project context

This repo is the design file. Everything about this product — brief, research, structure,
screens, voice, visual language, system, handoff — lives here as files, not in chat history.

Read this file first, then the artifacts it points to. Never re-ask what is already written.

---

## Brief

**Loupe** — a community discovery site for designers where every published work arrives with its
author's own breakdown: colour, typography, grid, and the intent behind them. You see the
solution *and* can rebuild it.

**Who it is for.** Primary: a designer with **a task on the desk** — a specific component to
design (empty state, pricing, onboarding form) — who needs to see how others solved it and how it
is built. Sessions are short and targeted, so the main screen is **search and filters, not a
feed**. Secondary: the author, who publishes their **own work** and writes its breakdown — rights
are clean, the analysis is authentic, and the pool grows only as fast as people make things. Not
for private-archive hoarders, teams assembling a house style, or undirected browsing.

**Problem.** Inspiration sites show the result and say nothing about the construction. Three
confirmed failures: **can't reproduce it** — the system is invisible, so scale and grid get
guessed by eye; **can't see the why** — without the author's intent the form gets copied into a
context where it does not work; **don't believe it's real** — no signal whether it shipped or is
a concept. Source: the designer's own testimony at the phase-1 gate; phase 2 tests it against
other people.

**Spine.** The unit of content is *work + breakdown*: structured fields (colour, typography,
grid) + intent + a reality status linking to the live product. **The unit is polymorphic — one
screen or a whole case, both first-class.** **The machine extracts the objective fields; the
author confirms or corrects them** — the author's work is verification plus intent, never
transcription, and **intent is never generated**. The breakdown travels with the work, so
**property search is free**; tags are optional personal context inside your own collections.
**Completeness is measured on intent alone** — *absent → present → case* — and that is the axis of
filtering and ranking; the extracted fields carry a **confirmed / unconfirmed** trust state
instead. `[?]` is a first-class UI state. Social layer: save to a collection, like, follow an
author.

**Platform.** Roles split, not scaled. **Desktop primary** (~1440px): authoring — the breakdown,
upload — and heavy side-by-side facet comparison. **Mobile**: search, open a work, read its
breakdown, save to a collection — search is on the phone deliberately, because the primary persona
rejected a tool for lacking exactly that (`people/personas.md`). Whether the phone also needs the
**full facet filter** is `[?]` for phase 8. This inverts the pipeline's mobile-first default
deliberately: phase 8 decides refusals, not squeezing.

**Constraints.** A **pipeline exercise**: the deliverable is a full phase 0–10 run and a credible
static front-end. No backend, auth, real upload or persistence — every flow runs on fixtures, which
makes extraction a simulated step. Toolbox fallbacks bind. Artifacts are English, the working
conversation Ukrainian, and **the product's own UI language is undecided — phase 5 `/dsf:voice`
owns it**.

**Out of scope.** Not a private archive. **Not AI speaking in place of the author** — extraction
drafts the objective fields, the author confirms, intent is never generated. Not a token collector
or house-style exporter. Not an infinite feed as the main screen. Not curation — authors publish
only their own work.

**Success criteria** — observable:

1. **Reproducibility.** From the breakdown screen alone, a designer states the exact palette, type
   scale and grid values and rebuilds the component without an eyedropper. Checked per screen.
2. **Trust without a click.** Any card in the results shows reality status, the **confirmed /
   unconfirmed** state of the extracted fields, and how far intent has got — without being opened.
3. **Upload does not deter.** The "publish + deconstruct" flow completes end to end on the
   prototype without abandonment, and every required field has a justification.

**Open questions `[?]`**

- `[?]` **Supplier motivation — the main risk.** Why a designer writes **intent** for free.
  Extraction covers everything else, so the risk sits **entirely on intent**. *Hypothesis:*
  reputation — a stated reason is stronger proof of craft than a shot. Phase 2 found adjacent
  evidence but **no designer testimony about writing a breakdown**. If it fails, the spine needs
  rebuilding.
- `[?]` **What "confirmed" is worth.** Nothing says a reader believes a confirmation, or that an
  author corrects a wrong extraction rather than waving it through. *Hypothesis:* confirmation is
  cheap and therefore weak unless a wrong value is visibly costly. Phase 3 owns the state.
- `[?]` **Whether breakdown quality needs moderation.** Not asked. *Hypothesis:* no at this stage
  — but Fonts In Use, the closest analogue, **does** moderate before publication. Phase 3.
- `[?]` **Where the fixture imagery comes from.** Unsplash is photography and this product's
  content is interfaces. *Hypothesis:* the project's own Playwright screenshots of real products,
  each carrying source URL and capture date the way `concept/references.md` does, with Unsplash
  reserved for non-reference imagery. Phase 6.

**Closed by phase 2** — full reasoning in `research/research.md` and `.design/decisions.md`: the
**retrieval mechanism** is faceted filtering over the declared fields; **comparison** stays demoted
and the dedicated screen is cut; the **third axis** is not a column grid and is renamed to base
unit / density / spacing in phase 3; the **content unit** is both a screen and a case.

**Change history is not kept here.** Every superseded line, its date and its reason live in
`.design/decisions.md`.
---

## First contact

If this looks like a fresh clone (toolbox rows still `[?]`, no `phase-0` ledger), your FIRST
message to the designer must, before anything else:

1. Hand them the project home page: the absolute local path to `index.html` (and, once
   hosting is active, its URL) with one sentence on how to open it in a browser.
2. Say what the page is: the state view of the pipeline — the phase you are in, derived from
   artifacts on disk plus `/dsf:check` verdicts plus tags, with every prompt to send and the
   done-criteria each phase is verified against.
3. Name the first move: open the page, read "How this works", then type `/dsf:init`.

The page tracks state; the chat executes. Neither one guesses the other's job.

---

## Rules of engagement

- **Constitution:** `.design/memory/constitution.md` — the binding rules for every
  `/dsf:*` command. Read it before acting.
- **Phases:** `.design/memory/phases.md` — the canonical phase table: commands, checklists,
  tags, canonical artifact paths, the done/in-progress/locked definitions, and the
  `index.html` data contract. When a command and that file disagree, that file wins.
- **Progress:** `.design/progress/phase-N.md` — the append-only step ledger. Every command
  appends one line the moment a numbered step or a gate finishes, reads its ledger before a
  re-run, and never runs work that belongs to a later phase without stopping first (constitution
  rule 13, the phase-order guard).
- **Toolbox:** `.design/memory/toolbox.md` — which tools this project has, which fallback to
  use when one is missing, and the only three status values (`active` / `fallback` / `[?]`).
  Read it before using any tool.
- **Fallback prompts:** `.design/prompts/` — `critique.md`, `audit.md`, `document.md`,
  `extract.md`, `brief-interrogation.md`. These run whenever the matching toolbox row is not
  `active`.
- **Checklists:** `.design/checklists/phase-N-*.md` — read-only done-criteria. Nobody ticks
  them; `/dsf:check` verifies them against the files and writes the verdict to
  `.design/checklists/results/phase-N.md`.
- **Decisions:** every gate answer, "keep it" and contradiction resolution is recorded in
  `.design/decisions.md`; changes after sign-off go through `/dsf:change`.
- **Dashboard:** `index.html` — current status, artifacts and links. **The project home page
  is `index.html` — keep its data block current.**

---

## Toolbox

<!-- /dsf:init fills this in: one line per active tool and one per fallback in force -->

Resolved 2026-08-04. Full evidence, install details and switch-on instructions are in
`.design/memory/toolbox.md` — read that before using any tool; these lines are the summary.

- **Browser & screenshots — `active`.** Playwright MCP (`playwright` in `.mcp.json`), Chromium
  verified rendering. Take your own screenshots; never describe a screen from memory. The
  browser needs the `LD_LIBRARY_PATH` pinned in `.mcp.json` — do not drop it. The server goes
  live on a new session, so confirm the tools exist before relying on them.
- **Visual references — `fallback`.** No Refero. Build `concept/references.md` from web search
  plus your own screenshots; label every row `[web]` with its source URL and capture date.
- **Design quality laws — `active`.** `impeccable` v4.0.4 — use `/impeccable critique` and
  `/impeccable audit` for the quality pass in phases 4–10, instead of `.design/prompts/`.
- **Structured brief — `active`.** `superpowers` v6.2.0 — `/dsf:brief` runs its `brainstorming`
  skill instead of `.design/prompts/brief-interrogation.md`.
- **Imagery — `fallback`.** No Gemini key. Source images from Unsplash by content theme, one
  locked colorway, and record query + URL + photographer in `visuals/README.md`.
- **Icons — `active`.** **Solar, linear**, one style throughout. Locked — mixing sets or weights
  is a defect, not a variation. Downloaded into the repo when `/dsf:build` first needs them.
- **Hosting — `active`.** GitHub Pages at **https://phx67.github.io/DesignFlowTest/**, public,
  `main` root. `gh` is at `~/.local/bin/gh` (on PATH in new sessions only). **`Bash(curl:*)` is
  denied by `.claude/settings.json` — use `wget`.**

---

## Pipeline

Eleven phases (0–10) and seventeen commands, driven by `/dsf:*`. Each phase reads the previous
phases' artifacts, produces a Markdown artifact for the agent plus an HTML page for humans,
ends with a critique cycle and a human gate, updates the living docs, and commits.

| Phase | Command(s) | Output lives in | Tag |
|---|---|---|---|
| 0 · Init | `/dsf:init` | `.design/memory/toolbox.md`, `index.html` | `phase-0-init` |
| 1 · Brief | `/dsf:brief` | this file, `README.md`, folder scaffolding | `phase-1-brief` |
| 2 · Discover | `/dsf:research` + `/dsf:users` | `research/`, `people/` | `phase-2-discover` |
| 3 · Structure | `/dsf:ia` | `ia/` | `phase-3-ia` |
| 4 · Wireframes | `/dsf:wireframes` | `wireframes/` | `phase-4-wireframes` |
| 5 · Language | `/dsf:voice` + `/dsf:concept` | `voice/`, `concept/` | `phase-5-language` |
| 6 · Build | `/dsf:build` | `DESIGN.md`, `design-system/`, `ui/`, `visuals/` | `phase-6-build` |
| 7 · System | `/dsf:system` | `design-system/` — `docs/`, `patterns/`, `examples/` | `phase-7-system` |
| 8 · Responsive | `/dsf:responsive` | `responsive/`, breakpoint + grid tokens, the shell, `split-view` | `phase-8-responsive` |
| 9 · Motion | `/dsf:motion` | `animations/`, motion tokens, the components | `phase-9-motion` |
| 10 · Handoff | `/dsf:handoff` | `handoff/`, release | `phase-10-handoff` |

Cross-cutting, usable at any point: `/dsf:status` (where am I, what to type next),
`/dsf:critique` (defect table on any scope), `/dsf:check` (verify a phase against its
checklist and sign it off), `/dsf:change` (a request that invalidates signed-off work —
blast radius, re-opened phases, logged decision).

**Tags.** Exactly one tag per phase, as listed above — phases 2 and 5 have two commands and
still get one tag, created once both are done. Tags are created **only** by `/dsf:check`, on a
full pass, after the human confirms. Phase commands never tag. Phase 10 also carries the release
tag `v1.0`. A tag is the result of the gate, never a criterion inside it.

---

## Context blocks

Each phase appends its block below and keeps it current. A block is short — the facts later
phases need, plus paths. Not a retelling of the artifact.

### Brief
<!-- phase 1 · what the product is, who it is for, platform, constraints, success criteria -->
Loupe — a community discovery site for designers; every published work carries its author's own
breakdown (colour, typography, grid, intent). Primary user: a designer with a specific component
to design; the main screen is search + filters, not a feed. Authors publish **their own work
only**, and the unit is **one screen or a whole case, both first-class**. The breakdown is
structured and **is** the search index; **the machine extracts the objective fields and the author
confirms or corrects them** (changed 2026-08-07), with no mandatory tagging — tags are optional
personal context. **Completeness is measured on intent alone** (absent → present → case); the
objective fields carry a **confirmed / unconfirmed** trust state instead. `[?]` is a real UI state. Desktop primary (authoring, upload, heavy facet comparison); mobile does search, read a
breakdown and save — full facet filtering on the phone is `[?]` for phase 8. Static
front-end on fixtures, artifacts in English, product UI language deferred to phase 5.
Main risk carried forward: supplier motivation is a `[?]` with no evidence.
Full text: **Brief** section at the top of this file.

### Research
<!-- phase 2 · chosen interaction pattern · the three MVP mechanics · benchmark dimension · top three open questions · paths to research/ -->
**Chosen interaction pattern: faceted filtering over declared breakdown fields** — the only pattern
in which the breakdown travelling with the work is what makes it findable. *(2026-08-07: this
argument was originally "the author's **manual** breakdown". It survives the move to extraction
unchanged — the fields are still declared and still carried by the work; what changed is who drafts
them, not what retrieval acts on.)* Second choice, already
half-confirmed: task-taxonomy browse as the entry with facets refining inside it, on the Mobbin
model. AI free-text query is **disqualified at this size** (fixtures, few dozen items) because it
severs "fill a field → be found".

**Benchmark dimension:** how a product obtains unpaid structured work and holds quality without a
paid moderation team. Scored across categories: Discogs 29 · Genius 28 · Stack Overflow 27 ·
Wikipedia 26 · Letterboxd 24.

**Three mechanics for the MVP.** (1) The breakdown is the price of something the author wanted
anyway — filling it produces their own case-study page (Discogs: you cannot list a record without
the fields). (2) `[?]` is a dated, actionable marker carrying the control that fills it, not an
empty cell (Wikipedia's banner). (3) The right to mark quality is earned by contributing — the
answer to the moderation `[?]`: not staff, not nothing.

**Refero is two products, split 2026-08-07.** **Refero (browse)** — taxonomy, Figma plugin, "design
inspiration", "What are you designing next?" — is a **direct competitor** for the primary persona's
attention. **Refero Styles + MCP** is **adjacent**: it exists so an *agent* can build from the spec
("connects your agent… **it studies before it builds** — the output looks designed, not generated"),
overlapping with Loupe only on the auto-extraction of values. **Consequence phase 3 must honour:
matching the values is table stakes, not the contest — the contest is comprehension, so the
breakdown screen must not be designed as a spec dump.** Evidence:
`research/screens/refero-positioning-2026-08.png`; `.design/critique-log.md`.

**Top three open questions.** (a) **Refero Styles already ships success criterion 1** — exact colour
roles, named type scale with ratio, spacing, radii — auto-generated for 2,000+ sites with a
`DESIGN.md`; Loupe's defensible field is therefore *intent*, not values. **Refined by the split
above: it ships that criterion for a machine, Loupe ships it for a person.** (b) ~~Is the unit a
component or a whole work?~~ **Closed 2026-08-07 by `/dsf:change`: both. One screen or a whole
case, each first-class.** The research had recommended phase 3 pick one; the designer overrode
that deliberately. (c) "Own work only" — the closest analogue
(Fonts In Use) deliberately allows others' work; the restriction costs pool growth.

Also settled here: **"grid" is probably the wrong third axis** — the market's most complete spec
publishes density, base unit, max width and radii, never a column grid (H3).

Evidence: `research/research.md`, `research/research.html`, 27 captures in `research/screens/`.
Hypotheses H1–H8 are numbered in CONCLUSIONS. Note for phase 2b: the **Даня** interview
(component-name entry on Mobbin) is designer testimony with no artifact yet — record it or keep it
`[?]`.

### People
<!-- phase 2 · primary persona and why · main job in "when / I want / so that" form · top-3 MVP jobs · paths to people/ -->
**Primary persona — «Той, хто перевіряє, чи це взагалі можна побудувати»** (Даня, `[INT]`). Mid
UI/UX designer in a small outsourcing studio. Enters by the **name of a component**, not by a
property («екран реєстрації», «кошик») — this confirms `[RES]` **H7**. Trusts only screenshots of
shipped products and rejects «dribbble-дизайн… гарне, але пусте всередині». Loses his own saves
constantly: «90% моїх збережень це мертвий груз». Secondary: **Валя**, who has **none** of the
brief's problems and is kept as the user this product would fail to attract; **the author**, who is
**entirely `[?]`** — the interview never asks about publishing, so the supply side has no evidenced
job at all. That is the project's main risk, unchanged.

**Main job.** *When I have a specific component to design and no confidence that my own guess at how
to build it is right, I want to see how people who already solved that same thing made their
decisions and why, so that I can build my own version from reasons instead of from eyeballing a
picture.*

**MVP core — three jobs** (signed off 2026-08-07): **(1) Main** — build from reasons, not by eye;
the market already generates the *values*, so what enters the core is the **intent**. **(2) R2** —
know a work is real before opening it. **(3) R3** — return to what you already found without a hunt.

**Binding constraints from the gate.** Intent is a **value and a job, never a mandatory field** —
carried through the work's own case material, easy/optional/progressive, **no compulsory "justify
it" form anywhere**; its form and weight are `[?]` for **phase 3**. **Cut from the MVP:** likes and
follow-an-author (deliberately, to v2), the column grid as the third axis, a dedicated side-by-side
comparison screen, tags as a retrieval mechanism.

**Three `[?]` phase 3 inherits.** (a) The **form and weight of intent**. (b) The **third breakdown
axis must be re-named** — base unit / density / spacing, not a column grid (also phase 6, tokens).
(c) **Client alignment (R4)** — the best-evidenced job in the whole set and **absent from the
brief**; the IA checks whether "a collection you can show a non-designer" falls out of existing
collections almost for free.

**Also found in re-research:** **Fonts In Use moderates before publication** ("Submit for approval",
"Status: private draft (awaiting moderation)") — the closest analogue does **not** hold quality
without a moderator, which phase 3 must answer against `[RES]` **H5**.

Evidence: `people/personas.md`, `people/jtbd.md`, `people/personas.html`; primary source
`sources/Interview Script 30e58b052da9800b8138cae64003069a.html`, **n = 2**.

### Structure
<!-- phase 3 · main flow · navigation model and tap depth to the main job · paths to ia/ -->
**Six screens:** `Search` → `Results` → `Work` · `Collections` → `Collection` · `Publish` →
`Confirm the extraction`. **`Work` carries the breakdown itself** — one screen, not two, because the
breakdown travels with the work.

**Global navigation — three items:** **Search** (Main, R1, E1, E3), **Collections** (R3, E2, R4),
**Publish** (HJ1, HJ2). Rejected on purpose: author profile, a following feed, a separate Tasks
entrance, notifications.

**Tap depth: 2 of a 3-tap budget** to the main job — `Search` → `Results` → `Work`. The spare tap is
reserved for whatever `Work` cannot hold at once, most likely the case narrative. **Later phases are
held to this number.**

**Main flow:** arrive with a component due → name the task (or query the declared fields) → `Results`
→ `Work` → read the values, confirmed or not → read intent → rebuild → optionally save. Four flows
in total (Main, R3, R4, HJ1), all rendered by Mermaid without error.

**Decisions this phase made that later phases inherit:**

- **Intent is an annotation anchored to the work's material** — point at a region, say why.
  Progression *absent → present → case*. **Never a form.** This closes the `[?]` phase 2 handed over.
- **R4 is served by a shared *mode* of `Collection`**, not a new screen — the best-evidenced job in
  the set costs no new scope.
- **`Author` is a byline on `Work`, not a screen.** Follow stays cut to v2.
- **No curation object. `[RES]` H5 is UNCONFIRMED in this version** — quality is carried by
  completeness on intent plus the confirmed / unconfirmed state of the extracted values.
- **`Task` and `Facet value` render inside `Search` and `Results`** and are never addressed as
  screens.

**Three orphans left standing, each with a reason:** `Publish` and `Confirm the extraction` are
reached by **hypothesis jobs only** (HJ1, HJ2) and exist on the brief's criterion 3 — the weakest
joint in the structure, and the first thing to change if HJ1 fails. **S3** (collect alongside peers)
is deliberately unserved: P2-only.

Evidence: `ia/sitemap.md`, `ia/flows.md`, `ia/ia.html`.

### Wireframes
<!-- phase 4 · where the screens live, naming convention, state pages, the navigator panel -->
`[?]`

### Voice
<!-- phase 5 · pointer to voice/voice.md principles and voice/microcopy.md as the single copy source -->
`[?]`

### Concept
<!-- phase 5 · chosen direction and why · recorded taste and anti-references · icon set · image source -->
`[?]`

### Build
<!-- phase 6 · token levels, where components live, the shell, the kit showcase, visuals colorway -->
`[?]`

### System
<!-- phase 7 · contribution rules, showcase location and URL, patterns, backlog -->
`[?]`

### Responsive
<!-- phase 8 · the two breakpoints and the behavior that set them, the grid tokens, the split-view pattern -->
`[?]`

### Motion
<!-- phase 9 · motion tokens and their roles, the three jobs, where micro-interactions live, reduced-motion -->
`[?]`

### Handoff
<!-- phase 10 · pointer to handoff/, the map, the a11y checklist, release tag and live URLs -->
`[?]`

---

## The "keep it" rule

When the human says **"keep it"** about an experiment, it stops being an experiment and
becomes a rule. Write the rule down here, and route the change to wherever the truth
currently lives. The destination escalates as the project matures — update this section at
the end of every phase that moves it.

**Current destination for a change:** the screen file itself.

<!-- Phase 4: the screen, plus wireframes/_conventions.md if it is a rule for all screens -->
<!-- Phase 5: voice/voice.md + voice/microcopy.md for copy; concept/concept.md for visual decisions -->
<!-- Phase 6: the kit component or the token — never the screen -->
<!-- Phase 7: design-system/ (component, pattern or token) first, then the screens -->
<!-- Phase 8: the responsive behavior lives in components and the shell -->
<!-- Phase 9: motion lives in components, never in a screen -->

**Kept rules**

- `[?]`
