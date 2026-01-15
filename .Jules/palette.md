## 2024-05-23 - Accessibility Patterns for Static Apps
**Learning:** For single-page static apps that update content dynamically without page reloads, screen reader users miss context updates. Adding a simple `aria-live` region ("announcer") provides immediate feedback for actions like "Generate Scene".
**Action:** In future static generators, always include a hidden `aria-live="polite"` element and update its text content whenever the main view changes.

## 2024-05-24 - Visual Feedback for Instant Updates
**Learning:** Instant text replacement in static apps can be imperceptible to users, leading to "did it work?" confusion.
**Action:** Implement a `triggerAnimation` utility that forces a reflow (via `void element.offsetWidth`) to replay CSS animations whenever content is updated, providing clear visual confirmation.
