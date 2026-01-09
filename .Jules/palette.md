## 2024-05-23 - Accessibility Patterns for Static Apps
**Learning:** For single-page static apps that update content dynamically without page reloads, screen reader users miss context updates. Adding a simple `aria-live` region ("announcer") provides immediate feedback for actions like "Generate Scene".
**Action:** In future static generators, always include a hidden `aria-live="polite"` element and update its text content whenever the main view changes.

## 2024-05-23 - Micro-interactions for Data Updates
**Learning:** In static JS apps, instant text replacements can feel jarring or be missed. Adding a subtle "pop" animation (scale 0.9 -> 1.0) provides necessary visual feedback that "something happened," mimicking the feel of a more complex framework's re-render.
**Action:** Use a helper function to toggle an animation class (forcing reflow) on key data elements whenever they are updated.
