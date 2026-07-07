# Implementation Notes — Field-Guide Adoption (7 July 2026)

Running log of deviations from plan and edge cases hit during implementation. Per the field-guide "Implementation Notes" practice.

- [start] Plan written at docs/plan-2026-07-07-field-guide-adoption.md. Baseline: article scored 85.2 composite / 77.8 agent-rated; density 0.55%.
- [blind-spot finding, pre-work] The repo has two quality rubrics that disagree: `content_scorer.py` composite (gate ≥70) vs content-analyzer agent grade. Decision: scorer is the publish gate, agent reports are advisory. Documented in agentic-workflow.md.
- [interview] User confirmed scope = both tracks; author = CEO. CEO name verified live: Tengiz Meskhi, Chief Executive Officer (conceptdigital.com/about).
- [Track A done] docs/agentic-workflow.md created; CLAUDE.md "Working Method" section added.
- [BUG CAUGHT in review] Article said Rex raised "£5 million" twice — verified figure is €5,000,000 (features.md + live site). All five optimization agents missed the currency error. Fixed both instances. Lesson: adversarial verify checks presence of claims, not unit consistency — added nothing automated, but human/final-pass review caught it.
- [deviation] Removed the mid-article "Book a call" /contact CTA entirely (linker said remove-or-replace; all alternative targets were already linked). Article retains 3 CTAs: soft (web-dev, ~word 450), medium (MVP service), strong (conclusion /contact).
- [deviation] Internal links now 11 (map guideline ≤7 for <3k words) — accepted deliberately: pillar-class article, all links are Tier 1/2 targets recommended by the internal-linker agent.
- [note] Video embed remains an explicit italic TODO — no verifiable authoritative video selected; must be resolved before WordPress publish.
- [note] Reviewer field removed rather than left as a placeholder (placeholder text on-page is worse than absence).
