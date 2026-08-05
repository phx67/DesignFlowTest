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
built. Loupe pairs every work with a breakdown written by the person who made it: the palette,
the type scale, the grid, and the reasoning. The breakdown is filled in by hand — there is no
auto-extraction — and because it travels with the work, it doubles as the search index: you
find things by their properties rather than by tags somebody remembered to write.

**Who it is for.** A designer with a task on the desk — a specific component to design — who
needs to see how ten other people solved it *and* how those solutions are constructed. The main
screen is search and filters, not a feed. On the other side, authors publish their own work and
deconstruct it themselves.

**Platform.** Desktop is primary: search, breakdown and upload all live there. Mobile is for
browsing and saving to a collection.

**Scope.** This repo is an exercise of the full design pipeline. The product is a credible
static front-end built on fixtures — no backend, no accounts, no real uploads.

Full brief, success criteria and the open `[?]` questions: [`CLAUDE.md`](./CLAUDE.md).

## Research

<!-- phase 2 · competitors, benchmark, patterns -->
`[?]` → `research/research.html`

## People

<!-- phase 2 · personas and jobs -->
`[?]` → `people/personas.html`

## Structure

<!-- phase 3 · sitemap, navigation, flows -->
`[?]` → `ia/ia.html`

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
