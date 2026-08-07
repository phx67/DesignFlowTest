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

## 2026-08-07 · gate

**Decided:** "Персони підтверджую, primary — Персона 1 (Даня). Персона 3 лишається [?] — свідомо, як головний ризик проєкту (сторона постачання без досліджень). / Контрадикція платформи — варіант 1, оновити спеку, але вузько: мобільний отримує пошук/відкриття + збереження; розбір-авторство й важке фасетне зіставлення лишаються десктопними; чи потрібне мобільному повне фасетне фільтрування — [?] на фазу 8. Запиши доказ [INT · Даня · B3 Q4] і онови Platform у брифі."
**Contradicts:** `CLAUDE.md` → Brief → Platform, as written at phase 1 — "**Mobile**: browsing and saving to a collection, nothing else." The contradicting evidence is `[INT · Даня · B3 Q4]`: "Eagle крутий, але він десктопний, **а я часто шукаю з телефону в дорозі**" — the primary persona rejected a tool for not letting him *search* on a phone. The phase-1 line carried no research source; it was a deliberate choice made before any interview existed.
**Option:** (1) spec-update, narrowed. The phone gains **search, open a work, read its breakdown, save**. Authoring (writing the breakdown, upload) and heavy side-by-side facet comparison stay desktop. **Full facet filtering on mobile is left `[?]` for phase 8** — one respondent, one sentence, and it does not separate *finding* from *filtering*. Personas confirmed as written: 3 personas, primary = Persona 1; Persona 3 stays entirely `[?]` by explicit decision, as the project's main risk (the supply side has no research behind it).
**Propagated:** `CLAUDE.md` (Brief → Platform, and the Brief context block), `README.md` (Platform), `people/personas.md` (contradiction section marked resolved; open question 4 narrowed and routed to phase 8). Downstream inheritors: phase 3 `/dsf:ia` (mobile now carries a search entry point, so the sitemap and tap-depth budget must serve it) and phase 8 `/dsf:responsive` (owns the remaining facet-filter `[?]`).

## 2026-08-07 · gate

**Decided:** "Три роботи ядра підтверджую: Main, R2, R3. / Уточнення до Main: «намір» — це цінність/робота (глядач розуміє «чому»), а не обовʼязкове поле. Механізм подачі наміру — через сам матеріал роботи (кейс), легко/опційно/прогресивно; форма й вага — [?] на фазу 3. Жодної примусової форми «обґрунтуй». / Список вирізу приймаю, зокрема: — окремий екран порівняння — ріжу (зіставлення виходить побічно зі спільних полів); — лайки й підписку на автора — ріжу свідомо, у v2 (обслуговують P2 / непідтверджену P3, не первинного Даню); — теги як механізм пошуку — ріжу (лишаються особистим контекстом у колекціях). / «Колонковий грид як третя вісь» — виріз приймаю, але зафіксуй [?]: третю вісь розбору переозначити (база / щільність / spacing, не колонковий грид) у фазі 3/6. / R4/S2 (спільна картина з клієнтом) — варіант (c): лишити [?] на фазу 3, хай IA перевірить, чи «колекція, яку можна показати не-дизайнеру» випадає з наявних колекцій майже безкоштовно. Не ріжу і не роблю четвертою роботою ядра."
**Contradicts:** two written lines, both resolved by narrowing rather than by reversal. (1) `CLAUDE.md` → Brief → Spine: "Social layer: save to a collection, like, follow an author" — likes and follow are cut from the MVP. (2) `CLAUDE.md` → Brief → Spine: "structured fields (colour, typography, grid) + a free-text 'why'" — the third axis is no longer a column grid, and the "why" is not a required free-text field.
**Option:** MVP scope set. **Core: Main, R2, R3**, read off the matrix (importance 3 for the primary persona AND not closed by the market). **Cut: likes, follow-an-author, column grid as the third axis, a dedicated side-by-side comparison screen, tags as a retrieval mechanism.** Likes and follow are cut *deliberately, to v2* — they serve P2 and the unevidenced P3, not the primary persona. Three `[?]` marks are created rather than closed: **intent's form and weight** (phase 3 — it is a value and a job, never a compulsory "justify it" field, carried through the work's own case material, easy/optional/progressive); **the third breakdown axis must be re-named** as base unit / density / spacing (phase 3, then into tokens at phase 6); **R4/S2 client alignment** (phase 3 — the IA checks whether "a collection you can show a non-designer" falls out of existing collections almost for free). R4/S2 is neither cut nor promoted to a fourth core job.
**Propagated:** `people/jtbd.md` (gate refinement under the main job, the full matrix, MVP core, cut candidates, the uncovered-job section). Downstream inheritors: **phase 3 `/dsf:ia`** owns all three new `[?]` marks; **phase 6 `/dsf:build`** inherits the third-axis rename into the tokens. `CLAUDE.md` → Brief is **not** rewritten here — the brief's spine still describes the product, and the MVP scope is a phase-2 narrowing of it recorded in `jtbd.md`; if phase 3 finds the two disagreeing in practice, that is a `/dsf:change`.

