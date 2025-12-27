# Palette's Journal

## 2024-05-21 - Visual Styling vs Semantic Structure
**Learning:** This project uses specific classes (e.g., `.card-header`) for styling but applies them to generic `div` tags, missing the opportunity for semantic structure (`h2`, `h3`).
**Action:** When styling headers, always use the appropriate heading tag (`h1`-`h6`) and reset browser defaults in CSS if necessary, rather than styling `div`s.
