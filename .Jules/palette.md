## 2024-05-22 - Dynamic Content & Screen Readers
**Learning:** In single-page generators where main content updates dynamically without page reload, screen reader users receive no feedback.
**Action:** Always implement a Live Region (`aria-live="polite"`) that announces the key result (e.g., "Scenario generated: Joy vs Sadness") whenever the "Generate" action is triggered.
