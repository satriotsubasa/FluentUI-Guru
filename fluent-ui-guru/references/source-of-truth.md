# Source of Truth

Use this file to decide which documentation to read and which source wins when multiple sources overlap.

## Source Priority

Apply sources in this order:
1. Fluent 2 foundations and UX guidance
2. Fluent 2 React component documentation
3. Fluent UI React v9 Storybook for React implementation details
4. Flicon for icon discovery and selection only

Do not let a lower-priority source override a higher-priority source.

## Tier 1: Fluent 2 Foundations and UX Guidance

Read the relevant pages from this set before proposing UI:

### Entry points

- `https://fluent2.microsoft.design/`
- `https://fluent2.microsoft.design/get-started/design`
- `https://fluent2.microsoft.design/get-started/develop`

### Foundations

- `https://fluent2.microsoft.design/design-principles`
- `https://fluent2.microsoft.design/color`
- `https://fluent2.microsoft.design/color-tokens`
- `https://fluent2.microsoft.design/elevation`
- `https://fluent2.microsoft.design/layout`
- `https://fluent2.microsoft.design/material`
- `https://fluent2.microsoft.design/motion`
- `https://fluent2.microsoft.design/shapes`
- `https://fluent2.microsoft.design/typography`
- `https://fluent2.microsoft.design/iconography`

### UX guidance

- `https://fluent2.microsoft.design/accessibility`
- `https://fluent2.microsoft.design/content-design`
- `https://fluent2.microsoft.design/design-tokens`
- `https://fluent2.microsoft.design/handoffs`
- `https://fluent2.microsoft.design/onboarding`
- `https://fluent2.microsoft.design/wait-ux`

## Tier 2: Fluent 2 React Component Documentation

Use the React component tree as the component-level authority:
- `https://fluent2.microsoft.design/components/web/react/`

For any component in scope, read its relevant overview, usage, and accessibility guidance before implementing or auditing it.

Examples:
- Text, link, button, input, dialog, tabs, nav, table, tooltip, badge, card
- Any layout or content wrapper components used in the design

## Tier 3: Fluent UI React v9 Storybook

Use the official Storybook when the project stack supports Fluent UI React v9:
- `https://storybooks.fluentui.dev/react/?path=/docs/concepts-introduction--docs`

Use it for:
- Component API shape
- Props, slots, states, and variants
- Composition examples
- React-specific implementation details

Do not use it to override Fluent 2 design guidance.

## Tier 4: Flicon

Use Flicon as the mandatory icon source:
- `https://www.flicon.io/`

Use it only for:
- Finding icon names
- Comparing icon candidates
- Selecting icons from the intended icon corpus

Do not use it as authority for layout, motion, color, typography, spacing, or accessibility.

## Practical Reading Pattern

### New UI

Read:
- Relevant foundation pages
- Relevant UX pages
- Relevant component docs
- Storybook if React implementation is needed
- Flicon if icons are present

### Audit or refactor

Read:
- Relevant foundation pages
- Relevant component docs for every affected component
- Flicon icon rules if icons are present
- Power Platform guidance if the host is Power Platform

### Power Platform

Read:
- Relevant Fluent 2 source pages
- [power-platform-adaptations.md](power-platform-adaptations.md)
- Storybook only if the chosen implementation path can actually use Fluent UI React v9

## Conflict Resolution

- If Fluent 2 and local code disagree, Fluent 2 wins unless the user explicitly approves a deviation.
- If Storybook examples and Fluent 2 foundations appear to disagree, Fluent 2 wins.
- If Flicon and Fluent 2 disagree outside icon selection, Fluent 2 wins.
- If the host platform prevents exact compliance, stop and ask for approval before proceeding.
