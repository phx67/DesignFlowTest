<!-- filled by /dsf:users — start from this skeleton, do not restructure it -->

# Personas

**3 personas**, split by **behavior, not demographics**.

Personas are a **synthesis of research, not an act of authorship**. Every block below links back
to a specific place in the evidence. Where there is no data: `[?]`, phrased as a hypothesis,
never as a fact.

**Exactly one persona is marked primary**, with a stated reason.

## Evidence base and its limits

Two origins, cited separately throughout:

- **`[INT]`** — `sources/Interview Script 30e58b052da9800b8138cae64003069a.html`, a scripted
  interview with **two** respondents, **Валя** (graphic designer, 6 years) and **Даня** (mid
  UI/UX designer, small outsourcing studio). Cited as `[INT · name · Block N Q M]`. All quotes
  are verbatim from the transcript, in the original Ukrainian.
- **`[RES]`** — `research/research.md`, the phase-2a market study. Cited by section.

**Three limits on this base, stated before anything is built on it.**

1. **n = 2.** Two respondents, both in the Ukrainian market, one graphic and one UI/UX. No
   in-house product designer, no lead, no one outside this market.
2. **The interview never asks about supply.** Its stated goal is "Зрозуміти, як люди зараз
   шукають, зберігають і використовують візуальні референси" `[INT · Goal]` — how people
   *search, save and use*. Nobody was asked whether they would **publish their own work with a
   breakdown**. The project's main risk is therefore still carried entirely by `[?]`, and
   Persona 3 below is a hypothesis with no interview behind it.
3. **The template asks for a quote "from a real review or forum post found during research".**
   These quotes come from a primary interview instead, which is stronger evidence, not weaker.
   The deviation is deliberate and recorded here.

---

## Persona 1 — «Той, хто перевіряє, чи це взагалі можна побудувати»  ·  **PRIMARY**

**Why primary:** he is the brief's user, matched item for item. The brief's primary is "a designer
with **a task on the desk** — a specific component to design (empty state, pricing, onboarding
form)". He describes exactly that behaviour unprompted: "малюю кнопку чи картку товару - йду
дивитися, як це реалізовано в топових продуктах" `[INT · Даня · B1 Q3]`. He also confirms all
three of the brief's problems, while Persona 2 denies two of them. If the product is built for
one of these two people, the evidence says it is this one.

- **Context** — mid UI/UX designer in a small outsourcing studio, switching between tasks
  constantly: "Роботи доволі багато тому доводиться часто перемикатись між задачами."
  `[INT · Даня · B1 Q1]`. Works in stages — structure first, style second: "На початку проєкту -
  більше рішення. Мені важливо зрозуміти як інші вирішують цю ж задачу, які патерни працюють. А
  стиль - це вже потім, коли структура зрозуміла." `[INT · Даня · B4 Q3]`
- **Jobs**
  - Find how a **named component** is solved in shipped products. Enters by component name, not
    by property: "Mobbin зручний тим, що там є патерни: можна відфільтрувати суто «екран
    реєстрації» або «кошик»" `[INT · Даня · B1 Q6]`. **This confirms hypothesis H7 of
    `[RES · CONCLUSIONS]`, which until now rested on the designer's second-hand report.**
  - Take a solution apart well enough to rebuild it: "можливість його деконструювати. Коли я бачу
    не просто сайт, а розумію: ага, тут вони використали такий інтерліньяж і таку тінь, щоб
    створити об'єм **з певною ціллю**. Корисний той реф, який можна вкрасти як митець."
    `[INT · Даня · B4 Q1]`
  - Reach agreement with a client: "це фундамент для співпорозуміння з клієнтом" `[INT · Даня ·
    B1 Q2]`; "Зібрав мудборд прямо там, скинув клієнту на погодження. Він затвердив і я вже з
    розумінням напрямку йшов в макет." `[INT · Даня · B2 Q2]`
  - Defend a decision to his design lead **fast**: organises "так, щоб за 10 секунд можна було
    знайти приклад для аргументації своєї думки перед дизайн лідом" `[INT · Даня · B2 Q5]`
