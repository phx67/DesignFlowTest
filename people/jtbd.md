<!-- filled by /dsf:users — start from this skeleton, do not restructure it -->

# Jobs to be done

Every job is written as **"When [situation], I want [motivation], so that [outcome]"**, and
every job names the persona it belongs to and the research data it grew out of.

**If a feature name appears inside "I want", it is not a job — it is a feature.** Rewrite it as
human progress. A job backed by nothing goes to the **Hypotheses** section, not the main list.

Personas are referenced as **P1** (Даня — primary), **P2** (Валя), **P3** (the author — entirely
`[?]`). Sources: `[INT · name · Block N Q M]` = `sources/Interview Script
30e58b052da9800b8138cae64003069a.html`; `[RES · section]` = `research/research.md`.

---

## Main job — exactly one

**When** I have a specific component to design and no confidence that my own guess at how to
build it is right, **I want** to see how people who already solved that same thing made their
decisions and why they made them, **so that** I can build my own version from reasons instead of
from eyeballing a picture.

- Persona: **P1** — and this is the brief's primary user, matched item for item.
- Source: "малюю кнопку чи картку товару - йду дивитися, як це реалізовано в топових продуктах"
  `[INT · Даня · B1 Q3]`; "Мені важливо зрозуміти як інші вирішують цю ж задачу, які патерни
  працюють" `[INT · Даня · B4 Q3]`; and the outcome half verbatim: "можливість його
  деконструювати… тут вони використали такий інтерліньяж і таку тінь, щоб створити об'єм **з
  певною ціллю**" `[INT · Даня · B4 Q1]`.

**Why the "why" is inside the main job and not a related one.** `[RES · CONCLUSIONS]` H1 says the
values are table stakes — Refero Styles already generates roles, scale and radii for 2,000+ sites
automatically — and intent is the only part a machine cannot extract. The interview independently
puts "з певною ціллю" in the same sentence as the deconstruction. Two separate sources, one
conclusion.

> **Gate refinement, 2026-08-07 — read this before designing anything for intent.** Intent is a
> **value and a job — the reader comes away understanding *why*** — and **not a mandatory field**.
> It is carried **through the material of the work itself** (the case), and it is **easy, optional
> and progressive**. **No compulsory "justify your choice" form exists anywhere in this product.**
> What form intent takes and how much weight it carries is `[?]`, owned by **phase 3**. Recorded
> in `.design/decisions.md`.

## Related jobs — 3 to 5, on the way to the main one

| # | When… I want… so that… | Persona | Source |
|---|---|---|---|
| R1 | **When** the thing I have to build already has a name — a sign-up screen, a cart — **I want** to get straight to other people's versions of that same named thing, **so that** I don't spend the first ten minutes describing something I can already name. | P1 | "Mobbin зручний тим, що там є патерни: можна відфільтрувати суто «екран реєстрації» або «кошик»" `[INT · Даня · B1 Q6]`. Confirms `[RES · CONCLUSIONS]` **H7**, which until this interview had no artifact. |
| R2 | **When** something looks like the answer, **I want** to know it actually shipped and survived contact with real users before I commit time to it, **so that** I don't rebuild something that was never buildable. | P1 | "Mobbin мій фаворит, там реальні скріншоти працюючих аппок, а не просто картинки для лайків" `[INT · Даня · B1 Q5]`; "Не концепти, а живі додатки" `[INT · Даня · B2 Q1]`; the failure it guards against, unprompted: "славнозвісний dribbble-дизайн… гарне, але пусте всередині" `[INT · Даня · B3 Q1]`. Market side: `[RES · COMPETITORS]` three real differences, item 3. |
| R3 | **When** I know I have seen the solution before, **I want** to arrive back at it without a hunt, **so that** the time I spent finding it the first time isn't spent twice. | P1 · **not P2** | "Постійно! Пам'ятаю, що бачив круту анімацію меню, а де вона… фіг знає. Злюся, витрачаю час на повторний пошук" `[INT · Даня · B2 Q9]`; "90% моїх збережень це мертвий груз" `[INT · Даня · B3 Q3]`; scale limit: "не тоді коли в цій папці купа кейсів" `[INT · Даня · B2 Q8]`. P2 explicitly denies this job: "Та ні" `[INT · Валя · B2 Q9]`. |
| R4 | **When** a client and I are using the same word for two different pictures, **I want** to put something concrete between us early, **so that** we walk into the mockup already agreeing on the direction. | P1 **and** P2 — the only job both hold | "це фундамент для співпорозуміння з клієнтом" `[INT · Даня · B1 Q2]`; "Зібрав мудборд прямо там, скинув клієнту на погодження. Він затвердив" `[INT · Даня · B2 Q2]`; "референсами можна досягти спільного бачення ідеї" `[INT · Валя · B1 Q2]`. |
| R5 | **When** my lead questions a decision I have already made, **I want** the reasoning behind it to become obvious to them in seconds, **so that** the conversation is about the work rather than about whether I am to be trusted. | P1 | organises saves "так, щоб за 10 секунд можна було знайти приклад для аргументації своєї думки перед дизайн лідом" `[INT · Даня · B2 Q5]`. |

