# Audit and Refactor Checklist

Use this file for reviews, audits, and refactors where the goal is Fluent 2 conformance.

## Audit Sequence

1. Identify the host platform and implementation stack.
2. Read the relevant Fluent 2 foundation and UX pages.
3. Read the relevant React component docs if components are involved.
4. Read the icon policy if icons are present.
5. Read Power Platform guidance if the host is HTML web resource, PCF, or Vite-based code app.
6. List deviations before editing code.

## What to Check

### Foundations

- Does the UI align with Fluent 2 design principles?
- Are color and elevation choices Fluent-consistent?
- Are shape, material, and motion choices aligned with Fluent 2?
- Is typography using a Fluent-consistent hierarchy?
- Is spacing and layout consistent rather than ad hoc?

### UX guidance

- Does the UI respect accessibility guidance?
- Does copy follow Fluent content-design expectations?
- Are design tokens used where applicable instead of hard-coded design drift?
- Are loading and wait states aligned with Fluent wait UX guidance?

### Components

- Is the selected component the correct Fluent pattern for the job?
- Are states, density, affordances, and hierarchy consistent with the component guidance?
- Are custom-built controls replacing an existing Fluent pattern without a valid reason?

### Icons

- Are icons sourced from Flicon?
- Are icon metaphors literal and consistent?
- Are non-Fluent icon sets mixed in?

### Platform constraints

- Is the host platform preventing exact Fluent fidelity?
- If yes, has the work stopped for approval before introducing compromise?

## Finding Format

For each finding, capture:
- Current behavior
- Why it conflicts with Fluent 2 or icon policy
- Which source area it violates
- Recommended Fluent-aligned change
- Whether approval is required before fixing it

## Refactor Rules

- Fix the highest-impact design deviations first.
- Prefer adopting an existing Fluent pattern over inventing a local variant.
- Remove bespoke styles that fight Fluent tokens or hierarchy.
- Keep changes scoped to the conformance goal. Do not widen the refactor without reason.
- If exact compliance is blocked, stop and ask instead of approximating silently.
