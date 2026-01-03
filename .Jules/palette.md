## 2024-05-23 - Accessibility Patterns for Static Apps
**Learning:** For single-page static apps that update content dynamically without page reloads, screen reader users miss context updates. Adding a simple `aria-live` region ("announcer") provides immediate feedback for actions like "Generate Scene".
**Action:** In future static generators, always include a hidden `aria-live="polite"` element and update its text content whenever the main view changes.

## 2024-05-23 - Semantic Structure & Labels
**Learning:** Even in simple single-page apps, using correct semantic tags (like `h2` for card headers) is crucial for screen reader navigation. Visual styling should be decoupled from tags so that semantic structure can be upgraded without breaking the design. Also, always programmatically associate labels with form inputs using `for` attributes.
**Action:** Review static templates to ensure headings are hierarchical (`h1` -> `h2` -> `h3`) and all form inputs have associated labels.
