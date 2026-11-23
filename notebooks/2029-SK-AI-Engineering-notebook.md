# 2026-11-23 — Create initial robot project

**Author(s):** SK · **Type:** New · **Project:** Robot · **Prompt run by:** · **AI & model:** · **PR:** · **Status:** Drafting

## Challenge
Creating a drivetrain tha encompasses a CTRE Kraken motors, uses the Advantage Kit, and takes the numbers form the tuner constants
<!-- What problem, why it matters, who uses the result -->

**Out of scope:**
Don't affect, change, modify or impact our other subsytems without permission

## Prompt
<!-- ✂️ Copy from here to "End of Prompt". The AI sees only this part. -->

### Context
<!-- What the AI can't guess: repo, existing files, design assumptions -->
Code is located here: https://github.com/hackbots-3414/2027_Preseason.git

 - Should be compatable with CTRE


### Behavior
<!-- Steps, inputs → outputs, "when X, then Y", edge cases -->
In a PS5 controller:
 - Left Joystick Up --> Forward
 - Left Joystick Down --> Backward
 - Left Joystick Left --> Moves to the left
 - Left Joystick Right --> Moves to the right

 - Right Joystick right --> robot rotates clockwise
  - Right Joystick right --> robot rotates anti-clockwise

### Acceptance Criteria
<!-- Observable checks: normal behavior, failure modes, what must be visible on the dashboard -->
- Should have loggin mechinisms which are compatible with Advantage kit
- Make it possible for Swerve Drive
- Mkae it possible through WPLib VS Code 2026
- Have a updates field, we should be able to see the robot simulated on glass

### Constraints
<!-- Robot: WPILib / Phoenix 6 / best practices / IO layer / sim. Tool: platform, users, data, offline? -->

DO NOT EDIT ANY FILES, ESPECIALLY THE TUNER CONSTANTS FILE

### Components
<!-- One line each: Role · Part · CAN ID / port · limits · notes -->
- 

### Safety
<!-- Current/soft limits, behavior when disabled or a sensor fails; no secrets or personal info -->
- Look for the specifi battery voltage, and make sure that the code is power efficient so that the voltage is never below 7
- It will burn out if the voltage is below 7, if that happens log it

### How I Want the AI to Work
<!-- Paste prompt-library/standard-ai-instructions.md here, plus any additions for this challenge -->

**— End of Prompt —**

## Validation Plan
<!-- Write before you see any code -->
- **How I'll test:** 
- **My own checks (not given to the AI):** 
- **What the AI couldn't verify:** <!-- fill in after it responds -->
- **Comfort (1–5):** · **Would help me understand:** · **Explain-back with / date:** 

## Outcome
- **Prompt sent:** [chat link] · **Produced:** [PR / files] · **First try?** · **Follow-ups:** · **Time:** 
- **Pluses:** 
- **Deltas:** 
- **AI mistakes caught:** 
- **What I learned:** 
- **Prompt lessons:** 

## Mentor Review
- **Reviewer / date:** · **Comments:** 
