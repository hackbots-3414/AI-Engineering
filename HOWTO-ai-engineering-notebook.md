# HOWTO: Your AI Engineering Notebook

This is the guide for filling in [`TEMPLATE-ai-engineering-notebook.md`](TEMPLATE-ai-engineering-notebook.md). Read it once, and come back when you're unsure about a section. The template stays short on purpose. The explanations live here.

> **The golden rule:** you must be able to support whatever code you create, however you created it. If you can't explain it, it doesn't merge.

## Setting up your notebook

- **File name:** `YYYY-initials-ai-engineering-notebook.md`, using your four-digit graduation year and lowercase initials with no spaces or periods. Example: `2028-jd-ai-engineering-notebook.md`. Putting the year first keeps each class grouped together when files are sorted.
- **Location:** `notebooks/`
- **One notebook for your whole time on the team.** Don't start a new one each season.

## Adding an entry

- Copy the entry block from the template, everything from `# YYYY-MM-DD` down.
- **Put the newest entry at the top** of your notebook, so the most recent work is the first thing anyone sees.
- Delete any section that doesn't apply, and add sections when you need them.
- The `<!-- comments -->` in the template are hints. They don't show up when GitHub displays the file, so you can leave them in or delete them.

## Section by section

### Header line
Fill in what you know. **Type** says whether this is a new challenge or a refinement of an earlier entry; link to that entry if it is a refinement. **AI & model** matters: when something breaks weeks later, the first question will be which model wrote it and from what prompt.

### Challenge
What problem are we solving, and **why** does it matter? Who will use the result: the driver, the pit crew, scouts, you? Write it so a teammate who missed the meeting would understand it.

**Out of scope** tells the AI what *not* to do or touch. This stops it from "helpfully" rewriting things you didn't ask about. Since the Challenge section sits outside the prompt, repeat anything important from it in **Context**.

### Prompt
Everything from `## Prompt` to **End of Prompt** gets copied and pasted to the AI. **The AI sees only this part,** so it has to stand on its own. Don't write "see above."

**Context:** what the AI needs to know that it can't guess. Which repo and files already exist, what the related code already does, which design assumptions apply. If a team instructions file exists (e.g. `FRC_CODING_INSTRUCTIONS.md`), say that it should be followed, or attach it.

**Behavior:** describe the behavior in detail: the steps of the algorithm, the sequence of events, the inputs and expected outputs. Concrete examples work well: "When X happens, Y should happen." Include edge cases: what if the sensor is unplugged? What if the button is pressed twice?

**Acceptance Criteria:** how will anyone know it's correct? Write checks someone could actually observe or measure. Telling the AI how the result will be judged makes it build toward those checks, and makes it add ways to *see* them. Include:
- **Normal behavior,** e.g. "Holding right bumper runs the intake until the beam break trips, then it stops within 100 ms."
- **Edge cases and failure modes,** e.g. "If the beam break is unplugged, the intake stops after 3 seconds and reports a fault instead of running forever."
- **What must be visible,** e.g. "I need to see intake velocity, current, and gamepiece-detected on the dashboard."

**Constraints:** the overarching rules the solution must follow.
- *Robot code:* Java and WPILib command-based (give the version); vendor libraries (CTRE Phoenix 6, Pro or not; REVLib; PathPlanner); follow the [Hackbots best practices](https://therekrab.github.io/frc-programming-reference/); whether to use the IO layer pattern; whether it must work in simulation first.
- *Tools and other projects:* platform (Python script, web page, Google Sheet, phone app); who runs it and on what device; where data comes from and goes; whether it must work offline (e.g. at competition with no Wi-Fi).

**Components:** one line per piece of hardware or software involved, with the role it plays. Example:
`Left Front Steer Motor · WCP Kraken X60 (integrated TalonFX) · CAN ID 4, CANivore bus "drivetrain" · 21.43:1, soft limits 0–90° · inverted`

**Safety:**
- *Robot:* current limits, soft limits, max speeds, and what happens when the robot is disabled or a sensor fails. Can anyone get pinched or hit?
- *Tools:* no passwords, API keys, or personal information in code or prompts.

**How I Want the AI to Work:** paste in [`prompt-library/standard-ai-instructions.md`](prompt-library/standard-ai-instructions.md). It tells the AI to ask questions before coding, build in testability, say what it couldn't verify, and explain its work at a level you can follow. Add anything specific to your challenge after it. If you think the standard instructions should change, open a PR so everyone benefits.

### Validation Plan
This section is **not** part of the prompt. It's how *you* independently decide whether the output is good. **Write it before you see any code,** so the AI's answer doesn't shape what you look for.

- **How I'll test:** where and how you'll check each acceptance criterion, e.g. "Builds clean → each criterion in sim → each criterion on the robot with wheels up / mechanism clear, watching the dashboard values."
- **My own checks (not given to the AI):** one or two checks you keep to yourself. If the code passes checks it was never told about, that's real evidence it works, not just that it was built to pass the test. Good examples: "follows best practices (hardware private, Commands returned, Triggers for boolean states)" or "mash the button rapidly: does anything get stuck or fight itself?"
- **What the AI couldn't verify:** fill this in *after* the AI responds. Copy its list, and make sure each item is covered by one of your tests.
- **Comfort (1–5):** 1 = "I can't follow it yet," 5 = "I could have written it myself." Be honest. This is how mentors know where to help.
- **Would help me understand:** e.g. a diagram of the command flow, a line-by-line walkthrough, a comparison to code you already know.
- **Explain-back:** who you walked through the code, and when.

### Outcome
- **Prompt sent:** link to the chat. If the prompt was edited before it was sent, paste the final version too.
- **Produced:** the PR or files. Generated code goes where it belongs (the robot repo, or `tools/`), never into your notebook.
- **Pluses:** what you're happy with, in the code and in your prompt.
- **Deltas:** what you'd do differently. You can ask the AI: *"Here is my prompt and what you produced. How should I have written the prompt to get this right the first time?"*
- **AI mistakes caught:** invented methods, deprecated APIs (e.g. Phoenix 5 vs Phoenix 6), ignored constraints, overconfident claims. Catching these is a skill, so record them.
- **What I learned:** about the code, the robot, the problem, or yourself.
- **Prompt lessons:** one or two reusable tips, e.g. "Always give the CAN bus name, not just the ID." Good ones get added to `prompt-library/`.

### Mentor Review
Mentors leave feedback here or on the PR.

## Refining
When a Delta is worth another try, add a **new entry at the top** with Type = "Refinement of [link]". It only needs the sections that changed, plus whatever the AI needs to stand on its own: if you're starting a fresh chat, include the full prompt again.
