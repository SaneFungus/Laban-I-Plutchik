## 2024-05-23 - Accessibility Patterns for Static Apps
**Learning:** For single-page static apps that update content dynamically without page reloads, screen reader users miss context updates. Adding a simple `aria-live` region ("announcer") provides immediate feedback for actions like "Generate Scene".
**Action:** In future static generators, always include a hidden `aria-live="polite"` element and update its text content whenever the main view changes.

## 2024-05-24 - State-Based UI Feedback Reset
**Learning:** In simple state-driven applications without a framework (Vanilla JS), managing temporary UI states (like "Copied!" feedback) manually can be error-prone when mixed with global state changes (like language switching).
**Action:** Use the main `render()` function to "reset" the UI after a timeout, ensuring the view always reflects the true underlying state, rather than manually reverting DOM changes.
