# Fluent UI Guru

![Fluent UI Guru logo](fluent-ui-guru/assets/Fluent_React_UI_icon.svg)

`fluent-ui-guru` is a Codex skill for creating, auditing, and refactoring UI that must strictly follow the [Fluent 2 Design System](https://fluent2.microsoft.design/).

It is designed to keep Codex aligned to:
- Fluent 2 foundations and UX guidance
- Fluent 2 React component documentation
- Fluent UI React v9 Storybook for React implementation details
- Flicon for icon discovery and selection

## What The Skill Enforces

- Strict Fluent 2 design language for layout, typography, color, motion, tokens, accessibility, content, and component usage
- Fluent UI React v9 as the preferred React implementation path when the project supports `@fluentui/react-components`
- Flicon as the mandatory icon source for discovery and selection
- Explicit audit findings before refactors
- Approval-first behavior when exact Fluent compliance is blocked by platform constraints

## Why Flicon Is Mandatory For Icons

This skill intentionally uses [Flicon](https://www.flicon.io/) for icon discovery and selection, even when the rest of the implementation follows Fluent 2 and Fluent UI React v9.

That constraint exists mainly for compatibility with Power Platform work, especially model-driven app implementations where the intended icon corpus is closer to the Flicon set.

Flicon controls icon discovery only. It does not override Fluent 2 rules for accessibility, layout, spacing, motion, color, or typography.

## Source Hierarchy

The skill applies documentation in this order:

1. [Fluent 2 foundations and UX guidance](https://fluent2.microsoft.design/)
2. [Fluent 2 React component docs](https://fluent2.microsoft.design/components/web/react/)
3. [Fluent UI React v9 Storybook](https://storybooks.fluentui.dev/react/?path=/docs/concepts-introduction--docs)
4. [Flicon](https://www.flicon.io/) for icons only

The full page list and conflict rules live in [`fluent-ui-guru/references/source-of-truth.md`](fluent-ui-guru/references/source-of-truth.md).

## Power Platform Focus

The skill is general-purpose, but it includes dedicated guidance for Power Platform:
- HTML web resources
- PCF controls
- Vite-based code apps

That guidance is documented in [`fluent-ui-guru/references/power-platform-adaptations.md`](fluent-ui-guru/references/power-platform-adaptations.md).

## Repository Layout

```text
.
├── README.md
├── docs/
│   └── superpowers/
│       ├── plans/
│       └── specs/
└── fluent-ui-guru/
    ├── SKILL.md
    ├── agents/
    │   └── openai.yaml
    ├── assets/
    │   └── Fluent_React_UI_icon.svg
    └── references/
        ├── source-of-truth.md
        ├── icon-policy.md
        ├── audit-refactor-checklist.md
        └── power-platform-adaptations.md
```

## Install

Install the skill into the local Codex skills directory:

```powershell
Copy-Item -LiteralPath .\fluent-ui-guru -Destination "$HOME\.codex\skills" -Recurse
```

Then restart Codex so the new skill is discovered.

## Use

Invoke the skill directly in Codex:

```text
$fluent-ui-guru
```

Example requests:
- "Use $fluent-ui-guru to audit this PCF control against Fluent 2."
- "Use $fluent-ui-guru to design this React page with Fluent 2 and Flicon icons."
- "Use $fluent-ui-guru to refactor this HTML web resource so it follows Fluent 2."

## Key Files

- [`fluent-ui-guru/SKILL.md`](fluent-ui-guru/SKILL.md): main skill rules and workflow
- [`fluent-ui-guru/references/source-of-truth.md`](fluent-ui-guru/references/source-of-truth.md): Fluent 2 page hierarchy and source precedence
- [`fluent-ui-guru/references/icon-policy.md`](fluent-ui-guru/references/icon-policy.md): icon selection rules and escalation
- [`fluent-ui-guru/references/audit-refactor-checklist.md`](fluent-ui-guru/references/audit-refactor-checklist.md): audit and refactor review flow
- [`fluent-ui-guru/references/power-platform-adaptations.md`](fluent-ui-guru/references/power-platform-adaptations.md): host-specific Power Platform guidance

## Status

This repo contains both:
- The source copy of the skill for maintenance and versioning
- The installable skill payload under `fluent-ui-guru/`
