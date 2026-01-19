## 2024-05-23 - Accessibility Patterns for Static Apps
**Learning:** For single-page static apps that update content dynamically without page reloads, screen reader users miss context updates. Adding a simple `aria-live` region ("announcer") provides immediate feedback for actions like "Generate Scene".
**Action:** In future static generators, always include a hidden `aria-live="polite"` element and update its text content whenever the main view changes.

## 2024-05-24 - Information Parity in Announcements
**Learning:** Even with an `aria-live` region, blindly announcing state changes ("New scene generated") isn't enough if context (like game instructions) is visual-only. Blind users miss the "why" of the change.
**Action:** Ensure the announcement template includes all critical game rules or instructions displayed on screen, not just the data values.
