## 2024-05-23 - Accessibility Patterns for Static Apps
**Learning:** For single-page static apps that update content dynamically without page reloads, screen reader users miss context updates. Adding a simple `aria-live` region ("announcer") provides immediate feedback for actions like "Generate Scene".
**Action:** In future static generators, always include a hidden `aria-live="polite"` element and update its text content whenever the main view changes.

## 2024-05-24 - Keyboard Shortcut Discoverability
**Learning:** Users rarely discover keyboard shortcuts in simple web apps without explicit visual cues.
**Action:** Embed `<span class='kbd-hint'>` directly into button labels to make shortcuts visible and intuitive, while keeping the main text dominant.
