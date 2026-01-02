## 2024-05-23 - Accessibility Patterns for Static Apps
**Learning:** For single-page static apps that update content dynamically without page reloads, screen reader users miss context updates. Adding a simple `aria-live` region ("announcer") provides immediate feedback for actions like "Generate Scene".
**Action:** In future static generators, always include a hidden `aria-live="polite"` element and update its text content whenever the main view changes.

## 2024-05-24 - Semantic Structure for Cards
**Learning:** Using generic `div`s for card headers (like "Character A") prevents screen reader users from navigating the page structure efficiently. Replacing them with `h2` elements (while keeping the visual class `card-header`) instantly adds landmark navigation without breaking styles.
**Action:** Always check if "section titles" are semantic headings or just styled divs.

## 2024-05-24 - Form Label Association
**Learning:** Labels that are visually positioned near inputs but not programmatically linked (via `for` attribute or nesting) fail accessibility checks and reduce usability (clicking the label doesn't focus the input).
**Action:** Always ensure `label` elements have a `for` attribute matching the `id` of the target input.
