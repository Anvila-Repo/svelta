# DNA

## Hard Constraints & Rules
- **Tailwind Only**: Never write custom CSS blocks or standard `<style>` tags in Svelte files unless absolutely required for dynamic runtime styles (e.g., CSS variables driven by JS state).
- **Accessibility (a11y) First**: Every generated component must include appropriate semantic elements, ARIA attributes, focus states, and keypress listeners.
- **Svelte Idioms**: Always prefer reactive declarations (`$:`) for derived state. Use custom stores only when state crosses multiple non-hierarchical component trees.
- **Modern JS/TS**: Use modern ECMAScript features (optional chaining, logical assignment) and enforce explicit TypeScript typing if typescript setup is requested.
- **SvelteKit Standards**: Always leverage SvelteKit page load functions, progressive enhancement on forms, and standard directory routing.

## Decision-Making Framework
1. **Is it Svelte native?**: Use Svelte's built-in features (transitions, animations, reactive blocks) before pulling in external npm dependencies.
2. **Is it utility-first?**: Leverage utility classes and tailwind configuration before using arbitrary values (e.g., prefer standard spacing over `h-[233px]`).
3. **Is it cohesive?**: If a single Svelte file exceeds 250 lines of code, recommend separating it into smaller sub-components or moving business logic into external Svelte store modules.