- **Pains**
  - **Cannot re-find his own saves.** Asked whether it happens: "Постійно! Пам'ятаю, що бачив
    круту анімацію меню, а де вона… чи в закладках браузера, чи в обраних тг або в Pinterest -
    фіг знає. Злюся, витрачаю час на повторний пошук" `[INT · Даня · B2 Q9]`. And: "90% моїх
    збережень це мертвий груз." `[INT · Даня · B3 Q3]`
  - **Beautiful work that is not real work.** "славнозвісний dribbble-дизайн. Це коли картинка
    візуально виглядає круто, але її неможливо реалізувати кодом або вона неюзабельна. Ти
    витрачаєш час на сміття, яке гарне, але пусте всередині." `[INT · Даня · B3 Q1]` — the brief's
    third problem, in a respondent's own words, unprompted.
  - **Folders stop working past a certain size:** "так як я все організовую по папкам то більш
    менш зручно, але не тоді коли в цій папці купа кейсів. Тоді вже звісно хочеться пошуком
    скористатись." `[INT · Даня · B2 Q8]`
  - **Time sink:** "та сама кроляча нора pinterest. Зайшов за іконкою, а через годину розглядаєш
    дизайн інтер'єрів у Скандинавії." `[INT · Даня · B3 Q2]`
  - **No tool fits:** tried Eagle, Savee, Notion. "Eagle крутий, але він десктопний, **а я часто
    шукаю з телефону в дорозі**. Notion занадто повільний для картинок. Ідеального інструменту
    поки не знайшов." `[INT · Даня · B3 Q4]` — see the contradiction note below.
- **Trust triggers**
  - **Convinces:** proof the thing shipped. "Mobbin мій фаворит, там реальні скріншоти працюючих
    аппок, а не просто картинки для лайків" `[INT · Даня · B1 Q5]`; "Не концепти, а живі додатки"
    `[INT · Даня · B2 Q1]`. Also: being able to picture it running — "коли він виглядає зрозуміло
    і логічно, і я можу уявити як це працює в реальному продукті" `[INT · Даня · B4 Q2]`.
  - **Scares off:** the unbuildable pretty picture, quoted under Pains `[INT · Даня · B3 Q1]`.
    Whether a *breakdown written by another designer* would be trusted, or suspected of being
    flattering to its author, is `[?]` — **hypothesis:** a source link to the live product does
    the trusting, and the breakdown is believed only as far as that link holds.
- **Quote**
  > "Корисний той реф, який можна вкрасти як митець." `[INT · Даня · B4 Q1]`

## Persona 2 — «Та, хто збирає концепт із фрагментів»  ·  secondary

**Why not primary:** she does not have the brief's problems. Asked what annoys her most in
searching, she says there is nothing: "Напевно ні… Зараз ні, бо я настільки звикла до цього
інструменту, настільки знаю що мені знайти що цього не буває" `[INT · Валя · B3 Q1]`. Asked
whether she loses her own saves: "Та ні, а навіть якщо і було то я швидко перемикалась і шукала
щось інше" `[INT · Валя · B2 Q9]`. She is satisfied with her tools: "мені вистачає пінтерест і
всього функціоналу, що він надає" `[INT · Валя · B3 Q4]`. Designing for her means designing
against a non-problem. She is kept in the set because she shares one strong job with Persona 1 —
client alignment — and because she is the closest thing we have to the user this product would
**fail** to attract.

- **Context** — graphic designer, six years including study, now across studios and companies
  `[INT · Валя · B1 Q1]`. Works fast and by reuse: "Мій девіз 'крадійка-художниця'. Ти постійно
  працюєш в швидкому темпі тому не маєш багато часу." `[INT · Валя · B1 Q2]`
- **Jobs**
  - Assemble a concept out of fragments: "ти береш частину тут, частину тут, шматок цієї
    інфографіки, шматок там і виходить така спільна картина де все круто" `[INT · Валя · B1 Q2]`
  - Reach a shared picture with the client: "референс дуже спрощує комунікацію з клієнтом… часто
    люди приходять з запитом 'візьми зроби'… а референсами можна досягти спільного бачення ідеї"
    `[INT · Валя · B1 Q2]`
  - Build up her eye over time — saving is memory, not storage: "треба зберегти щоб воно
    закріпилось в пам'яті, сформувалось в сукупну картина і потім при роботі я собі буває щось
    згадую і влучно можу застосувати" `[INT · Валя · B3 Q3]`
  - Work a board **together with a colleague**: "Особливо подобається коли працюю з таким зумером
    як я і ми разом збираємо ці дошки, кожен додає референси і все так разом. це дуже круто."
    `[INT · Валя · B2 Q5]` — the only mention of collaboration in the whole transcript.
