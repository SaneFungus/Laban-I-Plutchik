## 2024-05-23 - Accessibility Patterns for Static Apps
**Learning:** For single-page static apps that update content dynamically without page reloads, screen reader users miss context updates. Adding a simple `aria-live` region ("announcer") provides immediate feedback for actions like "Generate Scene".
**Action:** In future static generators, always include a hidden `aria-live="polite"` element and update its text content whenever the main view changes.

## 2024-05-24 - Transient Feedback State Management
**Learning:** When implementing temporary feedback (e.g., "Copied!" button text), restoring the original state via a global render function is safer than manually reverting the text, as it handles edge cases like language switching during the timeout.
**Action:** Use `render()` or state-driven updates to clear transient UI states instead of manual DOM manipulation.
