# Fluent UI Guru Design

**Date:** 2026-04-01

**Goal:** Create a reusable Codex skill that strictly enforces Fluent 2 design language, uses Fluent UI React v9 Storybook as the React implementation reference when applicable, and uses Flicon as the mandatory icon discovery source.

## Scope

The skill must support:
- Creating new Fluent UI interfaces.
- Auditing existing UI for Fluent 2 conformance.
- Refactoring UI toward Fluent 2 conformance.
- General frontend work with a dedicated Power Platform adaptation section for HTML web resources, PCF, and Vite-based code apps.

## Source Hierarchy

### Design authority

Use Fluent 2 documentation as the mandatory design source, especially:
- `https://fluent2.microsoft.design/`
- `https://fluent2.microsoft.design/get-started/design`
- `https://fluent2.microsoft.design/get-started/develop`
- `https://fluent2.microsoft.design/design-principles`
- `https://fluent2.microsoft.design/color`
- `https://fluent2.microsoft.design/elevation`
- `https://fluent2.microsoft.design/layout`
- `https://fluent2.microsoft.design/material`
- `https://fluent2.microsoft.design/motion`
- `https://fluent2.microsoft.design/shapes`
- `https://fluent2.microsoft.design/typography`
- `https://fluent2.microsoft.design/accessibility`
- `https://fluent2.microsoft.design/content-design`
- `https://fluent2.microsoft.design/design-tokens`
- `https://fluent2.microsoft.design/handoffs`
- `https://fluent2.microsoft.design/onboarding`
- `https://fluent2.microsoft.design/wait-ux`
- `https://fluent2.microsoft.design/color-tokens`
- `https://fluent2.microsoft.design/iconography`
- `https://fluent2.microsoft.design/components/web/react/`

### React implementation authority

When the project stack supports Fluent UI React v9, use:
- `@fluentui/react-components`
- `https://storybooks.fluentui.dev/react/?path=/docs/concepts-introduction--docs`

### Icon authority

Use `https://www.flicon.io/` as the mandatory icon discovery and selection source.

This is an intentional override for icon sourcing. The skill must still keep Fluent 2 in control for typography, color, motion, layout, accessibility, and broader visual language decisions.

## Non-Negotiable Rules

- Follow Fluent 2 strictly when the design language defines a pattern.
- Do not silently substitute non-Fluent icon libraries.
- Do not treat Storybook as overriding Fluent 2 foundations.
- Do not treat Flicon as overriding anything except icon discovery and selection.
- If platform constraints prevent exact Fluent conformance, stop and ask for approval before using a compromise.
- For audits and refactors, enumerate the deviations before proposing or applying changes.

## Skill Structure

The skill should contain:
- `SKILL.md`
- `agents/openai.yaml`
- `references/source-of-truth.md`
- `references/icon-policy.md`
- `references/audit-refactor-checklist.md`
- `references/power-platform-adaptations.md`

## Power Platform Notes

Power Platform is a common target but not the only target.

The skill should include dedicated guidance for:
- HTML web resources
- PCF
- Vite-based code apps

Those sections should adapt implementation details to platform constraints without relaxing Fluent 2 requirements by default.
