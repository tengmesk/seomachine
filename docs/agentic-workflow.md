# Agentic Workflow: Finding Your Unknowns

Working method for this workspace, adapted from [A Field Guide to Claude Fable: Finding Your Unknowns](https://claude.com/blog/a-field-guide-to-claude-fable-finding-your-unknowns) (Anthropic, 2026). The core idea: the skill of agentic work is systematically reducing your unknowns before, during, and after implementation.

**The framework**: Known Knowns (the prompt) · Known Unknowns (questions you know to ask) · Unknown Knowns (things you'd recognize on sight — surface them with prototypes) · Unknown Unknowns (gaps you haven't considered — surface them with a blind-spot pass).

## Pre-implementation

### 1. Blind Spot Pass
Before starting significant work (new cluster, new integration, a rewrite of core modules), explicitly enumerate the four quadrants. Ask: "what about this project/codebase/market do I not know that I don't know?"
*SEO Machine examples*: unverified client facts before writing; whether a target page exists on the live site; which data source a command silently depends on (DataForSEO vs GSC); conflicting quality rubrics.

### 2. Brainstorms & Prototypes
For subjective outputs (headlines, article angles, landing pages), generate several genuinely different directions to react to before committing.
*SEO Machine examples*: `headline-generator` agent variants; 3–4 outline directions before a pillar draft; meta-creator's 5×5 title/description options.

### 3. Interviews
When ambiguity remains, ask the user focused questions — one decision at a time, architectural/irreversible decisions first (publishing targets, brand claims, git policy, named authors). Don't guess facts only the user can know.

### 4. References
Point at concrete exemplars rather than describing style abstractly.
*SEO Machine examples*: `context/writing-examples.md` is the canonical voice reference; `examples/castos/` shows filled template format; a competitor URL beats a description of one.

### 5. Implementation Plans
Before substantial work, write a short plan to `docs/plan-YYYY-MM-DD-<slug>.md` highlighting the **decisions** (what changes, why, risks), not mechanics. Get the surprising decisions visible.

## During implementation

### 6. Implementation Notes
Keep a running log at `docs/notes-YYYY-MM-DD-<slug>.md`: deviations from plan, edge cases, bugs found, facts verified. This is institutional knowledge for the next session — memory files summarize it; notes preserve the detail.

## Post-implementation

### 7. Pitches & Explainers
Package plan + changes + outcomes into one stakeholder-readable document when work needs buy-in (e.g. before a big publish or a policy change).

### 8. Reports & Quizzes
For significant merges, produce a human-readable report of what actually changed, plus a short quiz the reviewer should be able to pass before merging. If you can't pass the quiz, you don't understand your own change.

## Standing decisions for this repo

- **Quality gate**: `content_scorer.py` composite ≥70 is the publish gate. The five `/write` agent reports (analyzer, seo-optimizer, meta-creator, internal-linker, keyword-mapper) are advisory inputs — reconcile their recommendations, don't chase every score.
- **Fact discipline**: any named client, statistic, or URL must trace to `context/` files or the live site. When unverifiable: genericize or omit. Never guess names — verify or interview.
- **Data honesty**: when DataForSEO/GSC aren't connected, label volumes/difficulty as estimates and note the gap in the output.