## 2026-08-07 · change-request (rule-12 guard fired)

**Decided:** "Бриф каже «Заповнює автор, вручну. Жодного авто-витягування», але переходимо на: машина витягує обʼєктивні поля (колір/тип/сітка) → автор підтверджує/править. Заодно уточни одиницю контенту в брифі: автор заливає один екран АБО цілий кейс." · scope: "Правило 12 — (1) оновити спеку. Скоуп — повний (радіус малий, борг лишати не хочу)." · consequence: "Наслідок №1: так — completeness тепер вимірює переважно намір. Обʼєктивні поля машина префілить, тож вони переходять зі стану «повнота» у стан «підтверджено / не підтверджено» (сигнал довіри), а намір (відсутній → присутній → кейс) стає єдиною прогресивною віссю повноти й ранжування. Усвідомлюю, що це концентрує ризик постачання на намірі."

**Contradicts:** four written lines, all in the phase-1 brief. `CLAUDE.md` → Brief → Spine — "The author fills it in **by hand — no auto-extraction anywhere.**"; `CLAUDE.md` → Brief → Out of scope — "Not AI or auto-extraction in place of the author."; `CLAUDE.md` → Research context block — "The breakdown is manual… no auto-extraction"; `README.md` — "The breakdown is filled in by hand — there is no auto-extraction". Also overrides one research recommendation: `research/research.md` → CONCLUSIONS, "Component or whole work?" — "**Phase 3 must pick one as the unit** and let the other be a facet"; the designer chose both.

**Why those decisions existed.** The manual rule came out of the phase-1 interrogation and was the premise of the phase-2 BENCHMARK dimension, confirmed at the gate on 2026-08-06: "the question is not 'can the breakdown be shown' but 'why would a person write one by hand when a machine writes it free' — which is `[?]` 1 of the brief, the one that rebuilds the spine if it fails." **Stated at the guard, and it matters:** the change does not contradict phase 2's *findings* — it contradicts a brief that phase 2 had already outgrown. `[RES]` H1 says the values are table stakes and intent is the only part a machine cannot supply; the Refero split of 2026-08-07 says "matching the values is table stakes, not the contest; the contest is comprehension". The spec chain was already internally inconsistent and this resolves it in the direction the evidence points.

**Option:** **(1) update the spec, full propagation.** No debt recorded — the designer explicitly refused to carry any ("борг лишати не хочу"). Three substantive consequences were put to the designer before the choice and all three were accepted: **(a)** the Discogs mechanic weakens, because a pre-filled breakdown has little left to charge for — phase 3 must say what the author still pays; **(b)** **H4 narrows to intent alone** — the objective fields are complete on day one, so they carry a *confirmed / unconfirmed* trust state instead of a completeness score, and intent (*absent → present → case*) becomes the single progressive axis for completeness and ranking; **(c)** on a fixtures-only static prototype, "the machine extracts" is a simulated step that phase 4 must render as UI states. The supply risk is now **concentrated entirely on intent**, which the designer recorded as understood.

