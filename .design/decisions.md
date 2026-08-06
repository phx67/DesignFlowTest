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

## 2026-08-05 · gate

**Decided:** "b" — the rule-13 phase-order guard fired on `/dsf:research` and the designer parked it, choosing to restart the session rather than run phase 2 out of order and without a browser.
**Contradicts:** `.design/checklists/results/phase-1.md` — "Result: **fail** — 12 pass · 0 fail · 1 human"; phase 1 is unsigned and untagged, so phase 2 is a later phase.
**Option:** withdrawn — no phase-2 work was done, no exception granted.
**Propagated:** none. Phase 2 starts fresh next session, after `/dsf:check 1` closes phase 1 with the browser working.

## 2026-08-06 · gate

**Decided:** "1. треба підняти з ASPIRATIONAL у HARD, це наш головний об'єкт для вивчення / 2. Локальний ринок - міжнародний. / 3. залишаємо, але переклеїмо ролі. лиши Polaris/Material, але як референс мови опису конструкції, а не конкурента за увагу"
**Contradicts:** `nothing`
**Option:** n/a
**Propagated:** `research/research.md` (COMPETITORS). Fonts In Use moves ASPIRATIONAL → HARD and is the phase's main object of study; Land-book dropped to keep HARD at five, its structured-filter lesson covered by Mobbin and Refero; the market stays international with no local-market row; Polaris/Material leave SOFT and become a **language reference** — studied for how construction is described, not scored in the competitor matrix.


## 2026-08-06 · gate

**Decided:** "Бенчмарк — постачання: як продукт отримує безоплатну структуровану працю й тримає якість без модерації. Бенчмаркимось проти Wikipedia / Stack Overflow / Discogs / Letterboxd / Genius / OpenStreetMap."
**Contradicts:** `.design/checklists/phase-2-discover.md` — "6–8 criteria, **4–5 reference products**, each scored"; the answer names six.
**Option:** exception, narrowed — five are scored and OpenStreetMap is cut, its mechanisms (open editing, community review, a tag wiki) duplicating Wikipedia's and its motivation being the furthest from Loupe's reputation hypothesis. The cut was stated to the designer at the time, with an offer to swap it back in for any of the five.
**Propagated:** `research/research.md` (BENCHMARK), `CLAUDE.md` → Research block (`benchmarkDimension`), `index.html` context.

## 2026-08-06 · gate

**Decided:** "Патерн — (1) фасетна фільтрація за задекларованими полями. Але інтерв'ю вже показує вхід назвою компонента (Даня фільтрує Mobbin по «екран реєстрації»/«кошик»), тож у /dsf:users перевір (4) таксономію задач як вхід, а фасети як уточнення всередині — модель Mobbin. (3) AI-запит дискваліфіковано для цього масштабу."
**Contradicts:** `.design/checklists/results/phase-1.md:35` — "The evidence under item 12 is one person." A second named respondent (Даня) is introduced here, so that note is now out of date rather than wrong.
**Option:** spec-update — the phase-4 condition on pattern 4 is no longer hypothetical; `/dsf:users` must capture the Даня interview as a citable artifact or carry it as `[?]`.
**Propagated:** `research/research.md` (PATTERNS, CONCLUSIONS), `CLAUDE.md` → Research block, `index.html`. Pattern 1 is the decision; pattern 4 is promoted from "second choice under a condition" to a named phase-2b test with the Mobbin model as its reference.
