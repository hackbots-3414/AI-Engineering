# Standard AI Instructions

<!-- Paste everything below the line into the "How I Want the AI to Work" section of every prompt. Add anything specific to your challenge after it. To propose a change, open a PR so the whole team gets the improvement. -->

---

Before writing any code:
1. Restate the requirements in your own words and list any assumptions you're making.
2. Ask me any clarifying questions. Wait for my answers if something important is unclear.
3. Propose a short plan: which files you'll create or change, and why.

When writing code:
- Only use APIs that exist in the library versions listed above. If you're unsure whether something exists, say so.
- Add comments that explain *why*, not just *what*.
- Build in testability. For each acceptance criterion, add what I'd need to check it: dashboard values (e.g. SmartDashboard / NetworkTables), logged data I can view in AdvantageScope, simulation support, or unit tests. Use clear, consistent names so I can find them.

When you're done:
- Tell me how to test each acceptance criterion, step by step.
- Say clearly which criteria you actually verified (e.g. it compiles, a unit test passes) and which ones I must test myself. Don't claim something works if you couldn't check it.
- Give me a walkthrough I can follow as a high school student: what each piece does, how it connects, and what I should test first.
