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

**Spine.** The unit of content is *work + author's breakdown*: structured fields (colour,
typography, grid) + a free-text "why" + a reality status linking to the live product. The author
fills it in **by hand — no auto-extraction anywhere.** Because the breakdown travels with the
work, **property search is free** and tagging is not required; tags are optional personal context
inside your own collections. **Progressive completeness** — publish with a minimum, the breakdown
grows, completeness is visible on the card and is an axis of filtering and ranking, and `[?]` is a
first-class UI state. Social layer: save to a collection, like, follow an author.

**Platform.** Roles split, not scaled. **Desktop primary** (~1440px): search, breakdown, upload.
**Mobile**: browsing and saving to a collection, nothing else. This inverts the pipeline's
mobile-first default deliberately — phase 8 is a decision about refusals, not about squeezing.

**Constraints.** A **pipeline exercise**: the deliverable is a full phase 0–10 run and a credible
static front-end. No backend, auth, real upload or persistence — every flow runs on fixtures.
Toolbox fallbacks bind. Artifacts are English, the working conversation Ukrainian, and **the
product's own UI language is undecided — phase 5 `/dsf:voice` owns it**, so phase 4 uses grey
placeholder text and fixes no tone.

**Out of scope.** Not a private archive. Not AI or auto-extraction in place of the author. Not a
token collector or house-style exporter. Not an infinite feed as the main screen. Not curation —
authors publish only their own work.

**Success criteria** — observable:

1. **Reproducibility.** From the breakdown screen alone, a designer states the exact palette, type
   scale and grid values and rebuilds the component without an eyedropper. Checked per screen.
2. **Trust without a click.** Any card in the results shows reality status and breakdown
   completeness without being opened.
3. **Upload does not deter.** The "publish + deconstruct" flow completes end to end on the
   prototype without abandonment, and every required field has a justification.

**Open questions `[?]`**

- `[?]` **Supplier motivation — the main risk.** Why a designer deconstructs their own work for
  free. *Hypothesis:* reputation — a breakdown is stronger proof of craft than a shot. There is
  **no interview evidence**; phase 2 looks for designers writing process breakdowns for free
  elsewhere. If it does not hold, the spine needs rebuilding.
- `[?]` **The retrieval mechanism.** Candidates: filters over the breakdown, optional tags, AI
  search. Decided in phase 3.
- `[?]` **Comparison — pain and feature, both unproven.** "Can't compare ten examples of one
  component" was demoted from the confirmed problems, and the side-by-side view from the spine.
  *Hypothesis:* shared fields deliver comparison as a side effect and no dedicated screen is
  needed. Phase 2 confirms or restores it. Consequence: the structured-fields decision now rests
  on the index alone.
- `[?]` **Is "grid" the right third axis?** *Hypothesis:* weaker than colour and typography;
  density or composition may be what designers actually reach for. Phase 2.
- `[?]` **Where the fixture imagery comes from.** Unsplash is photography and this product's
  content is interfaces. *Hypothesis:* the project's own Playwright screenshots of real products,
  each carrying source URL and capture date the way `concept/references.md` does, with Unsplash
  reserved for non-reference imagery. Phase 6.
- `[?]` **Whether breakdown quality needs moderation.** Not asked. *Hypothesis:* no at this stage
  — completeness is the only visible quality signal. Phase 3.

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
only**. The breakdown is manual, structured, and **is** the search index — no auto-extraction, no
mandatory tagging; tags are optional personal context. Progressive completeness, `[?]` is a real
UI state. Desktop primary (search, breakdown, upload); mobile is browse + save only. Static
front-end on fixtures, artifacts in English, product UI language deferred to phase 5.
Main risk carried forward: supplier motivation is a `[?]` with no evidence.
Full text: **Brief** section at the top of this file.

### Research
<!-- phase 2 · chosen interaction pattern · the three MVP mechanics · benchmark dimension · top three open questions · paths to research/ -->
**Chosen interaction pattern: faceted filtering over declared breakdown fields** — the only pattern
in which the author's manual breakdown is what makes their work findable. Second choice, already
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

**Top three open questions.** (a) **Refero Styles already ships success criterion 1** — exact colour
roles, named type scale with ratio, spacing, radii — auto-generated for 2,000+ sites with a
`DESIGN.md`; Loupe's defensible field is therefore *intent*, not values. (b) Is the unit a
**component or a whole work**? The brief claims both. (c) "Own work only" — the closest analogue
(Fonts In Use) deliberately allows others' work; the restriction costs pool growth.

Also settled here: **"grid" is probably the wrong third axis** — the market's most complete spec
publishes density, base unit, max width and radii, never a column grid (H3).

Evidence: `research/research.md`, `research/research.html`, 27 captures in `research/screens/`.
Hypotheses H1–H8 are numbered in CONCLUSIONS. Note for phase 2b: the **Даня** interview
(component-name entry on Mobbin) is designer testimony with no artifact yet — record it or keep it
`[?]`.

### People
<!-- phase 2 · primary persona and why · main job in "when / I want / so that" form · top-3 MVP jobs · paths to people/ -->
`[?]`

### Structure
<!-- phase 3 · main flow · navigation model and tap depth to the main job · paths to ia/ -->
`[?]`

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