- **Pains**
  - Losing her own direction after a long search: "Так, звісно, дуже часто… було відчуття що
    зовсім не туди пішла і треба починати спочатку" `[INT · Валя · B4 Q4]`
  - Time lost not to missing references but to wrong ones: "час втрачаю більше не через нестачу
    референсів, а через те що ну це не те що я хочу" `[INT · Валя · B3 Q2]`
  - **She reports no search pain and no retrieval pain at all** — quoted above. This is the
    finding, not an omission.
- **Trust triggers**
  - **Convinces:** a reference that shows how to keep beauty and function together — "показує як
    досягти щоб було і гарно, але при цьому зберігало функціональність і читабельність, легкість
    сприйняття" `[INT · Валя · B4 Q1]`. And other people: "Я показую близьким, і я показую своїм
    колегам, питаю їх думку" `[INT · Валя · B4 Q2]`.
  - **Scares off:** `[?]` — never asked and never volunteered. **Hypothesis:** friction at entry.
    Her whole account is built on speed and one habitual tool; a product asking her to fill fields
    before she can look would lose her at the first screen.
- **Quote**
  > "Мій девіз 'крадійка-художниця'." `[INT · Валя · B1 Q2]`

## Persona 3 — «Автор, який розбирає власну роботу»  ·  secondary · **entirely `[?]`**

**Why this persona exists with no evidence:** the brief names the author as the secondary user
and the product cannot exist without them — "the author, who publishes their **own work** and
writes its breakdown". **The interview contains nothing about this person**, because its script
never asks about publishing. Every block below is a hypothesis. It is written out rather than
omitted so the gap is impossible to miss.

- **Context:** `[?]` — **hypothesis:** the same designer as Persona 1, on the other side of the
  transaction, at the moment a project ships and is about to become portfolio material.
- **Jobs:** `[?]`, **but no longer evidence-free — updated 2026-08-07.** **Hypothesis:** to have
  credible proof of craft. The brief's own wording: "reputation — a breakdown is stronger proof of
  craft than a shot". Two market findings now stand behind it, and neither closes it:
  - **A practitioner states the payoff in exactly those terms.** Type designer David Jonathan Ross,
    soliciting submissions: social posts "fade away after a few days", whereas an entry is "a
    **lasting record**… also a way to bring a few **extra eyeballs to your work**"
    `[RES · Re-research · Q1]`, `research/screens/djr-fontsinuse-submissions.png`. **Why the `[?]`
    survives:** he is asking for *a use*, not a breakdown, and as a foundry owner he benefits from
    the submission. It is the right motive from the wrong mouth.
  - **Behance authors hand-draw structured credit tables** in free text because the platform gives
    them no fields `[RES · COMPETITORS · Behance]` — an appetite for structure, inferred from one
    screenshot. Adjacent evidence, not evidence.
  - **A mechanic nobody in the benchmark had:** on Fonts In Use the *beneficiary* of the metadata
    subsidises the contributor — DJR gives a free font issue per submitted use, two if the font had
    no prior uses. **For Loupe there is no identified equivalent beneficiary — `[?]`.**
- **Pains:** `[?]` — **hypothesis:** writing a breakdown competes with the next paid project. The
  benchmark says this is only solved when the structured entry is the price of something they
  wanted anyway `[RES · BENCHMARK · Discogs, criterion 5]`.
- **Trust triggers:** `[?]` — both halves unknown. **Hypothesis:** they are convinced by seeing
  their breakdown drive traffic to their own work, and scared off by the breakdown being reused
  without attribution.
- **Quote:** `[?]` — **no verbatim line exists for this person.** Nothing is composed to fill the
  slot.

---

## Merged personas

None. Валя and Даня were tested for merging and are **not** one persona: they differ in the two
things the template asks about. Different jobs — she assembles a concept out of fragments
`[INT · Валя · B1 Q2]`, he retrieves a solution to a named component `[INT · Даня · B1 Q6]`.
Different pains — he cannot re-find his saves and says so with feeling `[INT · Даня · B2 Q9]`,
she reports the same pain does not exist for her `[INT · Валя · B2 Q9]`. They share exactly one
job, client alignment, which is why that job is the most strongly evidenced in the whole set.

