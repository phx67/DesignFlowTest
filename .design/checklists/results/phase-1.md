Reopened 2026-08-07 · by /dsf:change · the brief's manual-breakdown rule and the content unit both changed

# Phase 1 — Brief · check results

Checked: 2026-08-05 · Checklist: `.design/checklists/phase-1-brief.md`
Result: **pass** — 13 pass · 0 fail · 0 human · 13 of 13 items

Re-check. The 2026-08-05 run earlier the same day returned 12 pass · 1 human: item 8 could not be
verified because the Playwright MCP server would not launch. The browser now works and item 8 was
verified directly, with screenshots. No artifact changed between the two runs.

| # | Item | Verdict | Evidence |
|---|---|---|---|
| 1 | Brief produced by a structured brainstorm, human's answers recorded not invented | pass | `.design/progress/phase-1.md:4-5` (`brief.2`, `brief.3`) + `.design/decisions.md` — 3 gate entries, answers verbatim incl. the mid-gate re-scope from private archive to community pool |
| 2 | `CLAUDE.md` Brief block: what it is, problem, who for, platform, constraints | pass | `CLAUDE.md:12` (what), `:16` (who), `:23` (problem), `:38` (platform), `:42` (constraints) |
| 3 | Success criteria written and observable | pass | `CLAUDE.md:52-59` — three criteria, each a checkable action: reproduce from the breakdown screen, read status+completeness off a card without opening it, complete the publish flow without abandonment |
| 4 | Unanswered marked `[?]` with an explicit hypothesis | pass | `CLAUDE.md:63,67,69,74,76,80` — six `[?]`, each carrying *Hypothesis:* and the phase that closes it |
| 5 | Brief names what the product is not doing | pass | `CLAUDE.md:48-50` — five exclusions incl. "not AI or auto-extraction in place of the author" |
| 6 | Twelve pipeline folders, none missing, none invented | pass | `research/ people/ ia/ wireframes/ voice/ concept/ ui/ design-system/ visuals/ responsive/ animations/ handoff/` all present, each with `.gitkeep`; no folder created outside the list |
| 7 | `README.md` Brief section filled and matches `CLAUDE.md` | pass | `README.md:23-43` — same product, same spine (manual breakdown as index), same platform split, links to `CLAUDE.md` for the full text |
| 8 | `index.html` renders standalone; phase 1 `in progress` with artifacts present; `context.product` / `oneLiner` filled | pass | Verified in Chromium via the Playwright MCP, served at `http://127.0.0.1:8731/index.html`. Header reads **Loupe**; phase 0 green, phase 1 badged **in progress**, phases 2–10 grey; footer "1 of 11 phases done". Result tab renders `PRODUCT: Loupe`, the one-liner in full, `ARTIFACTS 2/2` with `CLAUDE.md` and `README.md` both ticked, and "12 of 13 criteria closed". Console: one 404 for `/favicon.ico`, which the local server produces and the repo does not carry — no JS errors, all four `assets/` files load, zero external requests |
| 9 | `.design/memory/toolbox.md` has no `[?]` in the Status column | pass | All 7 rows resolved: Browser `active`, Visual references `fallback`, Design quality `active`, Structured brief `active`, Imagery `fallback`, Icons `active`, Hosting `active` |
| 10 | Repo under git with the brief committed | pass | `fceb502` — "feat: phase 1 — product brief and repo scaffolding", touching `CLAUDE.md` and `README.md` |
| 11 | Pushed, since `toolbox.md` records hosting as `active` | pass | `317b964` pushed; `HEAD == origin/main` at the time of the check |
| 12 | No claim about audience or market without a source or a `[?]` | pass | `CLAUDE.md:27-28` names the source of the problem statement — the designer's own testimony at the phase-1 gate, logged verbatim in `.design/decisions.md` — and says phase 2 tests it against other people. The one unsourced load-bearing claim, supplier motivation, is `[?]` at `CLAUDE.md:63`. **Caveat for phase 2:** the source is a single person, so the audience and problem are testimony, not research |
| 13 | Brief fits on one screen | pass | `CLAUDE.md:10-61` — 52 lines of body, trimmed from 79 during `brief.7` because the first draft did not fit |

## Open

Nothing blocking. Two notes carried forward, neither a checklist item:

- **The dashboard `steps` object is two lines behind the ledger.** It reads `8 of 10 steps done`,
  current `brief.9`; `.design/progress/phase-1.md` carries `brief.9` and `brief.10`. The ledger is
  the truth and the dashboard is the cache (constitution rule 8). `/dsf:check` may not write that
  key — its edits are limited to `criteria`, `status`, `tagged` and `exists` — so `/dsf:status`
  repairs it.
- **The evidence under item 12 is one person.** The audience and all three confirmed problems rest
  on the designer's own testimony. That clears this checklist, which asks only for a named source,
  but phase 2 must widen it or the brief stays a hypothesis with a citation.

