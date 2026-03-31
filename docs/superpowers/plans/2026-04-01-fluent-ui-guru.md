# Fluent UI Guru Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Build the `fluent-ui-guru` skill and supporting references in this workspace.

**Architecture:** Use a lean `SKILL.md` for the mandatory workflow and escalation rules, then move detailed source hierarchy, icon rules, audit checks, and Power Platform notes into small reference files. Generate `agents/openai.yaml` through the skill scaffold flow and validate the finished folder with the bundled validator.

**Tech Stack:** Markdown, YAML, Python helper scripts

---

### Task 1: Author the spec and scaffold the skill

**Files:**
- Create: `docs/superpowers/specs/2026-04-01-fluent-ui-guru-design.md`
- Create: `docs/superpowers/plans/2026-04-01-fluent-ui-guru.md`
- Create: `fluent-ui-guru/`

- [ ] Write the approved design to the spec file.
- [ ] Create the implementation plan file.
- [ ] Run `init_skill.py` to scaffold `fluent-ui-guru` with a `references/` directory and UI metadata.

### Task 2: Replace the scaffold with the real skill content

**Files:**
- Modify: `fluent-ui-guru/SKILL.md`
- Modify: `fluent-ui-guru/agents/openai.yaml`
- Create: `fluent-ui-guru/references/source-of-truth.md`
- Create: `fluent-ui-guru/references/icon-policy.md`
- Create: `fluent-ui-guru/references/audit-refactor-checklist.md`
- Create: `fluent-ui-guru/references/power-platform-adaptations.md`

- [ ] Write the final frontmatter and main instructions in `SKILL.md`.
- [ ] Add reference files for source hierarchy, icon policy, audit flow, and Power Platform adaptations.
- [ ] Ensure `agents/openai.yaml` has a useful display name, short description, and default prompt.

### Task 3: Validate and test the skill

**Files:**
- Modify if needed: any skill file that fails validation

- [ ] Run the bundled validator against `fluent-ui-guru`.
- [ ] Perform a manual forward-test pass against representative prompts because subagent dispatch is not available in this session unless explicitly requested by the user.
- [ ] Refine the skill if the manual review finds ambiguity or loopholes.
