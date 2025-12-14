## 2024-05-23 - Dynamic Content Announcements
**Learning:** For single-page apps that update content dynamically without page reloads (like generators), screen reader users are often left in the dark.
**Action:** Implement a standard `.visually-hidden` live region (`aria-live="polite"`) and populate it with a brief status message (e.g., "Scene generated") whenever the content updates. This provides immediate, non-intrusive feedback.