**Propagated (full):** `CLAUDE.md` — Spine rewritten (extraction + confirmation, polymorphic unit, completeness redefined), Out of scope, success criteria 2 and 3, open question 1 narrowed, open question (b) closed, a new open question on what "confirmed" is worth, Brief context block, Research context block. `README.md` — the "what it is" paragraph. `research/research.md` — a superseded-in-part note on the BENCHMARK premise, mechanic 1, H2, H4, the "Component or whole work?" conclusion row, open question 3. `research/research.html` — the same six places. `people/personas.md` — Persona 3 pains. `people/jtbd.md` — the Main job's FEATURE cell, MVP core job 1, HJ2. `people/personas.html` — the same three places. **Nothing was rewritten silently: every superseded line is kept in place, dated, and marked as superseded.**

**What survives untouched, verified rather than assumed:** the chosen retrieval pattern (the fields are still declared and still carried by the work — only the drafter changed), all three MVP core jobs, all three personas and every job in `jtbd.md`, the Refero split and its conclusion, H1, H3, the platform split and the mobile decision, the benchmark's scoring table, and the cut list.

**Phases reopened:** 1 and 2 — `status` back to `in-progress`, `steps.done` left intact, `criteria` left intact, `Reopened` lines added to both results files and both ledgers. Tags `phase-1-brief` and `phase-2-discover` left in place; history not rewritten.

## 2026-08-07 · gate

**Decided:** "записуй" — approval of the compressed Brief block presented at the `/dsf:brief` step-3 gate.
**Contradicts:** `.design/checklists/results/phase-1.md` — item 13 failed the 2026-08-07 re-check: the Brief block had grown to 121 lines / 1376 words against 81 / 847 when it last passed, the growth being inline change history rather than product substance.
**Option:** compress. **No decision is changed or removed** — only the *biography* of decisions: the dated "this replaces…", "changed 2026-08-07", "(Restated…)", "Known and accepted" annotations added by the `/dsf:change` of the same day. That record is kept in full in this log (entry `2026-08-07 · change-request`) and in the superseded notes inside `research/research.md`; the brief now carries a single pointer to it. Every `[?]` keeps its explicit hypothesis. Additionally, **three `[?]` that phase 2 had already answered were closed** rather than left standing open in the brief: **the retrieval mechanism** (faceted filtering over the declared fields — pattern gate, 2026-08-06), **comparison** (stays demoted; the dedicated screen was cut at the MVP gate), and **the third axis** (not a column grid — `[RES]` H3; renamed to base unit / density / spacing in phase 3). The designer was offered the chance to restore any of the three and restored none.
**Propagated:** `CLAUDE.md` (Brief block rewritten, ~60 lines), `index.html` (`context.oneLiner` reworded — the breakdown is machine-drafted and author-confirmed, so "their own breakdown" was slightly behind the spec). `README.md` needed no change: its Brief section was already rewritten during the change request and still matches.

## 2026-08-07 · gate

