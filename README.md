# Loupe

A community discovery site for designers, where every published work arrives with its author's
own breakdown — colour, typography, grid and the intent behind them — so a solution can be
rebuilt, not just admired.

This repo **is** the design file. Research, structure, screens, copy, visual language, the
design system and the handoff all live here as files. No Figma required.

**→ [Open the pipeline page](./index.html)** — this is your home: current phase, every
step and prompt to type, success criteria, and links to every viewable page. Also live at
**https://phx67.github.io/DesignFlowTest/**.

**Current phase: 1 · Brief** — the brief is written; run `/dsf:check` to sign it off, then
`/dsf:research`.

Built with [design-spec-framework](https://github.com/denysosadchyi/design-spec-framework) —
spec-driven development for product design. Work is driven by `/dsf:*` commands in Claude
Code; the rules live in `.design/memory/constitution.md`.

---

## Brief

<!-- phase 1 -->

**What it is.** Inspiration sites show a finished result and say nothing about how it was
built. Loupe pairs every work with a breakdown: the palette, the type scale, the grid — and the
reasoning behind them. **The machine extracts the measurable parts; the author confirms them and
supplies the one part no machine can, the intent.** Because the breakdown travels with the work,
it doubles as the search index: you find things by their properties rather than by tags somebody
remembered to write. A work can be **a single screen or a whole case** — both are first-class.

**Who it is for.** A designer with a task on the desk — a specific component to design — who
needs to see how ten other people solved it *and* how those solutions are constructed. The main
screen is search and filters, not a feed. On the other side, authors publish their own work and
explain it themselves.

**Platform.** Desktop is primary: writing a breakdown, uploading, and comparing works side by
side all live there. The phone searches, opens a work, reads its breakdown and saves it — because
the primary persona rejected a tool for not letting him search on the move.

**Scope.** This repo is an exercise of the full design pipeline. The product is a credible
static front-end built on fixtures — no backend, no accounts, no real uploads.

Full brief, success criteria and the open `[?]` questions: [`CLAUDE.md`](./CLAUDE.md).

## Research

<!-- phase 2 · competitors, benchmark, patterns -->

Twelve competitors in three groups, a comparison matrix built from screenshots taken for this
phase, a cross-category benchmark on **how a product gets unpaid structured work and holds its
quality without moderators**, and five retrieval patterns with one chosen: **faceted filtering over
the declared breakdown fields**.

The finding that reframed the project: a competitor already generates Loupe's construction spec
automatically for 2,000+ sites, so the defensible field is the author's *intent*, not the values.

- [`research/research.md`](./research/research.md) — the source of record, four sections, every
  claim sourced or marked `unverified`
- [`research/research.html`](./research/research.html) — the same, as a page you can hand to
  someone
- `research/screens/` — 38 captures, **33 of them referenced by filename** from `research.md`
  (2 added by the targeted re-research in phase 2b); the rest are working captures left from
  earlier verification passes

## People

<!-- phase 2 · personas and jobs -->

Three personas built from a two-respondent interview, one marked primary: **a mid UI/UX designer
who arrives with a named component to build**, trusts only work that shipped, and cannot re-find his
own saves. The second persona has none of those problems and is kept on purpose — she is the user
this product would fail to attract. **The third, the author who deconstructs their own work, is
entirely `[?]`**: the interview never asked about publishing, so the supply side of the product has
no evidence behind it at all. That is the project's main risk, and the file says so rather than
covering it.

The jobs, the coverage matrix and the three MVP jobs follow from the same evidence, and so does the
cut list — including the features the brief assumed and the matrix could not justify.

- [`people/personas.md`](./people/personas.md) — personas, the honesty audit, and what we still do
  not know about people
- [`people/jtbd.md`](./people/jtbd.md) — jobs in "when / I want / so that" form, the jobs × personas
  × features matrix, the MVP core and the cuts
- [`people/personas.html`](./people/personas.html) — the same, as a page you can hand to someone

## Structure

<!-- phase 3 · sitemap, navigation, flows -->

Six screens, three global navigation items, and the main job reachable in **two taps of a
three-tap budget**. Every screen is annotated with the job it serves, and the three that are not —
two screens reached only by hypotheses, one job left deliberately unserved — are listed as orphans
rather than quietly tidied away.

The structural decisions phase 3 made: intent is an **annotation on the work's own material**, not
a form; the client-facing view is a **mode** of a collection rather than a new screen; the author is
a byline, not a destination.

- [`ia/sitemap.md`](./ia/sitemap.md) — entities, the screen tree, navigation and the tap budget,
  and the jobs × screens coverage matrix
- [`ia/flows.md`](./ia/flows.md) — four Mermaid flows with their decisions, states and both endings
- [`ia/ia.html`](./ia/ia.html) — the same, as a page you can hand to someone

## Wireframes

<!-- phase 4 · grey screens with all states -->
`[?]` → `wireframes/index.html`

## Voice

<!-- phase 5 · voice principles and the copy source of truth -->
`[?]` → `voice/voice.html`, `voice/microcopy.md`

## Concept

<!-- phase 5 · chosen visual direction -->
`[?]` → `concept/directions.html`, `concept/concept.html`

## UI

<!-- phase 6 · token audit, tokens, components, kit showcase -->
`[?]` → `ui/kit.html`, `ui/tokens-audit.md`

## Design system

<!-- phase 7 · the system as a product, with live docs -->
`[?]` → `design-system/docs/index.html`

## Responsive

<!-- phase 8 · behavior-based breakpoints, adaptive shell and components, split-view -->
`[?]` → `responsive/width-audit.html`

## Motion

<!-- phase 9 · motion tokens, the three jobs, reduced-motion -->
`[?]` → `animations/motion-inventory.html`

## Handoff

<!-- phase 10 · spec, map, a11y, release -->
`[?]` → `handoff/index.html`

---

## Repo map

| Path | What lives there |
|---|---|
| `.design/` | Constitution, phase table, toolbox, fallback prompts, artifact templates, phase checklists, `checklists/results/` (the `/dsf:check` verdicts), `progress/` (the append-only step ledgers), decision log |
| `.claude/commands/dsf/` | The `/dsf:*` commands |
| `CLAUDE.md` | Agent context — brief plus a block per phase |
| `index.html` | The project's home page — phases, artifacts, links, status |
| `research/` · `people/` | Phase 2 |
| `ia/` | Phase 3 |
| `wireframes/` | Phase 4 — the screens, layered by every later phase |
| `voice/` · `concept/` | Phase 5 |
| `ui/` · `design-system/` · `visuals/` | Phases 6–7 |
| `responsive/` | Phase 8 |
| `animations/` | Phase 9 |
| `handoff/` | Phase 10 |