---

## Contradiction with the brief — resolved 2026-08-07, spec updated

**What it was.** `CLAUDE.md` → Brief → Platform read "**Mobile**: browsing and saving to a
collection, nothing else." The interview said the opposite: "Eagle крутий, але він десктопний,
**а я часто шукаю з телефону в дорозі**." `[INT · Даня · B3 Q4]` — the primary persona **rejected
a tool for not letting him search on a phone**. Searching, not browsing.

**Resolution.** Routed to the designer under constitution rule 12; they chose **option 1 — update
the spec**, narrowly. The brief now gives the phone **search, opening a work, reading its
breakdown, and saving**. Authoring — writing the breakdown, upload — and heavy side-by-side facet
comparison stay desktop. Logged in `.design/decisions.md` (2026-08-07).

**What stays open.** Whether the phone also needs the **full facet filter** is `[?]`, carried to
phase 8: the evidence is one respondent and one sentence, and it does not distinguish *finding*
from *filtering*.

---

## What we do not know about people

Specific enough to research in step 6.

1. **Would either respondent publish their own work with a breakdown, and for what?** Never asked
   `[INT · Goal]`. This is the project's main risk and the largest gap in the file.
2. **How much time is an author willing to spend on one breakdown before abandoning it?** No data.
3. **Does a designer trust a breakdown written by another designer**, or discount it as flattering
   to its author? No data; bears directly on whether the "why" field is read or skipped.
4. **Does Persona 1 need the full facet filter on mobile, or only finding and reading?** One
   sentence, ambiguous `[INT · Даня · B3 Q4]`. The narrower half is now settled — the phone
   searches, opens, reads and saves (brief updated 2026-08-07) — so what remains open is filtering
   specifically, and it belongs to **phase 8**.
5. **Would a visible completeness state attract or deter an author?** No data. The brief makes it
   an axis of ranking, so this drives real UI.
6. **Does Persona 2 care about construction values at all?** She never once mentions colour, type
   or grid as things she looks up — but she was never asked. Unknown whether irrelevant or merely
   unprompted.
7. **Does the "argue to the design lead in 10 seconds" job generalise** beyond one respondent in
   an outsourcing studio `[INT · Даня · B2 Q5]`?
8. **Is client alignment a job this product should serve at all?** It is the best-evidenced job in
   the interview and it is absent from the brief entirely.

---

## Self-critique — confirmed / hypothesis / invented

Run 2026-08-07 over `people/personas.md` and `people/jtbd.md`. `impeccable` is `active` but
`.design/memory/toolbox.md` scopes it to the quality pass of **phases 4–10**, and
`.design/prompts/critique.md` is a per-screen pass; phase 2 has no screens. So this is the
step-5 procedure itself: classify, extract what is dangerous, ask three questions.

**Verdict of the pass: two real defects, both of them the same error** — an argument from
silence written up as if it were a source. Rows 14 and 20.

