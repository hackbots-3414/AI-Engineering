# 2026-11-23 — Create initial robot project

**Author(s): SK** · **Type:** New · **Project:** Robot · **Prompt run by:** MrZ· **AI & model:** Opus 5.5 High· **PR:** · **Status:** Drafting

## Challenge
Drivetrain: We are going to be making a program which will allow the robot to Drive around. This program will be for the Drivetrain, which will help the Robot drive around.

<!-- What problem, why it matters, who uses the result -->

**Out of scope:**
Don't effect other subsystems

## Prompt
<!-- ✂️ Copy from here to "End of Prompt". The AI sees only this part. -->

### Context
<!-- What the AI can't guess: repo, existing files, design assumptions -->

Put code in here: https://github.com/hackbots-3414/2027_Preseason.git

- Compatible with CTRE
- Uses Kraken X60 for all 4 Drive motors
- Uses Kraken X45 for all 4 Steer Motors
- Use Generated Tuner Constants: https://github.com/hackbots-3414/2027_Preseason/blob/Sai_Max/src/main/java/frc/robot/generated/TunerConstants.java


### Behavior
<!-- Steps, inputs → outputs, "when X, then Y", edge cases -->

In a PS5 controller:
  - Left Joystick Up -> Forward
  - Left Joystick Down -> Backwards
  - Left Joystick Left -> Goes to the Left
  - Left Joystick Right -> Goes to the Right

  - Right Joystick Right -> Robot Rotates Clockwise
  - Right Joystick Left -> Robot Rotates Anti Clockwise


### Acceptance Criteria
<!-- Observable checks: normal behavior, failure modes, what must be visible on the dashboard -->
- Should be able to have Logging mechanism compatibly with 2026 Advatage Kit
- Make possible for Swerve Drive 
- Make Possible through VSCODE 2026
- Have Uptodate Field, where We can see the Robot be Simulated on GLASS
- 

### Constraints
<!-- Robot: WPILib / Phoenix 6 / best practices / IO layer / sim. Tool: platform, users, data, offline? -->
- DO NOT modify generated Tuner Constants:  https://github.com/hackbots-3414/2027_Preseason/blob/Sai_Max/src/main/java/frc/robot/generated/TunerConstants.java

### Components
<!-- One line each: Role · Part · CAN ID / port · limits · notes -->
- Look At Generated Tuner Constants:  https://github.com/hackbots-3414/2027_Preseason/blob/Sai_Max/src/main/java/frc/robot/generated/TunerConstants.java


### Safety
<!-- Current/soft limits, behavior when disabled or a sensor fails; no secrets or personal info -->
- Look for specefic battery Voltage, and make sure the Code is Power efficient so batter usage  is never below 7
- If Brownout Level Less than 7 then Log it 

### How I Want the AI to Work
<!-- Paste prompt-library/standard-ai-instructions.md here, plus any additions for this challenge -->
Here are the Best practices for our Team: https://therekrab.github.io/frc-programming-reference/

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