**R4 is the best-evidenced job in the whole set and the brief does not contain it.** Two of two
respondents raised client alignment unprompted, in different words, in the first block. It is
flagged here, carried into the matrix, and put to the designer at the MVP gate rather than
quietly serving as a justification for scope.

## Emotional jobs

<!-- how the person wants to feel; listed separately from functional jobs -->

| # | Job | Persona | Source |
|---|---|---|---|
| E1 | To come out of a search feeling the time bought something, instead of feeling robbed by it. | P1 | "Ти витрачаєш час на сміття, яке гарне, але пусте всередині" `[INT · Даня · B3 Q1]`; "та сама кроляча нора pinterest. Зайшов за іконкою, а через годину розглядаєш дизайн інтер'єрів у Скандинавії" `[INT · Даня · B3 Q2]`. |
| E2 | To feel that saving something is making the eye better, not making the folder bigger. | P2 | "треба зберегти щоб воно закріпилось в пам'яті, сформувалось в сукупну картина і потім при роботі я собі буває щось згадую і влучно можу застосувати" `[INT · Валя · B3 Q3]`. Read against P1's "90% мертвий груз" `[INT · Даня · B3 Q3]`, this is the same act producing opposite feelings. |
| E3 | To stay oriented while looking, instead of surfacing an hour later having lost the thread. | P2 (stated) · P1 (adjacent) | "було відчуття що зовсім не туди пішла і треба починати спочатку" `[INT · Валя · B4 Q4]`; "час втрачаю більше не через нестачу референсів, а через те що ну це не те що я хочу" `[INT · Валя · B3 Q2]`. |

## Social jobs

<!-- how the person wants to be seen by others -->

| # | Job | Persona | Source |
|---|---|---|---|
| S1 | To be read by the lead as a designer whose decisions have grounds, not preferences. | P1 | The ten-second argument is organised *for an audience of one specific person* `[INT · Даня · B2 Q5]`. **The audience is confirmed; the wish to be *seen* a certain way is my reading of his motive, not his words** (self-critique row 19). |
| S2 | `[?]` — **withdrawn as a social job, 2026-08-07.** It read "to be legible to a client as someone who understood the request rather than guessed at it". Both respondents describe a **practical mechanism** — a reference makes agreement possible — and **neither says anything about how they wish to be perceived**. The social framing was mine (self-critique row 20). The functional job survives untouched as **R4**. | — | "фундамент для співпорозуміння" `[INT · Даня · B1 Q2]`; "часто люди приходять з запитом 'візьми зроби'" `[INT · Валя · B1 Q2]` — both support R4, neither supports a social job. |
| S3 | To do the looking-and-collecting *with* peers rather than alone. | P2 only | "Особливо подобається коли працюю з таким зумером як я і ми разом збираємо ці дошки, кожен додає референси і все так разом" `[INT · Валя · B2 Q5]` — the only mention of collaboration in the entire transcript, and it belongs to the persona the product is **not** built for. |