| # | Statement | Where it lives | Verdict | Source or the gap |
|---|---|---|---|---|
| 1 | P1 enters by component name, not by property | `personas.md` P1 · jobs; `jtbd.md` R1 | **confirmed** | `[INT · Даня · B1 Q6]`, verbatim. Closes `[RES]` H7. |
| 2 | P1 cannot re-find his own saves and it costs him time | `personas.md` P1 · pains; `jtbd.md` R3 | **confirmed** | `[INT · Даня · B2 Q9, B3 Q3, B2 Q8]`, three separate answers. |
| 3 | P1 rejects visually strong work that could not ship | `personas.md` P1 · pains; `jtbd.md` R2 | **confirmed** | `[INT · Даня · B3 Q1]`, unprompted. |
| 4 | P1 trusts screenshots of shipped products | `personas.md` P1 · trust; `jtbd.md` R2 | **confirmed** | `[INT · Даня · B1 Q5, B2 Q1]`. |
| 5 | P1 works structure-first, style-second | `personas.md` P1 · context | **confirmed** | `[INT · Даня · B4 Q3]`. |
| 6 | P2 has no search pain and no retrieval pain | `personas.md` P2 · pains | **confirmed** | `[INT · Валя · B3 Q1, B2 Q9, B3 Q4]`, asked directly three ways. |
| 7 | P2 works with a colleague on shared boards | `personas.md` P2 · jobs; `jtbd.md` S3 | **confirmed** | `[INT · Валя · B2 Q5]`. |
| 8 | Client alignment is held by both respondents | `jtbd.md` R4, S2 | **confirmed** | `[INT · Даня · B1 Q2, B2 Q2]` + `[INT · Валя · B1 Q2]`. The strongest evidence in the file. |
| 9 | P1 is the primary persona | `personas.md` P1 · header | **hypothesis** | The *match to the brief* is checkable and it holds. But it is a choice made over **n = 2**, one of whom is a graphic designer. If a third respondent looked like Валя, the choice would be a coin toss. Stated as a decision, not as a finding. |
| 10 | Persona 3 in every block | `personas.md` P3 | **hypothesis**, declared | The interview never asks about publishing `[INT · Goal]`. Already written as such. |
| 11 | Behance authors hand-draw credit tables | `personas.md` P3 · jobs | **confirmed** | `research/screens/behance-project-detail.png` — the observation itself. |
| 12 | …therefore authors *want* to present work in a structured way | `personas.md` P3 · jobs | **hypothesis** | An inference from one screenshot. The file already calls it "adjacent evidence, not evidence" — kept, because it is load-bearing for HJ1. |
| 13 | A source link to the live product is what makes a breakdown believable | `personas.md` P1 · trust | **hypothesis**, declared | Nobody was asked. Drives R2's whole feature. |
| 14 | **P2 scores 1 on R1 — "works by theme and fragment, never names a component"** | `jtbd.md` matrix, R1 · P2 | **invented** | **Argument from silence.** She was never asked what she enters by; the cell reads her *not mentioning* components as evidence that she does not use them. A `1` with a citation attached is worse than a `[?]` — it looks measured. **Must become `[?]`.** |
| 15 | Main job — build from reasons rather than by eye | `jtbd.md` main | **confirmed** | `[INT · Даня · B1 Q3, B4 Q1, B4 Q3]`. |
| 16 | Intent is the part a machine cannot supply (H1) | `jtbd.md` main · note; MVP core 1 | **hypothesis** | Two independent supports — `[RES · CONCLUSIONS · H1]` (a market inference) and Даня's "з певною ціллю" `[B4 Q1]` (one clause of one sentence). For the **first job of the MVP core**, that is thin. See the dangerous subset. |
| 17 | R5 — defending a decision to a lead in ten seconds | `jtbd.md` R5 | **confirmed for P1**, **hypothesis as a general job** | `[INT · Даня · B2 Q5]`, n = 1, in an outsourcing studio. Gap 7 of this file. |
| 18 | E1, E2, E3 as *emotional* jobs | `jtbd.md` emotional | **confirmed** as statements, **hypothesis** as classification | Every quote is verbatim; calling them emotional rather than functional is my reading. Low risk — it changes emphasis, not scope. |
| 19 | S1 — "wants to be read by the lead as grounded" | `jtbd.md` S1 | **hypothesis** | Даня said he wants to *find an argument fast* `[B2 Q5]`. That he wants to be *seen a certain way* is my interpretation of his motive. Plausible, unstated. |
| 20 | **S2 — "wants to be legible to the client as someone who understood"** | `jtbd.md` S2 | **invented** | Same error as row 14, one step further. Both respondents describe a *practical* mechanism — a reference makes agreement possible. Neither says anything about how they wish to be **perceived**. The social framing is entirely mine. **Must be re-labelled or marked.** |
| 21 | No product makes a saved item's construction searchable (R3 · COMPETITORS) | `jtbd.md` matrix | **hypothesis** | Checked against the twelve products in `research.md` — but **Eagle, the tool the primary persona actually named and rejected `[INT · Даня · B3 Q4]`, is not in `research.md` at all.** The claim is unchecked against the one competitor the evidence points at. |
| 22 | Likes / follow-an-author close no job | `jtbd.md` cut list | **confirmed** | Read off the matrix; supported by `[RES · COMPETITORS · diff 3]` and `[RES · PATTERNS · 5]`. |
| 23 | HJ1–HJ5 | `jtbd.md` hypotheses | **hypothesis**, declared | Correctly quarantined. |

