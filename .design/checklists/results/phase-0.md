# Phase 0 — Init · check results

Checked: 2026-08-04 · Checklist: `.design/checklists/phase-0-init.md`
Result: **pass** — 12 pass · 0 fail · 0 human · 12 of 12 items

| # | Item | Verdict | Evidence |
|---|---|---|---|
| 1 | No `[?]` in the Tools table | pass | `awk '/^## Tools/,/^## Rules/' .design/memory/toolbox.md \| grep -cF '`[?]`'` → `0` (expected 0). Statuses: active·fallback·active·active·fallback·active·active |
| 2 | Evidence for every `active`, reason for every `fallback`, in **Notes** | pass | `.design/memory/toolbox.md` **Notes** — 7 entries, one per row. Concrete evidence present: `v0.0.78`, chromium, `LD_LIBRARY_PATH`, `v4.0.4`, `v6.2.0`, `brainstorming`, device-code auth. Fallback reasons: `GEMINI_API_KEY` unset, `refero.design` account required |
| 3 | **Rules for later phases** operational, not a restatement | pass | `.design/memory/toolbox.md` — 2 bullets for 2 `fallback` rows. Each names the phase, the command and the artifact: `/dsf:concept` → `concept/references.md` labelled `[web]`; `/dsf:build` → Unsplash with query+URL+credit in `visuals/README.md` |
| 4 | Git repo initialized; remote configured | pass | `git rev-parse --is-inside-work-tree` → `true`; `origin` → `https://github.com/phx67/DesignFlowTest.git` |
| 5 | Hosting decided: Pages enabled, URL recorded | pass | `gh api repos/phx67/DesignFlowTest/pages` → `html_url: https://phx67.github.io/DesignFlowTest/`, `source: main /`, `status: built`. URL recorded in `.design/memory/toolbox.md` and `README.md:9` |
| 6 | Renders: phase 0 in progress, 1–10 locked, artifacts missing | pass | Chromium render of `index.html`: phase 0 `class="nav-item is-current-phase"`, phases 1–10 plain `nav-item`, footer `0 of 11 phases done`. 49 of 51 artifacts `exists: false`. The 2 flagged `true` are phase 0's own outputs, which exist — scored per the human's adjudication below |
| 7 | Eleven phases, canonical paths, `context` values empty | pass | Data block parsed: 11 phases; every artifact path matches the canonical spellings in `.design/memory/phases.md`; all six `context` strings `""`. `context.toolbox` holds 7 rows — the documented non-string exception in `phases.md` |
| 8 | Nothing edited outside the data block, nothing in `assets/` | pass | `git diff 66bbef7..HEAD -- assets/` → empty. `git diff 66bbef7..HEAD -- index.html` → hunks at `@@ -3150` and `@@ -3162` only; the data block spans lines 3142–3360 |
| 9 | `CLAUDE.md` **Toolbox** filled; context blocks untouched | pass | `CLAUDE.md` — 7 bullets, one per toolbox row with its status. Context blocks: 12 `[?]` intact. `git diff 66bbef7..HEAD -- CLAUDE.md` → one hunk, `@@ -54`, the Toolbox section only |
| 10 | `README.md` present, with the `index.html` link | pass | `README.md`, 15413 bytes; line 9 carries `https://phx67.github.io/DesignFlowTest/` |
| 11 | First commit made; pushed since hosting is `active` | pass | `0235fc7` phase 0 scaffolding, `3a2eca1` ledger close, `06a1562` gitattributes. `HEAD` == `origin/main` == `06a1562e995…` |
| 12 | Designer handed the project page: link, purpose, first move | pass | Delivered in-session at step `init.9`; ledger line `.design/progress/phase-0.md` → `init.9 · Hand over the project home page · 2026-08-04 17:13`. Handover carried the Pages URL, the state-view framing, and `/dsf:brief` as the single next move |

## Open

None. All twelve items pass.

## Notes on this verdict

**Item 6 — adjudicated at a human gate, 2026-08-04.** The item's third clause reads "every
artifact showing as missing", but `.design/memory/phases.md` binds `exists` to *"true once the
file is real and non-empty"* and instructs phase commands to mark their own artifacts `true`
(`/dsf:init` step 8 says the same). Phase 0's two artifacts — `.design/memory/toolbox.md` and
`index.html` — are real and non-empty, so the two rules cannot both be honoured.

Put to the designer, who chose to read "every artifact" as the not-yet-produced artifacts of
phases 1–10, on the grounds that a phase's checklist requiring its own outputs to show as missing
is self-contradictory. Scored **pass** on that reading. The alternative offered and declined was
to flip both flags to `false`, which would have made the dashboard contradict the files on disk.

**This is a framework-level wording defect, not a project one.** Item 6 as literally written can
never pass on any project, because `/dsf:init` always produces those two files. It is worth
reporting upstream: the clause should scope itself to phases 1–10, or to "artifacts of phases not
yet run". Recorded here so the next `/dsf:check 0` on any repo does not re-litigate it from zero.
