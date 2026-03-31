# Power Platform Adaptations

Use this file when implementing or auditing Fluent-aligned UI in Power Platform environments.

## Core Rule

Power Platform constraints change implementation details, not the design target.

Default target:
- Fluent 2 design language
- Flicon for icon discovery and selection

If the host environment blocks exact Fluent behavior or styling, stop and ask for approval before introducing a compromise.

## HTML Web Resources

Use this path when building plain HTML, CSS, and JavaScript inside a model-driven app or similar host.

### Guidance

- Scope styles carefully to avoid host CSS collisions.
- Recreate Fluent hierarchy with disciplined tokens and CSS variables instead of ad hoc values.
- Preserve accessible focus treatment, contrast, and keyboard behavior.
- Use Fluent-consistent spacing, typography, layering, and motion where the host allows it.
- Keep markup semantic even when the host shell is legacy or constrained.

### Watch for

- Global CSS leakage from the host app
- Host fonts or resets changing your intended rendering
- Interactive patterns that cannot fully match Fluent behavior inside the host container

## PCF

Use this path for Power Apps Component Framework controls.

### Guidance

- Prefer Fluent UI React v9 patterns when the control architecture and dependency constraints allow them.
- Isolate styling so the control stays visually coherent inside the host shell.
- Respect container size, density, and responsiveness constraints of the model-driven surface.
- Use design tokens deliberately rather than layering arbitrary custom CSS on top.

### Watch for

- Bundle or runtime limits that make Fluent dependencies impractical
- Host theming interactions that distort token intent
- Controls that inherit unexpected layout or font rules from the surrounding app

## Vite-Based Code Apps

Use this path when the Power Platform project is a code app or similar Vite-managed frontend.

### Guidance

- Prefer `@fluentui/react-components` when React is available and acceptable for the project.
- Use Fluent UI React v9 Storybook for component APIs and composition patterns.
- Keep custom wrappers thin. Do not rebuild Fluent primitives without a clear need.
- Use Flicon-selected icons consistently across the app.

### Watch for

- Local component abstractions that drift from Fluent semantics
- Token bypass through hard-coded colors, radii, spacing, or typography
- Mixing Fluent components with unrelated visual systems

## Model-Driven App Bias

Model-driven app work often benefits from:
- Clear information hierarchy
- Dense but readable layouts
- Predictable form and command patterns
- Strong accessibility and keyboard support

Use Fluent 2 to improve clarity and consistency, not to impose novelty for its own sake.

## Escalation Triggers

Stop and ask for approval when:
- The host shell prevents an exact Fluent component pattern
- The project cannot ship Fluent UI React v9 where it would normally be preferred
- The selected Flicon icon cannot be implemented in the target environment
- Existing Power Platform constraints force a meaningful design deviation