## Hypotheses

<!-- jobs that sound right but have no data behind them. They stay here until data arrives. -->

**Every job of P3 lives here.** The interview never asks about publishing `[INT · Goal]`, so the
supply side of this product has no evidenced job at all. This is the project's main risk, kept
visible rather than promoted into the tables above.

| # | Job | What would confirm it | Where to look |
|---|---|---|---|
| HJ1 | **When** a project of mine ships, **I want** proof of my craft that survives inspection, **so that** the work argues for me when I am not in the room. (P3) | A designer stating, unprompted, that a shot alone under-represents their work — and that they have written a breakdown for free to fix that. | Behance project pages where authors hand-build structure the platform does not give them `[RES · COMPETITORS · Behance]`; Medium/Substack design case studies; Fonts In Use contributor pages. |
| HJ2 | **When** I would have to build a case-study page by hand anyway, **I want** that page to fall out of the act of describing the work once, **so that** I pay the cost once instead of twice. (P3) | Evidence that designers rebuild the same breakdown separately for a portfolio. This is `[RES]` **H2** and the Discogs criterion-5 mechanic, untested on designers. **Weakened 2026-08-07:** extraction pre-fills most of the page, so "the cost" the author avoids is now small — and a payback that costs nothing buys no intent. | Portfolio-building threads; the structure of existing Behance/Read.cv case studies. |
| HJ3 | **When** I read someone else's account of their own work, **I want** to be able to tell craft from flattery, **so that** I copy a decision rather than a boast. (P1, reading side) | A designer saying they discount self-authored explanations, or that a live source link is what makes them believe one. | Designer forums; comments under case studies; a targeted question in step 6. |
| HJ4 | **When** I am assembling a look, **I want** the construction values, not just the picture. (P2) | P2 naming colour, type or spacing as something she looks up. She never does — but she was never asked `[INT · Валя]`, gap 6 of `personas.md`. | A follow-up question; graphic-designer communities as a proxy. |
| HJ5 | **When** my entry is visibly incomplete, **I want** that to read as work in progress rather than as low quality, **so that** publishing early does not cost me standing. (P3) | Evidence that a visible completeness state attracts rather than deters. `[RES]` **H4** makes incompleteness cost reach; nobody has checked how an author feels about that. | Discogs "Needs Vote" discussions; Wikipedia stub-tag debates; a targeted question in step 6. |

---

## Matrix — jobs × personas × features

Cell for a persona column: importance **1–3** · what shows it. Unknown importance is `[?]`, never
an averaged number. **P3's column is almost entirely `[?]` and that is the finding** — the
interview never asks about publishing `[INT · Goal]`, so the supply side has no measured
importance for any job.

