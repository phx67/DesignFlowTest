# Decisions

The project's decision log. Every human gate answer, every "keep it", every spec contradiction
resolved under constitution rule 12, and every change request lands here as one entry.

**Append-only.** Newest entry at the bottom. Nothing is edited after the fact and nothing is
deleted — a decision that was later reversed stays, and the reversal is a new entry that names
it. The log is the project's memory of *why*; rewriting it is how a repo starts lying about
itself.

**Written by** any `/dsf:*` command at its gates, and by the rule-12 guard whenever a request
contradicts something written. **Read by** `/dsf:status` (what has been decided so far) and
`/dsf:change` (whether this request has already been settled once).

## Entry format

One heading plus four fields per entry, nothing else:

```md
## YYYY-MM-DD · <trigger>

**Decided:** what was decided — the human's own words, verbatim, wherever they said it.
**Contradicts:** `file:line` + the line quoted — or `nothing`.
**Option:** spec-update | exception | withdrawn | n/a
**Propagated:** every file touched as a result — or `none`.
```

- **trigger** is one of: `gate` (a mandatory gate answer), `keep-it` (an experiment promoted to
  a rule), `contradiction` (the rule-12 guard fired), `change-request` (`/dsf:change`).
- **Option** is `n/a` for a plain gate answer that contradicted nothing.
- **Verbatim matters.** "Warmer, less corporate — like the second one" is a decision. "The human
  approved the palette direction" is a summary of one, and summaries are what drift is made of.
- Keep an entry to five lines. If the reasoning needs more, it belongs in the artifact; link it.

---

## 2026-08-05 · gate

**Decided:** "артефакти англійською, обговорення українською; мова продукту — окреме рішення фази 5"
**Contradicts:** `nothing`
**Option:** n/a
**Propagated:** all phase artifacts stay English; product UI language deferred to phase 5 `/dsf:voice`, recorded as a constraint in `CLAUDE.md` — Brief.

## 2026-08-05 · gate

**Decided:** "демотуй проблему 3 до [?], як і фічу" — then "затверджую" on the brief carrying that edit.
**Contradicts:** `nothing` — the brief was unwritten; the edit was made before it reached disk.
**Option:** n/a
**Propagated:** `CLAUDE.md` (Brief), `README.md`, `index.html`. Comparison demoted from confirmed problem and from the spine to an open `[?]`; the structured-fields decision now rests on the index alone.

## 2026-08-05 · gate

**Decided:** "розбір є індексом (шукаєш за властивостями), але колір/тип/сітку заповнює дизайнер вручну при заливанні рефа. Ніякого авто-витягування. Саме заповнення розбору = акт деконструкції." — later re-scoped by the human to a community pool: "Спільнотний сайт відкриттів для дизайнерів, а не приватний архів. […] Головний момент — відкриття зі спільного пулу, а не повторне знаходження власного мотлоху."
**Contradicts:** `nothing` on disk — the first, private-archive brief was played back in chat and rejected at the gate before any file was written.
**Option:** n/a
**Propagated:** `CLAUDE.md` (Brief), `README.md`, `index.html`. Manual deconstruction survived the re-scope; the private archive did not.
