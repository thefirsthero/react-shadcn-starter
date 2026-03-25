---
description: 'Theme and styling guidance for CSS files in this Vite plus shadcn starter. Use when editing CSS and design tokens.'
applyTo: '**/*.css'
---

# Theme and CSS Instructions

## Token-first styling

- Prefer updating existing design tokens before adding one-off hardcoded color values.
- Keep token naming aligned with current semantic groups such as background, foreground, primary, muted, border, ring, and sidebar.
- Preserve the existing OKLCH-based token format for consistency.

## Dark mode compatibility

- When adding or changing a token in :root, make the corresponding update in .dark unless intentionally shared.
- Keep contrast and readability balanced in both light and dark themes.
- Avoid introducing styles that only work in one theme.

## Tailwind and layering conventions

- Keep Tailwind directives and plugin declarations at the top of the file.
- Preserve the existing @theme and @layer organization.
- Prefer utility class composition in components over adding large custom CSS blocks unless needed for global theming.

## Scope and maintainability

- Limit global selector changes to cases where app-wide behavior is intended.
- Avoid unrelated refactors while making style fixes.
- Keep responsive behavior and existing layout assumptions intact.

## Validation mindset

- Confirm that visual changes do not regress core UI primitives.
- Verify styles remain consistent across pages, sidebars, cards, and interactive controls.
