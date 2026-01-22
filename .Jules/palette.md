## 2024-05-23 - Accessibility Patterns for Static Apps
**Learning:** For single-page static apps that update content dynamically without page reloads, screen reader users miss context updates. Adding a simple `aria-live` region ("announcer") provides immediate feedback for actions like "Generate Scene".
**Action:** In future static generators, always include a hidden `aria-live="polite"` element and update its text content whenever the main view changes.

## 2024-05-23 - Clipboard Feedback
**Learning:** For actions like "Copy to Clipboard", temporary visual feedback (changing button text) is crucial. Resetting this state using the main `render(false)` loop ensures consistency and avoids "stuck" states.
**Action:** When implementing temporary feedback in state-driven apps, piggyback on the main render cycle to reset the UI after a timeout.
