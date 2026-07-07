# Implementation Plan: Field-Guide Adoption + Pillar Article Finalization

**Date**: 7 July 2026
**Source**: [A Field Guide to Claude Fable: Finding Your Unknowns](https://claude.com/blog/a-field-guide-to-claude-fable-finding-your-unknowns)
**Scope decision (user)**: Both tracks — institutionalize the methodology in the repo AND finish the pending pillar-article work using it.

## Key decisions (the "data model" of this change)

| Decision | Choice | Why |
|---|---|---|
| Where methodology lives | New `docs/agentic-workflow.md` + short section in `CLAUDE.md` | CLAUDE.md is loaded every session (durable); full guide in docs to keep CLAUDE.md lean |
| Article author (E-E-A-T) | Tengiz Meskhi, Chief Executive Officer | User chose CEO; name verified on conceptdigital.com/about |
| Reviewer field | Removed (not left as placeholder) | SEO agent flagged placeholder text as harmful; don't assert an unverified reviewer |
| H1 change | "…Development Company in London…" | Exact-phrase gap was the top finding of 2 of 5 agents |
| Video embed | Leave explicit TODO unless a verifiable authoritative video found | Never embed unverified URLs |
| Quality rubric conflict | Note in workflow doc; scorer (composite ≥70) is the gate, agent reports are advisory | Blind-spot finding: two rubrics disagree (85.2 vs 77.8) |

## Work items

### Track A — Institutionalize (repo process)
1. `docs/agentic-workflow.md`: the 8 practices mapped to SEO Machine's content pipeline (blind-spot pass → brainstorm → interview → references → plan → notes → explainer → quiz).
2. `CLAUDE.md`: add a concise "Working Method" section pointing at the doc.

### Track B — Finish pillar article (using the methodology)
3. Fix 1: exact primary phrase in H1, intro, conclusion (density 0.55% → ~1%).
4. Fix 2: "bespoke software development" in one H2.
5. Fix 3: internal links — remove dup `/contact`, add mobile-app/internal-tools/logistics/healthcare links, improve 2 anchors.
6. Fix 4: meta description ≤160 chars with CTA verb; delete the on-page placeholder footnote; add a second real external authority link.
7. Fix 5: readability — split 5 long sentences, add transition words (Flesch 47.7 → target 55+).
8. Fix 6: author = Tengiz Meskhi (CEO).
9. Re-run scrubber + content scorer (gate: ≥70; expect ≥85).

### Track C — Post-implementation artifacts
10. Implementation notes kept during work → `docs/notes-2026-07-07-field-guide-adoption.md`.
11. Explainer: one document packaging plan + changes + results for stakeholder review.
12. HTML report + quiz delivered to user before merge.
13. Branch + PR (repo convention); user merges after quiz.

## Known risks
- H1/meta edits could push past 60-char limits — count characters on every edit.
- Adding 4 internal links could exceed the ≤7 rule for <3k words; article is ~2,900 words and will land at 10 links — acceptable for pillar content per seo-guidelines ("unless 3,000+ word article"; pillar target is 3,500+, and we're also adding text). Verify final count + word count together.
- Link additions must use only URLs verified in `context/internal-links-map.md`.
