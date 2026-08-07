# Critique log

Every `/dsf:critique` run whose owning phase has no critique artifact of its own. Phase 4's
tables live in `wireframes/_critique.md`; everything else lands here. One dated section per run,
append-only. Gate answers live in `.design/decisions.md` and never here.

## 2026-08-07 · scope: `research/research.md` — the Refero record

Requested by the designer, who suspected Refero was recorded as a direct competitor while its
purpose is a different one — an AI-workflow tool for feeding templates to an agent, rather than a
human community for learning and understanding other people's decisions.

Source of truth for this scope: `research/research.md` (phase 2, not yet signed off — the fix goes
in at the source, not into the HTML render).
Quality pass: the built-in checks, **Honesty** row. `impeccable` is `active` but
`.design/memory/toolbox.md` scopes it to the quality pass of phases 4–10, and
`.design/prompts/critique.md` is a per-screen pass; phase 2 has no screens.
Positioning re-verified in Chromium at 1440×900 on 2026-08-07, not from memory:
`research/screens/refero-positioning-2026-08.png`.

**Verdict on the premise: confirmed by half, and the other half matters.** Refero's MCP proposition
is unambiguously agent-facing — "connects **your agent** to a curated library… **It studies before
it builds** — and the output looks designed, not generated" — and its `h1` is "Design Research for
the AI Era". But its `meta description` is literally "UI/UX references and **design inspiration**",
its taxonomy is built for human browsing, it ships a **Figma plugin**, designers are named **first**
in "designers, builders and AI", and its entry question "**What are you designing next?**" is the
brief's primary user restated. So "the purpose is different" is too strong as a blanket claim: the
product is **two products under one roof**, and the defect was that `research.md` did not
distinguish them.

| Where | What is wrong | How to fix | Outcome |
|---|---|---|---|
| `research.md` — Aspirational group, Refero row | The class flattens two products with different purposes and audiences: a human browse library that competes for the primary persona's attention, and a machine-facing spec + MCP server that does not | Split into two records: `Refero (browse)` stays a competitor; `Refero Styles + MCP` becomes adjacent, overlapping only on auto-extraction of values | **fixed** — option (b) chosen at the gate |
| `research.md` — comparison matrix, Refero row | Records "Designers, builders **and AI**" and "an MCP server **for coding agents**" and then draws no consequence from either anywhere in the file. Load-bearing data, unused — an Honesty defect | Split the matrix row in two and state the consequence in CONCLUSIONS | **fixed** |
| `research.md` — "This is Loupe's spine, generated automatically" | Formally true, but without the qualifier it reads as "Loupe is already built by someone else". Styles delivers values **to a machine for assembly**, not to a person for understanding | Add the purpose distinction beside the values claim | **fixed** — carried by the new "Why Refero is two rows" note |
| `research.md` — open question 1 (success criterion 1) | Asks what a hand-written breakdown buys over a generated one, without noticing the two are aimed at opposite consumers | Refine the question rather than answer it | **fixed** |
| `research.md` — CONCLUSIONS | No row carried the consumer split, so phase 3 would inherit "match the values" as the whole contest | Add a gap row: matching values is table stakes, comprehension is the contest, and the breakdown screen must not be a spec dump | **fixed** |
| `research.md` — header, "All screenshots … captured … on 2026-08-06" | Stale: three captures are from 2026-08-07 (two from the phase-2b re-research, one from this critique) | Correct the header and date the later captures where cited | **fixed** |
| `research.md` — H1 (`intent, not values`) and H3 (`third axis`) | Both rest on the *values*, which the split does not touch | Leave untouched, deliberately | **dropped by the human** — "`:280` і `:285` не чіпай" |

Propagated: `research/research.html` (both tables, the new note, the capture, open question 1, the
CONCLUSIONS row) — verified in Chromium, 15 images, 0 broken, no horizontal page scroll;
`CLAUDE.md` → Research block, because phase 3 reads it and inherits the consequence.

Nothing deferred. No "keep it" was said.
