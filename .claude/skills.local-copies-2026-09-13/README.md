# Local skill copies, parked 2026-09-13

These 26 entries used to live at `.claude/skills/`. They were moved here as
part of the vault-layers build so that this repo stops name-shadowing the
user-wide `marketing-skills` plugin (installed at
`~/.claude/plugins/cache/marketingskills/marketing-skills`, version 2.3.0,
43 skills) and so `.claude/skills/` can hold the vault-deployed skills instead.

**Nothing was deleted, and the move is one command to undo:**

```bash
cd ~/seomachine && git mv .claude/skills.local-copies-2026-09-13 .claude/skills
```

## What was actually measured (2026-09-13), because the premise was wrong

The assumption going in was "26 identical copies of plugin skills". They are
not identical:

- **0 of 26** are byte-identical to the plugin's version.
- **7 share a name with a plugin skill and differ from it**, so those really
  were shadowing: `content-strategy` (19 changed lines), `copy-editing` (129),
  `copywriting` (17), `marketing-ideas` (16), `marketing-psychology` (15),
  `programmatic-seo` (14), `seo-audit` (119).
- **18 have names the plugin does not use at all**: ab-test-setup,
  analytics-tracking, competitor-alternatives, email-sequence, form-cro,
  free-tool-strategy, launch-strategy, onboarding-cro, page-cro, paid-ads,
  paywall-upgrade-cro, popup-cro, pricing-strategy, product-marketing-context,
  referral-program, schema-markup, signup-flow-cro, social-content. Several
  look like renamed variants of a plugin skill (`page-cro` vs the plugin's
  `cro`, `email-sequence` vs `emails`), but a renamed variant is not a
  shadow - under its own name it is extra capability this repo had and, while
  parked here, no longer has.
- `growth-lead-SKILL.md` is a loose file, not a skill directory, so it was
  never loadable as a skill in the first place.

**Founder call:** whether the 7 real shadows should be dropped in favour of
the plugin versions, and whether the 18 locally-named ones should be promoted
into `~/tengo-skills` (the marketplace) or into the vault's `Skills/` so every
project can use them. Until that call, restoring is the safe default if
seomachine feels like it lost something.
