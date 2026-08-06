<!-- filled by /dsf:research — start from this skeleton, do not restructure it -->

# Research

Four sections, nothing else: **COMPETITORS · BENCHMARK · PATTERNS · CONCLUSIONS**.
Every factual claim carries a link or a screenshot path from `research/screens/`.
Where no source exists: `[?] unverified` plus the explicit hypothesis. Never round a guess
into a number.

All screenshots were captured by the agent in Chromium at 1440×900 on **2026-08-06**. Where a
product hides its catalogue behind a login, the reachable surface is captured and the row is
labelled `access restricted`.

---

## COMPETITORS

Three groups, **max 5 per group**. Set signed off by the designer at the step-1 gate on
2026-08-06 (`.design/decisions.md`): Fonts In Use raised from Aspirational to Hard as the phase's
main object of study; Land-book dropped to keep Hard at five, its structured-filter lesson being
covered by Mobbin and Refero; market international, no local-market row; Polaris/Material moved
out of the competitor set and kept as a **language reference** (below the matrix).

### Hard — same product, same audience, same market

| Product | Why it belongs here | What specifically to learn from it |
|---|---|---|
| **Fonts In Use** — `fontsinuse.com` | The only shipping product with Loupe's exact mechanic: a work, an author-written structured breakdown, and every field of that breakdown doubling as the search index. Narrower domain (typography only), running since 2010. | Whether a hand-written breakdown survives at scale without moderation, and what makes contributors write one. Read the field set on a use page and the counts beside each value: `research/screens/fontsinuse-use-detail.png` |
| **Dribbble** — `dribbble.com` | The canonical shot gallery: designers publish their own work, likes / follows / collections. The social layer Loupe inherits. | That its whole filter set is Tags + Color + Timeframe, and that Color is machine-extracted and already a live facet at `/shots?color=050504`: `research/screens/dribbble-filters.png`, `research/screens/dribbble-auto-palette.png` |
| **Behance** — `behance.net` | Long-form project case studies by the maker — the closest existing thing to "the author explains their own work". | How much structure authors invent when the platform gives them none: the credits table on the studied project is hand-drawn out of `⎯` characters inside a free-text block. `research/screens/behance-project-detail.png` |
| **Mobbin** — `mobbin.com` | A searchable library of real product screens, browsed by pattern and element — the closest match to Loupe's "task on the desk" behaviour. | That retrieval itself is the paywall: "Filter & search results — Limited" on the Free tier. `research/screens/mobbin-pricing.png` |
| **Savee** — `savee.com` | Saving and discovery for designers; the collection layer Loupe copies. | Its retrieval stack — advanced filters, AI recommendations and **search by image** — a fourth candidate the brief did not list. `research/screens/savee-home.png` |

### Soft — different product, same underlying job

| Product | Why it belongs here | What specifically to learn from it |
|---|---|---|
| **Figma Community** — `figma.com/community` | Construction is fully available: you open the file and read the layers, styles and variables. The limit case of transparency. | That even with total transparency Figma still shipped **Inspo (Beta)** as a trending feed of "riffs" — the feed is the default surface even for the tool vendor. `research/screens/figma-inspo-feed.png` |
| **CodePen** — `codepen.io` | Result and source sit on one screen by default: "a social development environment for front-end designers and developers". | Why it needs no structured fields at all — the artifact is executable, so the breakdown is redundant. Loupe's images cannot be executed, which is the whole reason a breakdown has to exist. `research/screens/codepen-trending.png` |
| **Are.na** — `are.na` | Reference collecting where meaning comes from which channels a block sits in, not from tags. | The alternative to properties: connection as the index. Free tier stops at 200 blocks. `research/screens/arena-home.png` |
| **Awwwards** — `awwwards.com` | Every entry carries a structured jury evaluation, and the site filters by **Font** and **Color** — two of Loupe's three axes, shipping. | The scoring model (Design 40% / Usability 30% / Creativity 20% / Content 10%, minimum 18 jurors, three outlying scores dropped) and the single-select typeface filter. `research/screens/awwwards-font-filter.png`, [about-evaluation](https://www.awwwards.com/about-evaluation/) |

### Aspirational — international benchmarks in the category

