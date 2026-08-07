# Phase 3 — Structure · check results

Checked: 2026-08-07 · Checklist: `.design/checklists/phase-3-ia.md`
Result: **pass** — 22 pass · 0 fail · 0 human · 22 of 22 items

First close of this phase; the tag `phase-3-ia` does not yet exist. Browser items were verified
with Playwright MCP, which `.design/memory/toolbox.md` records as `active`.

**One item carries a logged exception rather than a clean literal pass — item 18.** It is called out
in Open below rather than buried in its row.

| # | Item | Verdict | Evidence |
|---|---|---|---|
| 1 | Entities listed, each tied to a job; jobless objects in a separate section | pass | `ia/sitemap.md` → **Entities**, 7 rows each naming its job or stating plainly that none produces it (`Author`); **Questionable** section holds 4 more — Quality mark, Tag, Like/Follow, Comment |
| 2 | Screens derived from the product's own jobs, not a competitor's menu | pass | The tree's own note records the single deliberate debt to the market — a task taxonomy as the entry — and grounds it in H7 and `[INT · Даня · B1 Q6]`, not in a menu |
| 3 | Every screen annotated with its job; jobless screens marked `[ORPHAN]` | pass | All 7 screen nodes carry job ids. **Zero `[ORPHAN]` markers in the tree is correct**: the one screen that had none (`Author`) was removed at the gate. `Publish` and `Confirm the extraction` carry `[HYPOTHESIS]` — they *have* jobs (HJ1, HJ2), which are unevidenced, and the matrix separately lists them as orphan columns. Two labels, two different definitions, both stated in the file |
| 4 | Screens and states not confused | pass | `ia/sitemap.md:65` — "States — empty, error, loading — are **not** screens; they belong to `wireframes/_screens.md` in phase 4". `ia/flows.md` opens with a shape legend making the same split |
| 5 | Global navigation, 3–5 items, each justified by its job | pass | **3 items** — Search, Collections, Publish — each with a job cluster and a stated reason; four rejected candidates recorded so the absences read as decisions |
| 6 | Tap depth to the main job counted for the primary persona | pass | `ia/sitemap.md:146` — a five-row path table, main job at **2 taps** |
| 7 | Main job within three taps, or the trade-off argued | pass | **2 of a 3-tap budget.** The spare tap is explicitly reserved for what `Work` cannot hold at once; the reason it stays at 2 is stated — the breakdown sits on `Work` rather than behind it |
| 8 | Main-job flow in Mermaid with steps, diamonds, empty/error/loading, both endings | pass | Flow 1 — screens `Search`, `Results`, `Work`; 6 diamonds; **loading, error, two distinct empties, unconfirmed**; success plus the two former dead ends now routed back |
| 9 | 2–3 key related-job flows also drawn | pass | **Three** — R3, R4, HJ1 |
| 10 | Every flow node exists in the sitemap; new ones added back | pass | The seven square nodes across all four flows are exactly the seven sitemap screens: `Search`, `Results`, `Work`, `Collections`, `Collection`, `Publish`, `Confirm the extraction`. `flows.md` records "none added" |
| 11 | Mermaid syntax valid — diagrams render as diagrams | pass | All four parsed and rendered by **Mermaid 11.16.1 in Chromium, zero errors**, twice: once before the critique fixes and once after. Not checked by eye |
| 12 | At least one "no" branch leads somewhere real | pass | **Six** do: `SErr→Search`, `DeadTax→Search`, `Thin→Results`, `CErr→Collections`, `Lost→Search`, `SErr3→Collection` |
| 13 | Traceability matrix, jobs as rows, screens as columns | pass | 11 job rows × 7 screen columns, plus a separate 2-row block for the hypothesis jobs |
| 14 | Orphan screens and orphan jobs listed explicitly | pass | Both tables present — 2 orphan screens (`Publish`, `Confirm the extraction`), 1 orphan job (`S3`) |
| 15 | Each orphan has a decision | pass | Keep-with-recorded-weakness for both screens, with the reason each is kept; **deliberately unserved** for S3, with the reason it is not built |
| 16 | Critique across four defect classes, against the existing matrix | pass | `.design/progress/phase-3.md` `ia.6` and `.design/decisions.md` — 10 defects across dead ends, missing states, excess depth and orphans; the orphan rows reconcile against the existing matrix rather than rebuilding one |
| 17 | Dead ends and missing states fixed, visible in the flows | pass | Four dead ends gained exits and three flows gained error states; `flows.md` states "no dead end left" per flow and the coverage table lists the states now present. Two dead ends survive **labelled as deliberate** — a client who never replies, and the abandonment criterion 3 exists to measure |
| 18 | `ia/ia.html` opens standalone with the tree, **live-rendered** Mermaid and the matrix | pass | Chromium at `http://127.0.0.1:8745`: 4 diagrams, 1 tree block, 6 tables, 26 matrix ticks, 2 orphan rows, 0 broken images, no horizontal scroll, **0 external references** — it opens with no script and no network. **The word "live-rendered" is not satisfied literally**: the diagrams are genuine Mermaid output on the dark theme, rendered at build time and inlined as SVG. Waived as a one-off exception at a human gate on 2026-08-07 ("лишаємо svg"), logged in `.design/decisions.md` with the trade — a 686 KB self-contained page over a 3.5 MB vendored renderer. **Outcome met, mechanism deviates, deviation gated** |
| 19 | `CLAUDE.md` → Structure block records the main flow and navigation | pass | Six screens, three global items, the 2-of-3 tap budget, the main flow, and the five decisions later phases inherit |
| 20 | `README.md` Structure section links to `ia/ia.html` | pass | Present, alongside links to `sitemap.md` and `flows.md` |
| 21 | `index.html` data block regenerated — phase 3 artifacts present | pass | JSON parses; all three phase-3 artifacts `exists: true`, `steps` 9 of 10 with `current: "ia.10"` |
| 22 | Phase committed; pushed if hosting is `active` | pass | `7634c59`, `8bc5a47`, `7e5c180` — all on `main` and pushed; `git status --short` → 0 lines |

## Open

Nothing blocking. Three things recorded so the next phase does not rediscover them:

- **Item 18 is a granted exception, not a silent pass.** If phase 4's wireframe navigator or any
  later HTML page needs true live rendering, the decision to vendor Mermaid gets re-opened there —
  the log entry exists so it is not re-argued from zero.
- **A drift risk created by that exception:** `ia/ia.html` will not pick up an edit to
  `ia/flows.md` without the render step being re-run. Whoever next edits the flows owns that.
- **The structure's weakest joint, stated rather than hidden:** `Publish` and `Confirm the
  extraction` are reached by hypothesis jobs only, and the "no empty row or column" target is
  deliberately not met. If HJ1 fails, that cluster is the first thing that changes.
