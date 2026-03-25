# Copilot Instructions for react-shadcn-starter

This repository uses React 19, TypeScript, Vite, Tailwind CSS v4, shadcn-style UI components, and react-router-dom.

## Core conventions

- Prefer TypeScript and function components.
- Keep imports consistent with the existing style (external imports first, then internal imports).
- Reuse existing utilities and components before adding new abstractions.
- Use the existing `cn` utility from `src/lib/utils.ts` for class name composition.
- Follow existing naming and file patterns in `src/components`, `src/pages`, and `src/config`.

## Routing and app structure

- Keep route definitions in `src/Router.tsx`.
- Use the existing `AppLayout` pattern for shell and nested page routes.
- Preserve support for both BrowserRouter and HashRouter through `VITE_USE_HASH_ROUTE`.

## UI and styling

- Prefer existing shadcn-style primitives in `src/components/ui` before creating custom primitives.
- Use Tailwind utility classes and design tokens already defined in `src/index.css`.
- Keep light and dark mode behavior compatible with the current theme token approach.
- Maintain responsive behavior for new layouts and components.

## State and behavior

- Prefer local state first; only introduce context or global state when clearly needed.
- Keep components focused and avoid mixing unrelated concerns in one file.
- Extract reusable logic into hooks when duplication appears across pages/components.

## Quality bar

- Keep changes minimal and aligned with current architecture.
- Avoid broad refactors unless explicitly requested.
- Ensure TypeScript types are explicit where inference is unclear.
- Ensure `npm run lint` and `npm run build` remain clean after changes.

## Do not

- Do not replace existing UI primitives with a different component system.
- Do not introduce new state libraries without explicit request.
- Do not break the existing route structure or GitHub Pages hash-route compatibility.
