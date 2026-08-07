# Phase 2 — Discover · check results

Checked: 2026-08-07 · Checklist: `.design/checklists/phase-2-discover.md`
Result: **pass** — 25 pass · 0 fail · 0 human · 25 of 25 items

Both sub-commands have run: `/dsf:research` (steps `research.1`–`research.9`, commit `8a00b3f`)
and `/dsf:users` (steps `users.1`–`users.9`, commits `2bb4e5d`, `8917b36`), plus one `/dsf:critique`
pass on the Refero record (`77b9a45`). Browser items were verified with Playwright MCP, which
`.design/memory/toolbox.md` records as `active`; none had to be deferred to the human.

| # | Item | Verdict | Evidence |
|---|---|---|---|
| 1 | Competitors in three groups, ≥5 products named | pass | `research/research.md:26` Hard · `:36` Soft · `:45` Aspirational; 12 products named across them plus a language reference |
| 2 | Comparison matrix, cells from collected data | pass | `research/research.md:53–67` — products as rows, six dimensions as columns, every cell carrying a screenshot path, a link, or `[?] unverified` |
| 3 | Benchmark: 6–8 criteria, 4–5 products, each scored | pass | `research/research.md` — 7 criteria rows under **Criteria**, 5 products scored under **Scoring** (Discogs 29 · Genius 28 · Stack Overflow 27 · Wikipedia 26 · Letterboxd 24) |
| 4 | Five different UX patterns, one chosen and argued | pass | `research/research.md:230+` — patterns 1–5 differing by mechanism; pattern 1 chosen with three reasons grounded in `CLAUDE.md`; pattern 3 disqualified with reasons |
| 5 | Hypotheses listed and numbered | pass | `research/research.md` CONCLUSIONS — **H1–H8**, 8 numbered items |
| 6 | `research/screens/` holds screenshots referenced by filename | pass | 38 captures present, **33 referenced by filename** from `research.md`. Note, not a failure: 4 `_verify-*` working captures from earlier verification passes sit in the folder and belong in `.playwright-mcp/`; `figma-community-design-systems.png` is unreferenced |
| 7 | Every fact carries a link, a screenshot path, or "unverified" | pass | `research/research.md` **Sourcing pass** — 11 occurrences of `unverified`, each naming what was not collected; the pass explicitly lists what remains unsourced |
| 8 | `research/research.html` opens standalone and links its screenshots | pass | Opened in Chromium at `http://127.0.0.1:8733` — 15 images, **0 broken**, no horizontal page scroll; only console entry is the local server's `/favicon.ico` 404 |
| 9 | `people/personas.md` holds 2–4 behavior-based personas | pass | `people/personas.md` — 3 personas, split by jobs and pains; the **Merged personas** section states the merge test and its result |
| 10 | Exactly one primary, with a stated reason | pass | `people/personas.md:38` — Persona 1 marked **PRIMARY**, reason given; Personas 2 and 3 marked secondary |
| 11 | Every persona block points at a place in the evidence or carries `[?]` | pass | 15 block headings (3 personas × context / jobs / pains / trust / quote), each carrying an `[INT · … ]` or `[RES · … ]` citation or an explicit `[?]` with a hypothesis |
| 12 | One main job + 3–5 related, "when / I want / so that", none named after a feature | pass | `people/jtbd.md:17` main job · `:44` 5 related jobs (R1–R5). All 11 "I want" clauses inspected: none contains a feature name |
| 13 | Emotional and social jobs listed separately | pass | `people/jtbd.md:59` **Emotional jobs** (E1–E3) · `:69` **Social jobs** (S1–S3), both separate from the functional tables |
| 14 | Each job records where it came from | pass | Every row of every job table carries a Source column with an `[INT]` or `[RES]` citation; the Hypotheses table instead carries "what would confirm it" and "where to look" |
| 15 | Jobs × personas × features matrix with a competitors column | pass | `people/jtbd.md:104` — columns P1 · P2 · P3 · FEATURE · **COMPETITORS — already closed?** |
| 16 | Matrix ends in three MVP-core jobs and named cut candidates | pass | `people/jtbd.md:124` **MVP core — three jobs** (Main, R2, R3) · `:148` **Cut candidates**, 5 rows |
| 17 | A confirmed / hypothesis / invented audit is recorded | pass | `people/personas.md:230` **Self-critique** — 23 statements classified; 2 found **invented** |
| 18 | Claims that drive design but rest on `[?]` are called out | pass | `people/personas.md:266` **The dangerous subset** — 5 items, ordered by what it would cost to be wrong |
| 19 | At least one gap closed by targeted follow-up, visible in `research.md` | pass | `research/research.md:384` **Re-research after personas** — Q1 and Q3 produced findings, Q3 closed dangerous item 5 (Eagle, previously absent from the competitor set); Q2 recorded as an explicit null result rather than filled |
| 20 | `[?]` marks survive into `people/personas.html` | pass | Chromium: `document.querySelectorAll('.q').length` → **45** rendered `[?]` marks, including a whole persona card styled as unevidenced |
| 21 | `people/personas.html` opens standalone in a browser | pass | Opened in Chromium at `http://127.0.0.1:8732` — 3 persona cards with the primary marked, 8 tables, no horizontal page scroll (1425/1425); no external resources, so nothing to fail offline |
| 22 | `CLAUDE.md` → People block names the primary persona and the main job | pass | `CLAUDE.md` → Context blocks → **People** — primary persona named with its behaviour, main job in full "when / I want / so that" form, plus the three MVP jobs |
| 23 | `README.md` Research and People sections link to the HTML pages | pass | `README.md:61` → `research/research.html` · `README.md:86` → `people/personas.html` |
| 24 | `index.html` data block regenerated — artifacts present, context filled | pass | JSON parsed clean: phase 2 has all 6 artifacts `exists: true`, `steps` 17 of 19 with `current: users.9`; `context.benchmarkDimension`, `context.primaryPersona` and `context.mainJob` all non-empty |
| 25 | Phase committed; pushed if hosting is `active` | pass | `8a00b3f` (2a), `2bb4e5d` + `8917b36` (2b), `77b9a45` (Refero critique) — all on `main` and pushed; hosting is `active` in `toolbox.md` |

## Open

Nothing blocking. Three items are recorded here so the next phase does not rediscover them —
none of them is a checklist failure:

- **`research/screens/` hygiene.** 4 `_verify-*` working captures and 1 unreferenced capture sit
  alongside the 33 real ones. Cleanup belongs to whoever next touches that folder.
- **A stale count in prose.** `research/research.md` and the phase-2a ledger say "27 captures";
  the real figure is 38 present / 33 referenced. `README.md` was corrected during phase 2b; the
  older artifacts were deliberately left alone rather than back-edited.
- **Three `[?]` handed to phase 3 by the MVP gate** — the form and weight of intent, the renaming
  of the third breakdown axis, and whether client alignment (R4) falls out of existing collections.
  Plus one from the re-research: **Fonts In Use moderates before publication**, which H5 must
  answer.