---

# Phase 1 — Brief · re-check after reopening

Checked: 2026-08-07 · Checklist: `.design/checklists/phase-1-brief.md`
Result: **fail** — 12 pass · 1 fail · 0 human · 13 of 13 items

Re-check after `/dsf:change` (commit `9a37af7`) replaced the brief's manual-breakdown rule with
machine extraction plus author confirmation, and fixed the content unit as one screen **or** a
whole case. Every item was re-verified from the repo; nothing was carried over green from the
2026-08-05 verdict above.

| # | Item | Verdict | Evidence |
|---|---|---|---|
| 1 | Brief produced by a structured brainstorm, human's answers recorded | pass | Historical and unchanged by this reopening: `.design/progress/phase-1.md` steps `brief.1`–`brief.10`; `.design/decisions.md` carries the gate answers in the designer's own words |
| 2 | Brief block states product, problem, who, platform, constraints | pass | `CLAUDE.md` — **Loupe** (`:12`), **Problem** , **Who it is for**, **Spine**, **Platform**, **Constraints**; all present after the rewrite |
| 3 | Success criteria written and observable | pass | `CLAUDE.md:82–92` — 3 numbered criteria; 2 and 3 restated on 2026-08-07 so they test the confirmed/unconfirmed signal and the confirmation step rather than transcription |
| 4 | Unanswered things marked `[?]` with a hypothesis, not a default | pass | 10 `[?]` marks in the Brief block, each followed by an explicit hypothesis; one **added** by this change ("what 'confirmed' is worth") and one **closed** with its reason stated (the content unit) |
| 5 | The brief names what it is not doing | pass | `CLAUDE.md:76–80` **Out of scope** — rewritten to keep the exclusion meaningful: extraction is in scope, speaking *in place of* the author is not, and intent is never generated |
| 6 | Twelve pipeline folders, none missing, none invented | pass | All twelve present: `research/ people/ ia/ wireframes/ voice/ concept/ ui/ design-system/ visuals/ responsive/ animations/ handoff/` |
| 7 | `README.md` Brief section filled and matches `CLAUDE.md` | pass | `README.md:27–36` — carries the same two changes: "the machine extracts the measurable parts; the author confirms them and supplies… the intent" and "a single screen or a whole case" |
| 8 | `index.html` renders standalone, phase 1 `in progress`, artifacts present, `context.product` + `context.oneLiner` filled | pass | Opened in Chromium at `http://127.0.0.1:8735` — renders, no horizontal scroll, only console entry is the local `/favicon.ico` 404. `phases[1].status: "in-progress"`; both artifacts `exists: true`; `context.product: "Loupe"`, `context.oneLiner` non-empty |
| 9 | `.design/memory/toolbox.md` has no `[?]` in the Status column | pass | The tools table reads `active / fallback / active / active / fallback / active / active`. The 4 `[?]` occurrences in the file are all in the legend and the fallback rules, not in a Status cell |
| 10 | Repo under git with the brief committed | pass | `9a37af7` — `CLAUDE.md` and `README.md` both in the commit; working tree clean |
| 11 | Pushed, hosting `active` | pass | `git status -sb` → `## main...origin/main`, no divergence; `toolbox.md` records hosting `active` |
| 12 | No audience or market claim without a source or `[?]` | pass | Unchanged by this reopening. Every audience claim still carries the designer's testimony or a `[?]`; the market claims added on 2026-08-07 cite `[RES]` H1 and the Refero split |
| 13 | **The brief fits on one screen; it does not pre-empt later phases** | **fail** | The Brief block is now **121 lines / 1376 words**, against **81 lines / 847 words** when this item last passed on 2026-08-05 — **+62% by word count in one change**. The growth is not product substance but inline change-history: dated "this replaces…", "changed 2026-08-07", "weakened", "narrowed" annotations. Several of them also instruct later phases directly, which is what the second half of the item forbids |

## Open

- **Item 13 — the brief outgrew itself.** The change was correct and none of it should be lost, but
  its *history* does not belong in the brief: the full record already lives in
  `.design/decisions.md` (2026-08-07 entry) and in the superseded notes inside
  `research/research.md`. What closes this: `/dsf:brief` — compress the Brief block back to the
  **decisions**, keeping the `[?]` marks and dropping the narration of what each line used to say,
  leaving a single pointer to the decision log. Not a job for `/dsf:check`, which fixes nothing.

Two notes carried forward from the 2026-08-05 verdict, neither a checklist item and neither
affected by the reopening:

- **`context.oneLiner` is now slightly behind the brief.** It reads "designers publish their own
  work with their own breakdown"; the breakdown is now machine-drafted and author-confirmed. It is
  not false — the author still owns it — but it is worth a rewording. `/dsf:check` may not write
  `context`; `/dsf:status` or `/dsf:brief` owns it.