| Job | P1 (Даня) | P2 (Валя) | P3 (author) | FEATURE — what closes this job | COMPETITORS — already closed? |
|---|---|---|---|---|---|
| **Main** — build from reasons, not by eye | **3** · `[INT · Даня · B1 Q3, B4 Q1, B4 Q3]` | `[?]` · construction values never asked (`personas.md` gap 6) | `[?]` | The breakdown travelling with the work: **extracted values the author confirms** (changed 2026-08-07) **plus the author's intent**, intent carried through the case material itself | **partly** — Refero Styles auto-generates the values for 2,000+ sites (`refero-style-breakdown.png`); **nobody carries the intent** `[RES · CONCLUSIONS · H1]` |
| **R1** — enter by the name of the task | **3** · `[INT · Даня · B1 Q6]` | `[?]` · **never asked what she enters by.** Corrected 2026-08-07: this cell read `1`, argued from her not mentioning components — an argument from silence dressed as a score (self-critique row 14). What would settle it: ask her. | `[?]` | Task taxonomy as the entry, facets refining inside it | **yes** — Mobbin (`mobbin-landing-gated.png`) and Refero (`refero-home.png`); Mobbin additionally paywalls it (`mobbin-pricing.png`) |
| **R2** — know it is real without opening it | **3** · `[INT · Даня · B1 Q5, B2 Q1, B3 Q1]` | `[?]` · never mentions realness | `[?]` | Reality status on the card + a link to the live product | **no** — Mobbin guarantees it by sourcing rather than declaring it; Dribbble's studied shot admits "concept" in its fourth paragraph `[RES · COMPETITORS · diff 3]` |
| **R3** — get back to what I already found | **3** · `[INT · Даня · B2 Q9, B3 Q3, B2 Q8]` | **1** · explicitly denies the pain `[INT · Валя · B2 Q9]` | `[?]` | Collections whose contents stay searchable by the breakdown fields | **partly, and narrower than first claimed.** Corrected 2026-08-07 (self-critique row 21): **Eagle already searches a saved library by colour, tag, rating, format and by image** — it is desktop-only, which is exactly why the primary persona rejected it `[RES · Re-research · Q3]`, `eagle-search-filters.png`. What no product does is make **a public pool searchable by properties its authors declared**, reachable on a phone. Are.na caps the free tier at 200 blocks |
| **R4** — one shared picture with the client | **3** · `[INT · Даня · B1 Q2, B2 Q2]` | **3** · `[INT · Валя · B1 Q2]` | **`[?]` — nothing in the brief.** Carried to phase 3: does "a collection you can show a non-designer" fall out of the collections we already have, almost for free? | **partly** — Savee boards, Are.na channels and Pinterest serve it incidentally, none by design |
| **R5** — defend a decision fast | **3** · `[INT · Даня · B2 Q5]` | `[?]` · no lead appears in her account | `[?]` | Same feature as Main — the intent, in quotable form | **no** — Awwwards publishes jury *scores*, not reasons `[RES · COMPETITORS · Awwwards]` |
| **E1** — the time bought something | **3** · `[INT · Даня · B3 Q1, B3 Q2]` | 2 · `[INT · Валя · B3 Q2]` | `[?]` | Few relevant results instead of a feed as the main screen | **no** — market pattern 1: the feed is the default surface (`dribbble-browse.png`, `figma-inspo-feed.png`) |
| **E2** — the eye grows, not the folder | 1 · "90% моїх збережень це мертвий груз" `[INT · Даня · B3 Q3]` | **3** · `[INT · Валя · B3 Q3]` | Collections | **yes** — Pinterest fully satisfies her `[INT · Валя · B3 Q4]` |
| **E3** — stay oriented | 2 · `[INT · Даня · B3 Q2]` | **3** · `[INT · Валя · B4 Q4]` | `[?]` | Entering by a named task bounds the session | **no** — the feed is engineered against it |
| **S1** — read as grounded, not opinionated | **3** · `[INT · Даня · B2 Q5]` | `[?]` | `[?]` | Same feature as Main — the intent | **no** |
| ~~**S2**~~ — withdrawn 2026-08-07 | — | — | — | Withdrawn as a social job (self-critique row 20): the evidence supports a practical mechanism, not a wish to be perceived. **The functional half lives on as R4 and loses nothing** | — |
| **S3** — collect alongside peers | `[?]` · never mentions collaboration | **3** · `[INT · Валя · B2 Q5]` | `[?]` | **none** — the brief contains no collaboration; the social layer is save / like / follow | **yes** — Are.na channels, Savee boards |

**No row and no column is empty.** P3's column is `[?]` throughout, explained above; the two
`[?]` FEATURE cells (R4, S2) are the uncovered-job finding below, not an oversight.

---

## MVP core — three jobs

Signed off at the human gate on **2026-08-07** (`.design/decisions.md`). Read off the matrix:
importance 3 for the primary persona **and** not closed by the market.