**Decided:** "(a) Author — кредит на Work (лінк/підпис), не окремий екран; атрибуцію лишаємо, follow — v2. / (b) R4 — приймаю: спільний/клієнтський перегляд як режим колекції, не новий екран. / (c) Quality mark — лишити в Questionable, H5 непідтверджена в цій версії; функцію якості несе completeness + confirmed/unconfirmed, окремого обʼєкта курації не додаємо. / (d) Форма наміру — анотаційна модель: намір = анотації на матеріалі роботи (тицьнути ділянку + чому), прогресія absent → present → case. Не вільний абзац."
**Contradicts:** one written research instruction. `research/research.md` → CONCLUSIONS, **H5** — "*Test in phase 3: the quality state and who may set it exist as objects in the IA*". They do not, by this decision. H5 is therefore **unconfirmed in this version**, recorded rather than dropped. Nothing else was contradicted: (a), (b) and (d) all resolve `[?]` marks that phase 2 explicitly handed to phase 3.
**Option:** sitemap confirmed with four rulings. **(a)** `Author` loses its screen and survives as a byline on `Work`; the object had no job behind it and now has no destination either; follow stays cut to v2. **(b)** R4 — the job phase 2 could not place — is served by a **shared mode of `Collection`**, not a new screen, so the best-evidenced job in the whole set costs no new scope. **(c)** No curation object. The quality signal is carried by completeness on intent plus the confirmed / unconfirmed state of the extracted values; if the pool outgrows those two signals, the Questionable row is where the answer restarts. **(d)** **Intent is an annotation anchored to the work's material** — the author points at a region and says why — progressing *absent → present → case*. This closes the `[?]` the 2026-08-07 MVP gate assigned to phase 3, and it satisfies all three of that gate's constraints: carried by the material, optional, progressive, and no compulsory "justify it" form anywhere.
**Propagated:** `ia/sitemap.md` — Entities (Intent's form, Author reduced to attribution, Quality mark's Questionable row rewritten with H5's status), Screens (Author screen removed, shared view marked as a mode, six screens and no orphans), Navigation (three global items, tap budget). Downstream: phase 4 inherits the annotation model as the thing to wireframe, and `[RES]` H5 carries an **unconfirmed** verdict into phase 7, where contribution rules are written.

## 2026-08-07 · gate

**Decided:** "Чинити у джерелі: 1, 2, 3 — додати ребра (DeadTax→пошук по полях, Thin→Results, Lost→Search). 4, 5, 6 — додати error-вузли з поверненням (Flow 1→Search, Flow 2→Collections, Flow 3 — error на відправці). 7 — дії у круглі дужки, [...] лишити тільки за 7 екранами сітмапу. 8 — позначити Publish і Confirm the extraction як [HYPOTHESIS] у дереві. 10 — дописати в Entities, що Task і Facet value рендеряться всередині Search/Results. Лишити записом (не чинити): 9 — S3 свідомо поза скоупом (P2-only)."
**Contradicts:** `nothing` — the IA critique found defects against this phase's own output, not against an upstream decision.
**Option:** nine of ten rows fixed at the source, one left as a record. **Dead ends closed (1–3):** a task outside the taxonomy now falls back to a property query, a work with no intent returns to `Results`, and "never saved" routes to `Search` — that last node had promised an exit in its label that the graph did not draw. **Error states added (4–6):** flows 1, 2 and 3 each gained one with a return path; row 6 is worth naming because I had recorded flow 3's missing error as "a finding rather than an omission", which was a convenient formulation rather than a conclusion from evidence. **Node shapes fixed (7):** eight action nodes had been drawn with screen syntax, making the sitemap and the flows unreadable together; `[square]` is now reserved for the seven sitemap screens and a shape legend heads the file. **(8)** `Publish` and `Confirm the extraction` carry `[HYPOTHESIS]` in the tree — every job reaching them is unevidenced. **(10)** `Task` and `Facet value` are stated as rendering inside `Search` and `Results`, so phase 4 does not hunt for screens that were never intended. **(9) S3 stays unserved**, deliberately: it is P2-only, and P2 is the persona this product is not built for.
**Propagated:** `ia/flows.md` (all four diagrams redrawn, shape legend added, coverage table updated), `ia/sitemap.md` (Entities note, `[HYPOTHESIS]` markers). All four diagrams re-parsed and re-rendered by Mermaid 11.16.1 in Chromium after the fixes — zero errors. Two dead ends survive on purpose and are labelled as such: a client who never replies, and an author who abandons a failed extraction, which is what criterion 3 measures.

## 2026-08-07 · gate

**Decided:** "лишаємо svg" — the flow diagrams in `ia/ia.html` stay pre-rendered and inlined as SVG.
**Contradicts:** `.design/checklists/phase-3-ia.md`, item 18 — "`ia/ia.html` opens standalone in a browser with the screen tree, **live-rendered** Mermaid diagrams and the coverage matrix visible". The diagrams are Mermaid-rendered, but at build time rather than at page load, so the word "live-rendered" is not satisfied literally.
**Option:** one-off exception, recorded. Live rendering would mean vendoring `mermaid.min.js` — **3.5 MB** — into the repo and loading it on every visit, against a **686 KB** page that opens with no script and no network. The trade the designer took: a self-contained, fast page over literal compliance. **What is preserved either way:** the diagrams are genuine Mermaid output on the dark theme, and `ia/flows.md` stays the editable source, so any change is re-rendered from it rather than hand-edited in SVG. **What is given up:** the page cannot re-render a diagram edited in `flows.md` without the build step being re-run — a drift risk that belongs to whoever next edits the flows.
**Propagated:** nothing to change — the deviation is already stated in the `ia/ia.html` footer and in the shape legend. Recorded here so `/dsf:check 3` reads item 18 as a known exception rather than a defect, and so the same question is not re-litigated from zero in phases 5, 7 and 10, which also ship HTML pages.
