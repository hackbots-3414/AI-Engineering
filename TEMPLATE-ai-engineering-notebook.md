# AI Engineering Notebook — [Grad Year]-[Your Initials]

> **File name:** `YYYY-initials-ai-engineering-notebook.md`, using your four-digit graduation year, e.g. `2028-jd-ai-engineering-notebook.md`. Putting the year first keeps each class grouped together when files are sorted.
>
> **How to use this notebook:** Copy everything from the first `# YYYY-MM-DD` heading down to the end for each new entry, and put the newest entry at the **top** (below this note). Delete any section that doesn't apply, and add sections when you need them. The lines starting with `>` are guidance. Delete them as you fill each section in.
>
> **The golden rule:** you must be able to support whatever code you create, however you created it. If you can't explain it, it doesn't merge.

---

# YYYY-MM-DD — Challenge Short Name

| | |
|---|---|
| **Author(s)** | |
| **Entry type** | New challenge / Refinement of [link to earlier entry] |
| **Project** | Robot code / Tool / Other: ___ |
| **Prompt run by** | Mr. Z / Mr. Brown / self |
| **AI tool & model** | e.g. Claude Opus 5.5, Copilot, ChatGPT |
| **Branch / PR** | link |
| **Status** | Drafting / Prompted / Testing / Merged / Abandoned |

## Challenge

> What problem are we solving, and **why** does it matter? Who will use the result: the driver, the pit crew, scouts, you? Write it so a teammate who missed the meeting would understand it.

**Done when:**
> One to three sentences that describe success, e.g. "The driver can hold right bumper and the intake runs until a ball is detected, then stops on its own."

**Out of scope:**
> What the AI should *not* do or touch. This stops it from "helpfully" rewriting things you didn't ask about.

---

## Prompt

> ✂️ **Everything from here to "End of Prompt" is what gets copied and pasted.** The AI will see *only* this part, so it has to stand on its own. Don't write "see above."

### Context

> What does the AI need to know that it can't guess? Which repo and files already exist, what the related code already does, which design assumptions apply. If a team instructions file exists (e.g. `FRC_CODING_INSTRUCTIONS.md`), say that it should be followed, or attach it.

### Behavior / Functionality Required

> Describe the behavior in detail: the steps of the algorithm, the sequence of events, the inputs and expected outputs. Concrete examples work well: "When X happens, Y should happen." Include edge cases: what if the sensor is unplugged? What if the button is pressed twice?

### Constraints & Environment

> The overarching rules the solution must follow. Keep the subsection that applies and delete the other.

#### For robot code
- Language / framework: Java, WPILib command-based (version: ____)
- Vendor libraries: CTRE Phoenix 6 (Pro? yes/no), REVLib, PathPlanner, etc.
- Follow Hackbots best practices: https://therekrab.github.io/frc-programming-reference/
- Use the IO layer pattern (hardware + sim implementations): yes/no
- Must work in simulation before it goes on the robot: yes/no

#### For tools and other projects
- Platform: Python script / web page / Google Sheet / phone app / ___
- Who runs it, and on what device?
- Where does data come from, and where does it go?
- Must work offline (e.g. at competition with no Wi-Fi)? yes/no

#### Component: [Name / Role] *(repeat for each component)*

> The specific hardware or software piece and the role it plays in the solution.

- **Role:** e.g. Left Front Steer Motor
- **Part:** e.g. WCP Kraken X60 (integrated TalonFX)
- **ID / Port:** e.g. CAN ID 4, CANivore bus "drivetrain"
- **Units / Ranges / Limits:** e.g. gear ratio 21.43:1, soft limits 0–90°
- **Notes:** e.g. inverted, has a limit switch, homing sequence required

### Safety

> Robot: current limits, soft limits, max speeds, what happens when disabled or when a sensor fails. Can anyone get pinched or hit?
> Tools: no passwords, API keys, or personal information in code or prompts.

### How I Want the AI to Work

> Keep this block in every prompt. Edit it if you need to.

Before writing any code:
1. Restate the requirements in your own words and list any assumptions you're making.
2. Ask me any clarifying questions. Wait for my answers if something important is unclear.
3. Propose a short plan: which files you'll create or change, and why.

When writing code:
- Only use APIs that exist in the library versions listed above. If you're unsure whether something exists, say so.
- Add comments that explain *why*, not just *what*.
- Afterward, give me a walkthrough I can follow as a high school student: what each piece does, how it connects, and what I should test first.

**— End of Prompt —**

---

## Validation Plan

> Write this section **before** you see any code. What will you look for to decide whether the output is "good"?

**Tests / checks:**
- [ ] e.g. Builds with no errors or warnings
- [ ] e.g. In sim: pressing the bound button runs the intake, and it stops when the beam break trips
- [ ] e.g. On robot (wheels up / mechanism clear): ___
- [ ] e.g. Follows best practices: hardware is private, Commands returned, Triggers for boolean states

**My comfort reading this kind of code (1–5):** __
> 1 = "I can't follow it yet," 5 = "I could have written it myself." Be honest. This is how mentors know where to help.

**What would help me understand it faster?**
> e.g. a diagram of the command flow, a line-by-line walkthrough, a comparison to code I already know.

**Explain-back:** I walked ________ (mentor or teammate) through the code on ____ (date).

---

## Outcome Notes

**Prompt actually sent:** [link to the chat, or paste below if it was edited before sending]

**What was produced:** files created or changed, commit or PR link

**Did it work on the first try?** Yes / Partly / No. How many follow-up prompts did it take? ___

**Time spent:** ___

### What went right (Pluses)

> What you're happy with, in the code and in your prompt.

### What could be better (Deltas)

> What you'd do differently and what needs refining. You can ask the AI: "Here is my prompt and what you produced. How should I have written the prompt to get this right the first time?"
> When you're ready to try again, create a **new entry** at the top with Entry type = "Refinement of [this entry]". It only needs the sections that changed.

### AI mistakes I caught

> Invented methods, deprecated APIs (e.g. Phoenix 5 vs Phoenix 6), ignored constraints, overconfident claims. Catching these is a skill, so record them.

### What I learned

> About the code, the robot, the problem, or yourself.

### Prompt lessons (for the team prompt library)

> One or two reusable tips, e.g. "Always give the CAN bus name, not just the ID." Good ones get copied into `prompt-library/`.

---

## Mentor Review

> Mentors: leave feedback here, or on the PR.

- **Reviewed by / date:**
- **Comments:**