### The dangerous subset — drives design, stands on `[?]` or on invention

Ordered by what it would cost to be wrong.

1. **The supply side entirely** (P3, HJ1, HJ2). If no designer will write a breakdown, there is no
   corpus and nothing else in this file matters. `[?]` with zero evidence.
2. **Intent is what the reader actually wants** (row 16). This is **MVP core job 1**, just signed
   off. It rests on one clause from one respondent plus a market inference. If readers only want
   the values, Refero Styles already wins.
3. **Is a self-authored explanation believed?** (row 13, HJ3.) Decides whether intent is read or
   skipped — i.e. whether core job 1 pays off even if authors do write it.
4. **"P2 is not our user"** (rows 6, 14). It is the justification for cutting likes and follow. Row
   6 is solid; row 14 is invented and props it up unnecessarily.
5. **Eagle is unexamined** (row 21). The primary persona named a tool, said why he rejected it, and
   we never looked at it.

### Three targeted questions

| # | Question | It closes | Where the answer is |
|---|---|---|---|
| **Q1** | Do designers write structured breakdowns of **their own** work for free, and what do they say they get back for it? | Dangerous 1 — the whole supply side | Fonts In Use contributor and about pages; Behance / Read.cv case studies that carry hand-built structure; designer threads on why they write case studies |
| **Q2** | When a designer reads another designer's account of their own work, do they believe it — or discount it as flattering? | Dangerous 2 and 3 — whether intent is read at all | Discussion threads under design case studies; writing about what makes a case study credible |
| **Q3** | What is **Eagle** and what exactly does its search do? | Dangerous 5 — and it directly tests R3's "nobody does this" | `eagle.cool` — the product the primary persona named and rejected `[INT · Даня · B3 Q4]` |

---

## After re-research

Step 6, 2026-08-07. Three questions asked, **two produced findings and one produced a null result**,
recorded as such. Full evidence: `research/research.md` → **Re-research after personas**. Two new
captures: `research/screens/djr-fontsinuse-submissions.png`,
`research/screens/eagle-search-filters.png`.

| What changed | Persona · block | Because of | `[?]` dropped? |
|---|---|---|---|
| The reputation motive gained its first real evidence — "a lasting record… a way to bring a few extra eyeballs to your work" | **P3 · jobs** | Q1 — David Jonathan Ross's submission page, `djr-fontsinuse-submissions.png` | **No.** He solicits *a use*, not a breakdown, and benefits from the submission. Narrowed, not closed. |
| A new supply mechanic recorded: the *beneficiary* of the metadata pays the contributor (a free font issue per use, two for a font with no prior uses) | **P3 · jobs**, new bullet | Q1 — same source; this mechanic appears nowhere in the BENCHMARK | **No — it opens one.** Loupe has no identified equivalent beneficiary. |
| **Fonts In Use moderates before publication** — the form shows "Submit for approval" and "Status: private draft (awaiting moderation)" | **not a persona change** — it lands on the brief's `[?]` 6 and on `[RES]` H5 | Q1 — the same capture, read rather than assumed | **No — it contradicts an assumption.** The one product running on hand-written breakdowns does not hold quality without moderation; it has a moderator. Phase 3 must answer this. |
| The optional, progressive "why" is confirmed by the shipping analogue: image + title required, description explicitly optional | **not a persona change** — it corroborates the MVP gate of 2026-08-07 | Q1 | **n/a** — decision and evidence agreed independently. |
| **Eagle entered the evidence base.** Desktop-only, no mobile or web; searches by keyword, colour, tag, folder, rating, format and by image | **P1 · pains** — his rejection of Eagle is now verified, not taken on trust | Q3 — `eagle-search-filters.png`, [en.eagle.cool](https://en.eagle.cool/) | **No, but it corrected a claim:** `jtbd.md` R3 no longer says "nobody makes saved items searchable". |
| **Nothing found** on whether a self-authored explanation is believed | **P1 · trust triggers**; `jtbd.md` HJ3 | Q2 — two primary sources returned 403; search produced an editorial norm, not designer testimony | **No.** Explicitly a null result, not a gap quietly filled. |

**Gaps 1, 3 and 5 of "What we do not know about people" all survive this pass.** Gap 4 was settled
separately at the platform gate. Nothing was dropped without new data.
