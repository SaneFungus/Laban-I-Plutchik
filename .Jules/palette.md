## 2024-05-23 - Accessibility Patterns for Static Apps
**Learning:** For single-page static apps that update content dynamically without page reloads, screen reader users miss context updates. Adding a simple `aria-live` region ("announcer") provides immediate feedback for actions like "Generate Scene".
**Action:** In future static generators, always include a hidden `aria-live="polite"` element and update its text content whenever the main view changes.

## 2024-05-23 - Semantic Headings in Dynamic Cards
**Learning:** In single-page apps, using semantic headings (H1-H6) for content areas (like Cards) allows screen reader users to jump directly to relevant sections, which is otherwise impossible with generic `div` soup.
**Action:** Ensure distinct content sections use proper heading tags (`h2`, `h3`) instead of styled `div`s, even if they are visually identical.
