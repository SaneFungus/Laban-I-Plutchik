## 2024-05-23 - Accessibility Patterns for Static Apps
**Learning:** For single-page static apps that update content dynamically without page reloads, screen reader users miss context updates. Adding a simple `aria-live` region ("announcer") provides immediate feedback for actions like "Generate Scene".
**Action:** In future static generators, always include a hidden `aria-live="polite"` element and update its text content whenever the main view changes.

## 2024-05-24 - Context-Aware Animation
**Learning:** When updating UI content, users benefit from visual feedback (animation) on data regeneration, but find it distracting during localization changes (switching language).
**Action:** Pass a `shouldAnimate` flag to render functions. Animate only when the data/content changes, not when the representation (language) changes.
