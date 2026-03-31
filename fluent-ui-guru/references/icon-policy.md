# Icon Policy

Use this file whenever the task includes icon selection, icon replacement, icon audit, or icon-driven UI design.

## Mandatory Rule

Use Flicon as the required icon discovery and selection source:
- `https://www.flicon.io/`

This is intentional. Do not silently replace it with another icon picker or icon library.

## Why This Rule Exists

The target environments often include Power Platform implementations where the intended icon set is aligned with the Flicon corpus rather than the latest Fluent UI React v9 icon story.

Treat this as a compatibility constraint, not a suggestion.

## What Flicon Controls

Use Flicon for:
- Searching icon candidates
- Picking the icon name
- Verifying the icon belongs to the intended corpus

## What Flicon Does Not Control

Flicon does not override Fluent 2 guidance for:
- Meaning and metaphor
- Color usage
- Placement
- Sizing logic
- Accessibility
- Visual hierarchy

Use Fluent 2 iconography guidance for those decisions.

## Selection Rules

- Prefer literal metaphors over abstract or overly clever ones.
- Match the icon to the object or shape represented, not just the feature name.
- Keep icon usage consistent across similar actions and entities.
- Avoid mixing icon styles from different families.
- Avoid adding decorative icons that do not improve recognition or scanning.

## Usage Rules

- Keep system icons simple and readable.
- Use one solid color when coloring a system icon. Do not introduce multiple decorative colors.
- Respect contrast requirements.
- Use modifiers only when they clarify meaning without overcomplicating the icon.
- Validate whether a symbol may carry different cultural meaning in context.

## Audit Rules

When auditing icons, check:
- Is every icon sourced from Flicon?
- Does each icon match the intended metaphor?
- Are similar actions using similar icons?
- Are any non-Fluent icon libraries mixed in?
- Are color or modifier choices violating Fluent iconography guidance?

## Escalation Rules

Stop and ask for approval when:
- A requested icon is not available in Flicon
- The implementation environment cannot support the selected icon
- Existing UI depends on a non-Flicon icon library and replacing it may have product impact
- A compromise would require a non-Fluent icon family