1. **Main — build from reasons rather than by eye.** P1 = 3; the market closes **half** of it —
   Refero Styles already generates the values, nobody carries the intent. So what enters the core
   is not "a breakdown" but **the intent inside it**.
   **Bounded at the gate:** intent is a **value and a job, not a mandatory field**; it rides on the
   work's own case material; easy, optional, progressive; **no compulsory "justify it" form**. Its
   form and weight are `[?]` for **phase 3**.
   **Sharpened 2026-08-07 by `/dsf:change`:** the machine now extracts the values and the author
   confirms them, so this job's human half is **entirely** intent. Two follow-ons for phase 3:
   completeness is measured on intent alone (*absent → present → case*), while the extracted values
   carry a **confirmed / unconfirmed** trust state; and the unit may be **one screen or a whole
   case**, so this job must be answerable at both sizes.
2. **R2 — know it is real before opening it.** P1 = 3; market = **no**. This is success criterion 2
   of the brief, stated as a job.
3. **R3 — return to what I already found without a hunt.** P1 = 3; market = **partly** — collections
   are universal, but no product makes the *construction* of a saved item searchable, which is the
   one thing Loupe owns for free.

**Not R1**, despite scoring 3: the matrix shows Mobbin and Refero already close it. It stays the
**entry surface** (H7, now confirmed by `[INT · Даня · B1 Q6]`), but it is not what this product
has to invent.
**Not R5 / S1:** the same feature closes them as closes Main. A second outlet of one job, not a
fourth job.
**Not E1:** a consequence of Main + R1, not a separate thing to build.

## Cut candidates

Accepted at the same gate.

| Feature | Which job it was assumed to close | Why it closes nothing |
|---|---|---|
| **Likes** | "a quality signal" | No row in the matrix. Popularity as a signal is the one thing the market has tested and failed on R2 — Dribbble `[RES · COMPETITORS · diff 3]`. **Cut deliberately, revisit in v2.** |
| **Follow an author** | R3 — returning to what is valuable | `[?]` / low for P1. This is retrieval pattern 5, of which the research says plainly it "fails the primary user outright" `[RES · PATTERNS]`. It serves E2 / S3 — P2's jobs, and P2 is the persona this product is not built for — and P3, who is unevidenced. **Cut deliberately, revisit in v2.** |
| **Column grid as the third breakdown axis** | Main | H3: the most complete construction spec on the market publishes density, base unit, max width and radii, and **never** a column grid `[RES · CONCLUSIONS · H3]`. **Cut accepted, with a standing `[?]`: the third axis must be re-named — base unit / density / spacing rather than a column grid — in phase 3, and carried into the tokens in phase 6.** |
| **A dedicated side-by-side comparison screen** | "cannot compare ten examples of one component" | Demoted back at phase 1; the matrix produces no row that needs it. **Cut** — comparison falls out of the shared fields as a side effect, which is what the phase-1 hypothesis predicted and what no competitor contradicts `[RES · CONCLUSIONS]`. |
| **Tags as a retrieval mechanism** | R1 | R1 is closed by the task taxonomy, not by tags. **Cut as retrieval**; tags remain optional personal context inside your own collections, as the brief already has them. |

---

## The uncovered job — carried to phase 3, not cut

**R4, one shared picture with the client, is the best-evidenced job in the whole set** — 3 for both
respondents, raised unprompted by each of them in the first block — **and the brief does not
contain it.** Its FEATURE cell is empty.

(It was presented at the gate as "R4 + S2". S2 was withdrawn in the step-6 correction as an
unsupported social framing; **the functional job the gate decided about is untouched** — it was
always R4 that carried the evidence.)

Gate decision: **neither cut nor promoted to a fourth core job.** It stays `[?]` for **phase 3**,
where the IA answers one specific question: does "a collection you can show a non-designer" fall
out of the collections the product already has, almost for free? If it does, the job is served
without new scope. If it does not, the decision to leave it unserved becomes explicit.
