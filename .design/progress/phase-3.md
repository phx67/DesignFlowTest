# Phase 3 · Structure — step ledger

Written by `/dsf:ia` (steps `ia.*`).

- ia.1 · Entity inventory — objects before screens · 2026-08-07 · files: ia/sitemap.md (Entities) · 7 entities, 4 questionable; Author carries no job and is flagged; Quality mark wanted by [RES] H5 but demanded by no job
- ia.2 · Sitemap derived from jobs · 2026-08-07 · files: ia/sitemap.md (Screens) · 8 screens, 1 [ORPHAN] (Author), Publish cluster resting on hypothesis jobs only
- ia.2 · HUMAN GATE — sitemap · 2026-08-07 · files: ia/sitemap.md, .design/decisions.md · gate: "(a) Author — кредит на Work, не окремий екран, follow — v2. (b) R4 — режим колекції, не новий екран. (c) Quality mark лишається в Questionable, H5 непідтверджена; якість несе completeness + confirmed/unconfirmed. (d) Намір = анотації на матеріалі роботи, absent → present → case."
- ia.3 · Navigation model and tap-depth budget · 2026-08-07 · files: ia/sitemap.md (Navigation) · 3 global items, main job at 2 taps of a 3-tap budget, rejected globals recorded
- ia.4 · User flows in Mermaid · 2026-08-07 · files: ia/flows.md — 4 flows (Main, R3, R4, HJ1); all 4 parsed and rendered without error by Mermaid 11.16.1 in Chromium, not checked by eye; every screen node already existed in the sitemap, none added
- ia.5 · Traceability matrix · 2026-08-07 · files: ia/sitemap.md (Traceability) · 11 job rows x 7 screens; 3 orphans found and kept with reasons — Publish and Confirm the extraction covered only by hypothesis jobs, S3 deliberately unserved; the no-empty-row/column target is explicitly not met
- ia.6 · IA critique + HUMAN GATE — defect prioritization · 2026-08-07 · files: ia/flows.md, ia/sitemap.md, .design/decisions.md · 10 defects found across 4 classes, 9 fixed at the source, 1 left as a record (S3); all 4 diagrams re-rendered by Mermaid with zero errors after the fixes · gate: "Чинити у джерелі: 1-8, 10. Лишити записом: 9 — S3 свідомо поза скоупом (P2-only)."
- ia.7 · ia/ia.html · 2026-08-07 · files: ia/ia.html (686K) — verified in Chromium at http://127.0.0.1:8744; 4 inlined Mermaid SVGs, 6 tables, no horizontal page scroll; only console entry is the local server's /favicon.ico 404. Diagrams are Mermaid-rendered at build time and inlined as SVG rather than rendered live by a vendored 3.5MB mermaid.min.js — deviation from checklist item 18, raised for the designer
- ia.8 · Run the phase checklist · 2026-08-07 · files: — · 21 of 22 verified against the files; item 18 ("live-rendered Mermaid diagrams") is the one I cannot call a clean pass, because the diagrams are pre-rendered
- ia.9 · Living docs, dashboard, commit · 2026-08-07 · files: CLAUDE.md (Structure block), README.md (Structure section), index.html (phase-3 artifacts present, steps)
- ia.10 · Sign-off · 2026-08-07 · files: .design/progress/phase-3.md · commit 7634c59 pushed; no tag — /dsf:check 3 closes the phase
