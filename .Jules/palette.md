## 2024-05-23 - Accessibility Patterns for Static Apps
**Learning:** For single-page static apps that update content dynamically without page reloads, screen reader users miss context updates. Adding a simple `aria-live` region ("announcer") provides immediate feedback for actions like "Generate Scene".
**Action:** In future static generators, always include a hidden `aria-live="polite"` element and update its text content whenever the main view changes.
## 2024-05-24 - Semantic Structure and Labeling
**Learning:** Replacing stylized divs with semantic headings (`h2`) and explicitly associating labels (`for="id"`) instantly creates a navigable outline and context for screen readers without changing visuals.
**Action:** Always check that form inputs have associated labels and that document sections use header tags (h1-h6) rather than just bold text/divs.