- **The evidence under item 12 is one person.** Phase 2 added a second named respondent, so this is
  less true than it was, but the brief's own claims still rest largely on the designer's testimony.

**Re-run 2026-08-07, same day, verdict unchanged.** `/dsf:check 1` was invoked again before any fix
landed. Evidence that all thirteen verdicts above still stand: `HEAD` is still `12fd5c2` — the very
commit this verdict was written against — the working tree is clean, and
`git diff 12fd5c2 -- CLAUDE.md README.md index.html` is empty. The Brief block is still 121 lines /
1376 words. No new section is written and the dashboard `criteria` object is already current
(`passed 1–12`, `failed [13]`, `checkedAt 2026-08-07`); duplicating an identical table would make
this file harder to read as a history, which is the only reason it exists.

**Note on why item 13 is still open:** `/dsf:brief` ran and stopped at its own approval gate — the
compressed brief was presented in chat and **not approved, so nothing was written**. The fix is one
approval away, not one command away.

---

# Phase 1 — Brief · re-check after the compression

Checked: 2026-08-07 · Checklist: `.design/checklists/phase-1-brief.md`
Result: **pass** — 13 pass · 0 fail · 0 human · 13 of 13 items

Third verdict of the day, against `a02d1ca`. The 2026-08-07 re-check above failed item 13 — the
brief had grown to 121 lines / 1376 words carrying its own change history. `/dsf:brief` compressed
it back to decisions. Every item re-verified from the repo; nothing carried over green.

| # | Item | Verdict | Evidence |
|---|---|---|---|
| 1 | Brief produced by a structured brainstorm | pass | `.design/progress/phase-1.md` — `brief.2 · Interrogate` with the gate answer in the designer's words; the compression changed no decision, only their narration |
| 2 | Brief block states product, problem, who, platform, constraints | pass | All six headings present in the rewritten block: **Loupe**, **Who it is for**, **Problem**, **Spine**, **Platform**, **Constraints** |
| 3 | Success criteria written and observable | pass | Three numbered criteria: reproducibility checked per screen; a card showing reality status, confirmed/unconfirmed and intent progress without being opened; the publish flow completing without abandonment |
| 4 | Unanswered things marked `[?]` with a hypothesis | pass | 4 open `[?]`, **4 `*Hypothesis:*` clauses** — one per question. Three others were closed with their phase-2 answers cited, not dropped |
| 5 | The brief names what it is not doing | pass | **Out of scope** present; the AI exclusion kept meaningful — extraction drafts, the author confirms, intent is never generated |
| 6 | Twelve pipeline folders, none missing, none invented | pass | 12 of 12 present |
| 7 | `README.md` Brief section filled and matches `CLAUDE.md` | pass | `README.md` carries both current rules — "the machine extracts the measurable parts; the author confirms" and "a single screen or a whole case" |
| 8 | `index.html` renders standalone, phase 1 `in progress`, artifacts present, `context.product` + `context.oneLiner` filled | pass | Chromium at `http://127.0.0.1:8736`: renders, no horizontal scroll, no `{{PRODUCT_NAME}}` anywhere, only console entry is the local `/favicon.ico` 404. `phases[1].status: "in-progress"`, both artifacts `exists: true`, `product: "Loupe"`, `oneLiner` reworded to "a breakdown they confirm" |
| 9 | `.design/memory/toolbox.md` has no `[?]` in the Status column | pass | Status column reads 5 × `active`, 2 × `fallback`, 0 × `[?]` |
| 10 | Repo under git with the brief committed | pass | `a02d1ca`; `git status --short` returns 0 lines |
| 11 | Pushed, hosting `active` | pass | `## main...origin/main`, no divergence |
| 12 | No audience or market claim without a source or `[?]` | pass | Audience claims cite the designer's testimony or `people/personas.md`; the market claims that justified the extraction rule were moved out to `research/research.md` with the compression |
| 13 | **The brief fits on one screen; it does not pre-empt later phases** | **pass** | **85 lines / 891 words**, against 121 / 1376 at the failing check and 81 / 847 when it last passed — **+5% over that baseline, and the delta is three new decisions** (polymorphic unit, extraction + confirmation, completeness on intent alone) plus one new `[?]`, not narration. Second half verified separately: `grep -nE 'phase [0-9]+ must\|must not design'` over the block → **no matches**; phases are named only as owners of an open `[?]`, which is how the block read when it passed. Change-history residue → **0 matches** |

## Open

Nothing. The item-13 failure from earlier today is closed at its source: the change history now
lives only in `.design/decisions.md` and in the superseded notes inside `research/research.md`.

One note carried forward, not a checklist item: the brief's own claims still rest largely on the
designer's testimony, though phase 2 added a second named respondent. The `context.oneLiner` drift
flagged by the previous two verdicts is **closed** — `/dsf:brief` reworded it, and the dashboard
`steps` drift flagged on 2026-08-05 is closed too, `steps.done` now running `brief.1`–`brief.10`.
