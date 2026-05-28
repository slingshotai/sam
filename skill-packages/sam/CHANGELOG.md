# SAM — Changelog

## v2.1.0 — 2026-05-28

- Episode freshness check: when a member references an EP episode by number that isn't in the local ep-knowledge index, SAM now prompts them to update before answering, instead of guessing from the title. Keys off the episode number now baked into the EP newsletter's SAM-section prompt.

## v2.0.0 — 2026-05-18

**Major version: SAM evolves from teach-only to teach-or-do.**

The headline change: SAM can now *run* workflows packaged with paid Slingshot skills (e.g. `sam, check my account` runs an actual account analysis via MAGPIE and saves the report), not just teach. The teach-first DNA is preserved as one mode — *narrate* — within an evolved product. Members choose per invocation via the verb they use.

### Added — Workflow mode (6th mode alongside Q&A, Lesson, Demo, Discovery, Update)

- New `do/` folder pattern parallel to `learn/`. Skills can ship `learn/` only (mentor-only — existing pattern), `do/` only (rare — pure tool), or both (teach + do).
- Workflow files are markdown with frontmatter (`workflow`, `trigger`, `tools`, `duration`, `reads`, `writes`) plus a Purpose, Steps, and Success section.
- SAM scans all three skill locations (global, vault, project) for `do/*.md` and builds a trigger index. Triggers are natural-language phrases that route the member's input to the right workflow.
- SAM is stateless per invocation; workflow state lives in vault files declared in `reads:` / `writes:` frontmatter.

### Added — Verb-driven UX (narrate vs execute)

- **Narrate verbs** (`explain`, `walk me through`, `walk-through`, `teach me`, `tell me how to`) — SAM narrates each step as it runs the workflow. Preserves the teach-first DNA.
- **Execute verbs** (`run`, `do`, `check`, `find`, `replicate`, `analyse`, `update`, `post`, or no verb) — SAM runs silently, reports only the result summary.
- Ambiguous verbs fall back to the member's `agent_verbosity` profile setting.

### Added — Risk-tier system (per-tool, declared in SKILL.md)

- Tools declare risk per operation in their SKILL.md frontmatter (`tool_risks: { magpie.search: low, upload-post.publish: high }`).
- `low` = SAM runs automatically without confirmation, regardless of verbosity mode.
- `high` = SAM ALWAYS confirms before running, regardless of mode.
- Per-step `**[risk: high]**` overrides allowed inline in `do/` files.
- If a tool has no `tool_risks:` declared, SAM defaults to `high` (safest fallback) and warns the member.

### Added — `agent_verbosity` profile field

- New field in `~/.slingshot/profile.md`: `agent_verbosity: adaptive | explain | terse`.
- `adaptive` (default for new v2.0.0 members) — narrate first run of a workflow per profile, terse on subsequent runs. Tracks first-run state in `~/.slingshot/workflow-history.jsonl`.
- `explain` (default for v1.x members upgrading) — preserves the v1.x teach-first behaviour. No silent change for existing members.
- `terse` — for power users who know the workflows.

### Added — First-v2-invocation migration prompt

- When SAM is invoked and the profile exists but lacks `agent_verbosity`, SAM detects v1.x → v2.0.0 upgrade and runs a one-time migration prompt explaining the new modes + asking the member to pick a default. Saves to profile. Then proceeds with the original request.
- Default to `explain` if member doesn't pick — preserves v1.x behaviour.

### Changed — "What SAM Does NOT Do" principles

- Old: *"SAM does not do tasks. SAM teaches."*
- New: *"SAM can teach or do — the verb picks the mode."* Workflows are still made *visible* (clear summaries in execute mode). High-risk operations always confirm regardless of mode.

### Backwards compatibility

- Skills with `learn/` only (Brand Voice Pro, Moby, EP Knowledge) work identically to v1.x. Nothing changes for mentor-only skills.
- Existing v1.x evals (Q&A, Lesson, Discovery, no-match) all still pass — those modes are unchanged.
- Existing member profiles without `agent_verbosity` get the migration prompt on first v2 invocation, then default to `explain`.
- Pricing ($497 / $1,997) unchanged. Agent capability ships as v2.0.0 free upgrade for all members. Future paid `do/` packs (ig-growth, Crowd-Sunday, Veg-launch) priced per-pack on top.
- Update mechanism (`sam, update`) unchanged. v2 ships via the existing `git pull` path.

### Design references

- Design doc: `Vault/6.Resources/04.AI/Design Plans/2026-05-18-sam-v2-mentor-plus-agent-design.md`
- Implementation plan: `Vault/6.Resources/04.AI/Design Plans/2026-05-18-sam-v2-implementation-plan.md`
- First workflow shipping with v2: `ig-growth/do/account-check.md` (read-only weekly account tracker)

---

## v1.2.0 — 2026-04-03

- **Explicit update instructions**: Update process now has step-by-step commands for each component (SAM repo, brain, EP Knowledge, purchased skills). Uses `git pull origin main` as the primary update mechanism — no more partial updates.
- **Version tracking on all skills**: BVP, EP Knowledge, and EP Weekly Brief all have version fields and changelogs.

## v1.1.0 — 2026-04-03

Major architecture update.

- **Three knowledge layers**: Brain (Matt's direct knowledge), EP Knowledge (podcast evidence), Skill learn/ folders. Search priority: brain → skills → EP → research.
- **Starter brain**: Framework overviews ship with the public SAM repo. Full brain cloned separately from private `sam-brain` repo in Module 6.
- **Full update system**: `sam, update` now checks ALL components — SAM skill, brain, EP Knowledge, EP Weekly Brief, and all purchased skills. Presents a summary table with version comparisons and changelogs.
- **Update mode**: Added to mode table. Triggered by "sam, update", "check for updates", "new version".
- **Repo renamed**: `slingshot-onboarding` → `sam`. Old URLs redirect automatically.
- **Course restructured**: New Module 6 (Supercharge SAM's Brain), renumbered 07-10. Story Overlap moved to brain. Bonus module removed.
- **Video-vs-prompt notes**: Modules 1-4 now note that written prompts may differ from video versions.

## v1.0.0 — 2026-04-03

Initial release.

- SAM core: Q&A, Guided Lesson, Demo, and Discovery modes
- Voice guide: Matt Edmundson's teaching voice
- Member profile system (`~/.slingshot/profile.md`)
- Multi-site support with currency localisation
- Slingshot Framework learn content (7 areas, FUEL, Product Quadrant, Story Overlap)
- Cross-skill routing: searches all installed skills' `learn/` folders
- Custom overrides: `custom/` folder preserved across updates
- Version tracking: `version` field in frontmatter + this changelog
