# Organization Copilot Instructions
 
 ## Design System
 - Always import UI components from `@yourorg/design-system`
 - Reference docs: https://design.yourcompany.com
 - Use design tokens, never hardcode colors or spacing
 
 ## Required Components (use instead of native HTML)
 | Instead of...  | Use...                | Import from              |
 |----------------|----------------------|--------------------------|
 | `<button>`     | `<DsButton>`         | `@yourorg/ds/Button`     |
 | `<input>`      | `<DsTextField>`      | `@yourorg/ds/TextField`  |
 | `<select>`     | `<DsDropdown>`       | `@yourorg/ds/Dropdown`   |
 | `<dialog>`     | `<DsModal>`          | `@yourorg/ds/Modal`      |
 
 ## Styling Rules
 - Use CSS variables: `var(--ds-color-primary)`, `var(--ds-spacing-md)`
 - No inline styles except for dynamic values
 - Use `clsx` for conditional class names
 
 ## Code Patterns
 - All API calls must use `@yourorg/api-client`
 - Error boundaries required on every page-level component
 - Use `react-query` for server state management
 
 ## Anti-Patterns (never generate these)
 - No `fetch()` directly — use the API client
 - No `px` units — use design tokens
 - No `#hex` colors — use token variables