| Product | Why it belongs here | What specifically to learn from it |
|---|---|---|
| **Cosmos** — `cosmos.so` | Best-in-class discovery, and the only product that treats provenance as a filter. | Two mechanics: **AI content → Show / Blur / Hide** as a first-class control, and "Cosmos researches images — surfacing the artist, source, and story", i.e. the platform supplies attribution rather than the uploader. `research/screens/cosmos-search-and-ai-filter.png` |
| **Refero** — `refero.design` | The deepest structured taxonomy on the market — Page Types, Flows, UX Patterns, UI Elements, industry — plus a shipping AI "research mode" and an MCP server. | **Refero Styles (Beta)**: "2,000+ AI-readable design systems … colors, typography, spacing, components, and a DESIGN.md". This is Loupe's spine, generated automatically. `research/screens/refero-styles-beta.png`, `research/screens/refero-style-breakdown.png` |
| **Layers** — `layers.to` | Listed at the gate as a community built around writing about craft. **That rationale did not survive verification.** | Kept as a data point, not a benchmark: the live site is a tag rail over a "Hot" shot feed with inline ads, i.e. a Dribbble-shaped entrant. `research/screens/layers-explore.png` |

### Comparison matrix

| Product | Audience | Product core | Key mechanic | Trust | Monetization | Source |
|---|---|---|---|---|---|---|
| **Fonts In Use** | Typographers, designers, type foundries | "A public archive of typography indexed by typeface, format, industry, and period" | Author fills structured fields (Typefaces / Formats / Topics / Designers / Tags / Location); every value is a link with a live count, so the breakdown *is* the index | Per-image source URL + licence line; contributor name and date; artwork publication date; Staff Picks (6,322 of 34,239) as the only quality signal; open comments | Type-foundry sponsorships rotating in the header and in-grid (Typotheque, Frere-Jones Type, DJR, Kilotype observed), plus a Mobbin house ad. No user-facing paid tier seen — `[?] unverified` whether any other revenue exists | [about](https://fontsinuse.com/about), `fontsinuse-home.png`, `fontsinuse-use-detail.png`, `fontsinuse-advanced-search.png` |
| **Dribbble** | Designers publishing work; clients hiring them | Shot gallery + hiring marketplace | Post an image, collect likes and views; discovery by category chips and a three-control filter (Tags, Color, Timeframe) | Likes and view counts; PRO / PRO+ badges; "Available for work"; **no reality status** — the studied shot describes itself as a "concept" only in the fourth paragraph of prose | Pro subscriptions (Lite $4/mo, Standard $8/mo, Plus $99/mo, billed annually), services marketplace, display ads, job listings | `dribbble-browse.png`, `dribbble-filters.png`, `dribbble-shot-detail.png`, [pro](https://dribbble.com/pro) |
| **Behance** | Designers building a portfolio; recruiters | Adobe's portfolio network — long-form project pages | Publish a project as an image sequence with free-text; structured metadata is **Tools**, **Creative Fields** and free tags, plus a publication date | Owner profiles with location, appreciations / views / comments, publication date, "© All Rights Reserved"; tool badges on the card | Behance Pro and Recruiter Pro subscriptions (prices not collected — `[?] unverified`), job posts, asset and freelance-service sales | `behance-search-uiux.png`, `behance-project-detail.png` |
| **Mobbin** | Product designers with a component to design | Curated library of real app and website screens — "Discover real-world design inspiration" | Browse by app, flow, screen and pattern; copy and download screens. Catalogue is **access restricted** without an account | Content is captured from shipped products, so reality is guaranteed by sourcing rather than declared; "Featuring over 1,000 iOS & Web apps, and 200 sites — New content weekly"; logos of Metalab, Figma, Pentagram, Google, Spotify | Free (latest 4 apps/sites, limited flows, **limited filter & search results**, up to 3 collections); Pro €10/member/mo and Team €16/member/mo billed yearly; Enterprise; Finance+ add-on €399/mo | `mobbin-landing-gated.png`, `mobbin-pricing.png` |
| **Savee** | Designers collecting visual references | Personal library over a shared pool — "Browse inspiration curated by designers" | Save from anywhere via extension / mobile / Figma plugin into boards; retrieval by advanced filters, AI recommendations and **search by image** | Community curation and follower counts; "without ads, without an algorithm"; claims "over 1M users" — their own figure, not independently verified | Paid subscription ("Just the people who pay for it"), a template marketplace (80+ assets) and a paid course. Price not collected — `[?] unverified` | `savee-home.png` |
| **Figma Community** | Anyone using Figma | Distribution of openable design files, plugins and kits, plus **Inspo (Beta)**, a trending feed of "riffs" | Duplicate a file into your own workspace and inspect the real layers, styles and variables | Author profile, duplicate counts, likes; the file itself is the proof — nothing is described, everything is inspectable | Free; funnels into Figma seats | `figma-community-home.png`, `figma-inspo-feed.png` |
| **CodePen** | Front-end designers and developers | "A social development environment" — editor plus public gallery | Every Pen ships its HTML / CSS / JS panels beside the rendered result; fork to take it apart | The running code is the trust signal; author profile, follows | Free (unlimited public Pens, 3 files); PRO Starter $8/mo, Developer $12/mo, Super $26/mo (monthly rate; annual $96 / $144 / $312); sponsors and Carbon ads on free | `codepen-trending.png`, [pricing](https://codepen.io/pricing) |
| **Are.na** | "Students, hobbyists and connected knowledge collectors" | "Online software for saving and organizing the content that is important to you"; "playlists, but for ideas" | Blocks connected into channels; a block in several channels is how meaning accrues. No tags, no property filters | No ads and no algorithm, stated as policy; "sustained entirely by our members. The people who use it are our only customers"; independent team of four full-time | Premium $7/mo or $70/yr; Guest free up to 200 total blocks | `arena-home.png` |
| **Awwwards** | Web designers and studios competing for recognition | Juried awards + a filterable directory of winning sites (10,336 listed) | Submit a site, get scored by jury and pro users; browse by Awards, Category, Tag, Technology, Country, **Font**, **Color** | Award badges on the card (SOTD, DEV, Honorable Mention) readable without opening; scores are public: Design 40% / Usability 30% / Creativity 20% / Content 10%, minimum 18 jurors, the three most distant scores dropped, ≥6.5 → Honorable Mention | Paid site submissions, Pro membership, The Creative Pass at €11.50/month, Academy courses, job board, marketplace | `awwwards-websites.png`, `awwwards-font-filter.png`, [about-evaluation](https://www.awwwards.com/about-evaluation/) |
| **Cosmos** | Designers, art directors, creative teams | "Your space for inspiration" — visual discovery and collections | "Search the way you think": by colour (hex), by visual similarity, and with an **AI content** control set to Show / Blur / Hide | "Know what you're looking at. Cosmos researches images — surfacing the artist, source, and story" — the platform supplies attribution; AI-generated content is labelled and filterable | `[?] unverified` — no pricing page reached; app and web sign-up, "Inspiration for the world's top creative teams" | `cosmos-home.png`, `cosmos-search-and-ai-filter.png` |
| **Refero** | Designers, builders "and AI" | Library of real product screens and flows, organised by the deepest taxonomy in the set | Five parallel axes — Page Types, Flows, UX Patterns, UI Elements, industry — plus a natural-language "research mode" and an MCP server for coding agents | Screens are captured from shipped products; each Styles entry links to the live source URL (e.g. `ui.shadcn.com`) | Paid plans (page not collected — `[?] unverified`); MCP and Figma plugin as distribution | `refero-home.png`, `refero-styles-beta.png`, `refero-style-breakdown.png` |
| **Layers** | Designers publishing shots | Shot feed with a long free-tag rail | "Hot" feed filtered by ~30 open tags; card is author + title | Author name only; no source, no status, no construction | Inline sponsored cards ("Streamline · Ad"); rest `[?] unverified` | `layers-explore.png` |

#### Not a competitor — the language reference

Kept per the step-1 gate: studied for **how construction is described**, never scored for attention.

| Reference | What it contributes |
|---|---|
| **Material 3** — colour roles | "There are 26 standard color roles organized into six groups: primary, secondary, tertiary, error, surface, and outline." Colour is named by **role**, not by hex; roles carry an accessibility contract ("accessible minimum 3:1 contrast") and are delivered as tokens. `research/screens/material3-color-roles.png`, [m3.material.io](https://m3.material.io/styles/color/roles) |
| **Shopify Polaris** — type tokens | The opposite naming convention: a numeric scale decoupled from the value — `--p-font-size-350: 14px`, `--p-font-size-400: 16px`, weights `regular 450 / medium 550 / semibold 650 / bold 700`. The value can change without renaming the token. [polaris tokens/font](https://polaris-react.shopify.com/tokens/font) |

**Consequence for Loupe.** A breakdown that lists seven hexes is not reproducible; Refero Styles
already proves the working form — a role name, the hex, and one line on where it is used ("Hairline
`#e5e5e5` — borders, input outlines, card edges, badge outlines"). Loupe's colour field must carry
role + value + usage, and its typography field must carry a named scale with its ratio
("Major Second (1.125) from 16px base"), or criterion 1 of the brief cannot be met.

**Three shared market patterns** — what everyone does the same way:

1. **The feed is the default surface; search is a secondary control.** — evidence:
   `dribbble-browse.png` (opens on Popular, eight category chips, filters collapsed behind a
   button) and `figma-inspo-feed.png` (Figma's new Inspo is a Trending feed of "riffs"), with
   `layers-explore.png` as a third.
2. **Construction metadata exists, and it is machine-extracted rather than authored.** — evidence:
   `dribbble-auto-palette.png` (palette pulled from the image, each swatch a live facet at
   `/shots?color=050504`) and `refero-style-breakdown.png` (full colour roles, type scale, spacing
   and radii generated from a live site), with Cosmos's colour and visual-similarity search as a
   third: `cosmos-search-and-ai-filter.png`.
3. **Retrieval is the paywall.** — evidence: `mobbin-pricing.png` ("Filter & search results —
   Limited" on Free) and `arena-home.png` (free tier capped at 200 blocks), with Dribbble selling
   "search ranking" inside Pro: [dribbble.com/pro](https://dribbble.com/pro).

**Three real differences** — where they genuinely diverge:

1. **Who supplies the metadata.** The author (Fonts In Use: `fontsinuse-use-detail.png`), the
   platform (Cosmos "researches images"; Refero generates a DESIGN.md — `cosmos-home.png`,
   `refero-style-breakdown.png`), or nobody (Layers: `layers-explore.png`).
2. **Whether the work has to be the publisher's own.** Fonts In Use explicitly invites both —
   "contribute **your own work or other typography you admire**" (`fontsinuse-advanced-search.png`);
   Savee saves from anywhere (`savee-home.png`); Mobbin catalogues third-party products without the
   maker (`mobbin-landing-gated.png`); Awwwards requires a paid submission by the maker.
3. **What the at-a-glance trust signal is.** Award badges (Awwwards SOTD/DEV on the card —
   `awwwards-websites.png`), the breakdown itself printed on the card (Fonts In Use shows the
   typeface names under every thumbnail — `fontsinuse-home.png`), or popularity alone (Dribbble's
   likes and views — `dribbble-browse.png`).

**Three open questions** only the product owner can answer:

1. **Refero Styles already delivers Loupe's success criterion 1.** Exact palette with roles and
   usage notes, a named type scale with its ratio, 4px base unit, 1280px max width, radii per
   element — generated automatically for 2,000+ sites, free to browse, with a DESIGN.md to paste
   into an agent. What does a *hand-written* breakdown buy that the generated one does not, and is
   that worth twenty minutes of the author's time?
2. **The brief forbids publishing other people's work. The closest working analogue deliberately
   allows it.** Is "own work only" a rights decision, a quality decision, or a growth ceiling being
   accepted on purpose — and what happens to the pool's size if it holds?
3. **Is the unit a component or a whole work?** The brief's user has "a specific component to
   design — empty state, pricing, onboarding form", but the breakdown fields (palette, type scale,
   grid) describe a whole product. Refero indexes components; Fonts In Use and Refero Styles index
   whole works. Loupe currently claims both.

---

## BENCHMARK

**Dimension:** how a product obtains **unpaid structured work** from its participants, and holds
its quality **without a paid moderation team**.

**Why this one (evidence from the matrix):** the matrix killed the obvious answer. Showing
construction is no longer an empty niche — Refero Styles generates exact colour roles, a named
type scale with its ratio, a 4px base unit and per-element radii for 2,000+ sites automatically
(`research/screens/refero-style-breakdown.png`), and Dribbble already extracts a palette and turns
every swatch into a live search facet (`research/screens/dribbble-auto-palette.png`). What no
competitor has solved is the supply side: of twelve products, exactly **one** runs on breakdowns
written by hand — Fonts In Use, 34,239 entries since 2010, with Staff Picks (6,322) as its only
quality signal (`research/screens/fontsinuse-home.png`). Meanwhile authors visibly *want* structure
they are not given: on the studied Behance project the credits table is drawn out of `⎯` characters
inside a free-text block (`research/screens/behance-project-detail.png`). So the question is not
"can the breakdown be shown" but "why would a person write one by hand when a machine writes it
free" — which is `[?]` 1 of the brief, the one that rebuilds the spine if it fails.

Confirmed at the human gate on 2026-08-06. Reference set named by the designer; five of the six are
scored and OpenStreetMap was cut to stay inside the checklist's "4–5 reference products" — its
mechanisms duplicate Wikipedia's and its motivation is the furthest from the reputation hypothesis.
**All five come from outside this product's category.**

### Criteria — 7, each scored 1–5

| # | Criterion | What a 1 looks like | What a 5 looks like |
|---|---|---|---|
| 1 | **The contribution is structured** | The contributor types prose into one box; nothing they write becomes a field | The contribution is entered as named fields with controlled values, and every value becomes a browsable index entry |
| 2 | **Cost of the first contribution** | More than ten required fields, or an application/approval, before anything can be saved | One required input; everything else is optional and can be added later |
| 3 | **Partial contributions are legitimate** | Incomplete submissions are rejected or held in an invisible queue | An incomplete item is published, its incompleteness is shown to readers, and anyone can fill a missing field afterwards |
| 4 | **Contributor identity accrues** | Contributions are anonymous, or the name appears nowhere a reader looks | Every item names its contributor, and their profile aggregates what they have contributed as a visible count, score or rank |
| 5 | **The contribution pays back into the contributor's own work** | Contributing produces nothing the contributor can use themselves | The act of contributing produces something the contributor needed anyway — a listing they wanted to sell, a page they would have made, a record they keep for themselves |
| 6 | **Quality is regulated by readers, not staff** | A paid or appointed team reviews every submission before it appears | Anything published appears at once; quality is governed by reader-visible signals and reader edits, with the right to judge earned by participation |
| 7 | **Thin entries are marked, not deleted** | Weak entries vanish silently, or sit unmarked and indistinguishable from complete ones | A thin or disputed entry carries a standing, reader-visible marker that also functions as a task: it names what is missing and points at how to supply it |

### Scoring — five products, all from outside the category

| Product | Category | 1 | 2 | 3 | 4 | 5 | 6 | 7 | Total | Source |
|---|---|---|---|---|---|---|---|---|---|---|
| **Discogs** | Music database + marketplace | 5 | 2 | 4 | 3 | 5 | 5 | 5 | **29** | `research/screens/discogs-release.png`; [Voting Guidelines](https://support.discogs.com/hc/en-us/articles/360005055593-Database-Guidelines-20-Voting-Guidelines) |
| **Genius** | Lyrics annotation | 3 | 5 | 5 | 5 | 3 | 4 | 3 | **28** | `research/screens/genius-annotation.png` |
| **Stack Overflow** | Q&A for programmers | 3 | 4 | 2 | 5 | 4 | 5 | 4 | **27** | `research/screens/stackoverflow-reputation.png`; [what is reputation](https://stackoverflow.com/help/whats-reputation) |
| **Wikipedia** | Encyclopedia | 3 | 5 | 5 | 2 | 1 | 5 | 5 | **26** | `research/screens/wikipedia-maintenance-banner.png` |
| **Letterboxd** | Film diary + social | 2 | 5 | 5 | 4 | 5 | 2 | 1 | **24** | `research/screens/letterboxd-film.png` |

Notes on the scores that carry the most weight:

- **Discogs 5 on criterion 5.** The structured fields are not a favour to the database — a seller
  cannot list a record without them. Unpaid structured labour is bought with access to something
  the contributor already wanted.
- **Discogs 5 on criterion 7.** Every release carries a Data Quality state on the page itself
  (`Data Correct` on the studied release; `Needs Vote` and `Needs Major Changes` are the other
  values). Discogs describes a vote as "a quality marker that shows other users 'there is an error
  in that submission, have a look, maybe you can help'".
- **Wikipedia 5 on criterion 7, 1 on criterion 5.** The maintenance banner is the best gap marker
  in the set — reader-visible, dated ("December 2024"), and carrying the means to close it
  ("Find sources: *-logy* — news · newspapers · books · scholar · JSTOR"). And it is the clearest
  proof that a gap marker alone does not need a selfish payoff to work — but Wikipedia also has a
  25-year-old mission that Loupe does not.
- **Stack Overflow 5 on criterion 4.** The only fully numeric identity in the set, with published
  rates: answer upvoted +10, answer accepted +15 (+2 to the acceptor), suggested edit accepted +2,
  downvote −2, capped at 200/day.
- **Genius 5 on criterion 3 and 4.** Unannotated lines are the normal state, so a partial artifact
  is not a failed one; the studied song shows **1063 Contributors** and 12.3M views on the page, and
  artists can "Get Verified" so their own annotations are marked as the author's.
- **Letterboxd 2 on criterion 1.** Members supply a rating, a review and lists; the structured film
  metadata comes from TMDb, not from members — which is why it anchors the low end and is still in
  the set: it proves identity-driven contribution can be huge (7.4M watches on one film) while
  producing almost no structured data.

**Three mechanics worth carrying into the MVP:**

1. **Make the breakdown the price of something the author wants anyway** — from Discogs, because
   its 5 on criterion 5 is the only mechanism in the set that does not depend on goodwill. Concretely
   for Loupe: filling the breakdown is what produces the author's own presentable case-study page,
   the thing they would otherwise have built by hand for a portfolio.
2. **Make `[?]` a dated, actionable marker, not an empty cell** — from Wikipedia, because its gap
   banner names what is missing, when it went missing, and where to get it. Loupe's `[?]` should
   name the field, carry a date, and put the one control that fills it inside the marker.
3. **Earn the right to judge by participating** — from Discogs and Stack Overflow, because both hold
   quality with no paid reviewer by granting the marking privilege only to people the system has
   already watched contribute. This is the answer to the brief's `[?]` on moderation: not staff
   review, not nothing, but a reader-visible quality state that only earned readers can set.

**One that will not work here:** **a numeric reputation score as the primary motivator**
(Stack Overflow) — because Stack Overflow's points are earned by answering *someone else's* public
question, so the score measures service against a queue that already exists. Loupe has no queue: the
author publishes their own work, so the same score would measure self-promotion, and a leaderboard
over self-published work rewards volume over craft. It also contradicts the brief's own hypothesis,
which is a **portfolio** motive — "a breakdown is stronger proof of craft than a shot" — and a
portfolio motive and a points motive pull in opposite directions.

---

## PATTERNS

**The key interaction problem of this product, in one sentence:** how a designer who arrives with a
named component to build — an empty state, a pricing table, an onboarding form — gets from that
task to a small set of solved examples whose construction they can read, **without knowing any tag,
author or product name in advance**.

**Five principled patterns.** They differ in mechanism — what the system matches on — not in layout.

| # | Pattern | How it works | Where it is used in the wild | When it fits | When it breaks |
|---|---|---|---|---|---|
| 1 | **Faceted filtering over declared fields** | Each breakdown field is a facet with a controlled vocabulary and a live count; the user narrows by combining facets | Fonts In Use — Topics / Formats / Typefaces, every value a link with its count (`fontsinuse-home.png`); Awwwards — Awards / Category / Tag / Technology / Country / Font / Color (`awwwards-font-filter.png`) | The user knows which property matters, the vocabulary is small and shared, and the corpus is large enough that narrowing pays | The wanted axis is not a facet; combining six facets returns zero with no way back; the facet is only as reliable as the least careful contributor |
| 2 | **Query by example — "more like this"** | The user points at an item or pastes an image; the system returns neighbours by visual similarity. No vocabulary at all | Cosmos — "by visual similarity" and by colour (`cosmos-search-and-ai-filter.png`); Savee — "search by image" (`savee-home.png`) | The user can recognise what they want but cannot name it — taste-driven, pre-verbal search | The need is functional, not visual: two empty states that solve first-run and filtered-to-zero look nothing alike. It also cannot read the breakdown at all, so the author's work is dead weight |
| 3 | **Natural-language task query, answered by a model over the corpus** | The user describes the task in a sentence; a model retrieves examples and returns reasoning with them | Refero "research mode" — "Describe your task, get analysis, references, and reasoning back" (`refero-home.png`); Refero MCP for coding agents | The need is a sentence rather than a property, and the user wants an argument back, not just a grid | The corpus is small — a model over a few dozen fixtures manufactures confidence it has not earned. It also hides the index, so filling a field no longer makes the author findable |
| 4 | **Structured browse by a task taxonomy** | Navigation, not search: the entry point is a named list of design tasks, and the user walks into one | Refero — Page Types, Flows, UX Patterns, UI Elements (`refero-home.png`); Mobbin's pattern library (`mobbin-landing-gated.png`) | The user arrives with the task already named — exactly the brief's primary user | A task outside the taxonomy is invisible, and the taxonomy is a promise that must be kept for every component; past ~200 entries the taxonomy is itself a search problem |
| 5 | **Follow-and-collect: retrieval through people and sets** | The user does not query the corpus; they subscribe to authors and curated collections and retrieve from a small, human-filtered pool | Are.na channels (`arena-home.png`); Fonts In Use "Sets"; Dribbble follows; Savee boards | Recurring taste needs and serendipity; cheap to build, strong for retention | Fails the primary user outright — someone with a component due today cannot wait for the right author to post. It answers "what is good", not "what solves this" |

- **Chosen: 1 — faceted filtering over declared fields.** Three reasons, each grounded in
  `CLAUDE.md`:
  1. **It is the only pattern in which the author's manual breakdown is what makes their work
     findable.** The brief's spine — "because the breakdown travels with the work, property search
     is free" — is *only true* under this pattern. Pattern 2 ignores the fields, pattern 3 hides
     them, pattern 4 uses one and drops the rest, pattern 5 skips the corpus. And the benchmark's
     first mechanic (pay the author back with something they wanted anyway) has nothing to pay with
     if the fields do not drive retrieval.
  2. **It matches the platform split the brief already fixed.** Desktop primary at ~1440px is where
     a persistent facet rail beside results is affordable; mobile is "browsing and saving to a
     collection, nothing else", which is exactly what facets degrade into — a single chip row — with
     no feature lost.
  3. **It makes progressive completeness consequential instead of decorative.** An item with an
     empty typography field is absent from typography-filtered results, so incompleteness has a
     visible cost to its author. The brief already wants completeness to be "an axis of filtering
     and ranking"; this pattern is what turns that from a label into an incentive.
  **Confirmed at the human gate, 2026-08-06** (`.design/decisions.md`).
- **Second choice — and the condition is already partly met: 4 — task taxonomy browse as the entry,
  facets as the refinement inside it.** The condition was written as "if phase 2b finds that the
  primary persona opens with a *component name* rather than a *property*". At the pattern gate the
  designer reported that it already does: a respondent named **Даня** filters Mobbin by
  «екран реєстрації» and «кошик» — component names, not properties. **Source: designer's report of
  an interview, given verbatim at the phase-2 pattern gate; no interview artifact exists yet.**
  `/dsf:users` must either record that interview as a citable artifact or carry the claim as `[?]`
  — it may not be quietly promoted to a finding. If it holds, the taxonomy becomes the entry surface
  and facets the refinement, on the Mobbin model. That is a reordering of the same two mechanisms,
  not a replacement of the chosen pattern.
- **Disqualified: 3 — natural-language AI query.** Two reasons. The brief fixes the deliverable as
  "a credible static front-end … every flow runs on fixtures", so the corpus is a few dozen items
  and a model over it would perform a confidence the data cannot support. More seriously, it severs
  the link between filling in a breakdown and being found — the one incentive the benchmark
  identified as load-bearing and as absent everywhere else in the market. Disqualified **for this
  product at this size**, not in principle.

---

## CONCLUSIONS

| Gap | Hypothesis | Follows from |
|---|---|---|
| **A machine already writes the breakdown, free.** Refero Styles publishes colour roles with usage notes, a named type scale with its ratio, base unit, max width and per-element radii for 2,000+ sites, with a `DESIGN.md` to paste into an agent | What a machine cannot extract is **why**: "I used Intranet for the main heading because its blocky, unusual shapes felt right for the subject" is not derivable from CSS. Loupe's defensible field is the author's intent, not the values — the values are table stakes it must match, not the differentiator it was assumed to be | COMPETITORS — Refero row; `refero-style-breakdown.png` vs `fontsinuse-use-detail.png` |
| **Nobody has solved supply.** One product of twelve runs on hand-written breakdowns | The breakdown must be the price of something the author wanted anyway, on the Discogs model — the act of filling it produces the author's own case-study page | BENCHMARK — Discogs 5 on criterion 5 |
| **Whether breakdown quality needs moderation** — `[?]` 6 of the brief, previously unasked | No staff review and no free-for-all: a reader-visible quality state that only readers who have earned the privilege by contributing can set. Discogs and Stack Overflow both hold quality this way with no paid reviewer | BENCHMARK — mechanic 3; Discogs Voting Guidelines |
| **How `[?]` should look in the UI** — the brief makes it a first-class state but does not say what it does | A gap is a task: named field, a date, and the control that fills it, inside the marker — Wikipedia's banner form, not an empty cell | BENCHMARK — Wikipedia 5 on criterion 7; `wikipedia-maintenance-banner.png` |
| **The retrieval mechanism** — `[?]` 2 of the brief | Faceted filtering over declared fields, chosen at the pattern gate; task-taxonomy browse tested as the entry in phase 2b on the Mobbin model | PATTERNS — chosen pattern 1 |
| **Is "grid" the right third axis?** — `[?]` 4 of the brief | **Evidence says no.** The most complete construction spec on the market publishes *Spacing & Shape* — density, 4px base unit, 1280px max width, section gap, card padding, element gap, border radius per element, elevation — and never a column grid. The third axis should be spacing and shape, not grid | COMPETITORS — language reference; `refero-style-breakdown.png` |
| **Trust without a click** — success criterion 2 | The card must carry a *reality status* and a *completeness state*, because the market's at-a-glance signals are award badges (Awwwards SOTD/DEV) or the breakdown itself printed on the card (Fonts In Use), and popularity alone (Dribbble) demonstrably fails: the studied shot admits it is a "concept" only in its fourth paragraph | COMPETITORS — three real differences, item 3 |
| **Comparison** — `[?]` 3 of the brief, demoted at phase 1 | Keep it demoted. **No competitor in the set ships a dedicated side-by-side view**, including the two with the deepest structured data. Shared fields deliver comparison as a side effect, which is what the phase-1 hypothesis predicted | COMPETITORS — matrix, all twelve rows |
| **"Own work only"** — a constraint the closest analogue rejects | Fonts In Use deliberately invites "your own work **or other typography you admire**". Loupe's restriction is a rights-and-authenticity decision that costs pool growth; it should be stated as a chosen trade-off in the IA, not assumed to be free | COMPETITORS — three real differences, item 2 |
| **Component or whole work?** | Unresolved and load-bearing. The brief's user names a component; the breakdown fields describe a whole product. Refero indexes components, Fonts In Use and Refero Styles index whole works. Phase 3 must pick one as the unit and let the other be a facet | COMPETITORS — three open questions, item 3 |

**Numbered hypotheses for later phases to test:**

1. **H1 — Intent is the differentiator, not the values.** A breakdown whose "why" is empty is worth
   no more than an automatically generated one. *Test in phase 4:* the breakdown screen puts intent
   above the value tables, and `/dsf:check` verifies a reader can state *why* a choice was made, not
   only *what* it was.
2. **H2 — The breakdown pays the author back.** Completing it produces a page the author would have
   built for their portfolio anyway. *Test in phase 3:* the IA contains that page as a named object,
   or H2 is falsified and supply has no engine.
3. **H3 — The third axis is spacing and shape, not grid.** *Test in phase 3:* the breakdown's third
   field is density / base unit / max width / radius, and the word "grid" survives only if a
   designer asks for columns by name.
4. **H4 — Completeness must cost something.** An item with an empty field is absent from that
   field's filtered results, so incompleteness is visible to its author as lost reach. *Test in
   phase 4:* filtered results demonstrably exclude incomplete items, and the author's own view says so.
5. **H5 — Quality holds without staff if the right to mark is earned.** *Test in phase 3:* the
   quality state and who may set it exist as objects in the IA.
6. **H6 — A gap is a task.** `[?]` renders as field name + date + the control that fills it.
   *Test in phase 4:* every `[?]` on every screen carries all three, or it is a decoration.
7. **H7 — The entry surface is a task taxonomy, facets refine inside it.** Raised by the designer at
   the pattern gate from an interview with **Даня**, who filters Mobbin by «екран реєстрації» and
   «кошик». *Test in phase 2b:* `/dsf:users` records that interview as a citable artifact, or the
   claim stays `[?]` and pattern 1 stands alone.
8. **H8 — Reality status and completeness both fit on the card.** *Test in phase 4:* both are legible
   in the results grid without opening an item, at ~1440px and in the mobile browse view.

### Sourcing pass

Every factual claim above was walked and attached to a link or a screenshot path in
`research/screens/`. What remains unsourced is marked `[?] unverified` in the matrix and is listed
here so it is not mistaken for collected data:

- **Cosmos monetization** — no pricing page was reached; the row says `[?] unverified`.
- **Refero pricing** — a pricing link exists in the nav; the page was not collected.
- **Savee subscription price** and **Behance Pro / Recruiter Pro prices** — not collected.
- **Fonts In Use revenue beyond foundry sponsorships** — four sponsors were observed in the header
  and in-grid (Typotheque, Frere-Jones Type, DJR, Kilotype) plus a Mobbin house ad; whether any
  other revenue exists is unverified.
- **Layers monetization beyond inline sponsored cards** — unverified.
- **Savee's "over 1M users"** and **Refero's "2,000+"** are the companies' own published figures,
  recorded as claims, not independently checked.
- **The Даня interview** is the designer's report at a gate; no interview artifact exists yet.

One correction, kept visible rather than tidied away: at the step-1 gate **Layers** was placed in
the aspirational group on the rationale that it is a community built around writing about craft.
The live site is a tag rail over a "Hot" shot feed with inline ads. The rationale did not survive
verification; the row was kept as a data point and relabelled rather than quietly rewritten.
