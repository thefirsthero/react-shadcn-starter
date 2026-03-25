---
description: 'React and TypeScript implementation guidance for this Vite plus shadcn starter. Use when editing TS and TSX files.'
applyTo: '**/*.ts, **/*.tsx'
---

# React and TypeScript Instructions

## Component and file patterns

- Prefer function components and explicit props types when inference is unclear.
- Keep component files focused on one responsibility.
- Reuse utilities from src/lib and existing UI primitives from src/components/ui before creating new abstractions.
- Keep imports grouped as external first, then internal aliases and local modules.

## Routing and app structure

- Add or update route definitions only in src/Router.tsx.
- Preserve the existing AppLayout nesting pattern for page routes.
- Keep compatibility with BrowserRouter and HashRouter behavior controlled by VITE_USE_HASH_ROUTE.

## Styling and UI consistency

- Use Tailwind utility classes and design tokens already defined in src/index.css.
- Keep light and dark mode behavior aligned with existing token usage.
- Prefer class composition through cn from src/lib/utils.ts.
- Maintain responsive layouts for both mobile and desktop.

## State and logic

- Prefer local component state first.
- Extract shared logic into hooks only when duplication appears.
- Avoid introducing global state libraries unless explicitly requested.

## Quality checks

- Keep changes minimal and avoid broad refactors unless requested.
- Preserve TypeScript type safety instead of suppressing errors.
- After meaningful edits, run lint and build checks where possible.
