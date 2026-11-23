# 2026-11-23 — Create initial robot project 

**Author(s): DM** · **Type:** New · **Project:** Robot · **Prompt run by:** · **AI & model:** · **PR:** · **Status:** Drafting

## Challenge
Write a basic control script that commands a robot to approach the edge of any road, pause to confirm the path is clear (not if it were up to me), drive straight across to the opposite curb, and come to a complete stop insted of freaking out and moving.
<!-- What problem, why it matters, who uses the result -->

**Out of scope:**
Don't affect, change or modify any other subsystems
## Prompt
<!-- ✂️ Copy from here to "End of Prompt". The AI sees only this part. -->

### Context
<!-- What the AI can't guess: repo, existing files, design assumptions -->
put code in here: https://github.com/hackbots-3414/2027_Preseason.git

 - Compatible with CTRE
 - Uses Kraken x60 in all 4 drive motors
 - Uses Kraken x45 in all 4 steer motors


### Behavior
<!-- Steps, inputs → outputs, "when X, then Y", edge cases -->
In a PS5 controller:
 - Left joystick pushed forwards -> Forward
 - Left joystick pushed backwards -> Backwards
 - Left joystick pushed to the left -> Goes to the Left
 - Left joystick pushed to the right -> Goes to the Right

 - Right joystick pushed to the right -> Robot rotates clockwise
 - Right joystick pushed to the left -> Robot rotates counter clockwise

### Acceptance Criteria
<!-- Observable checks: normal behavior, failure modes, what must be visible on the dashboard -->

 - Compatible with CTRE
 - Uses Kraken x60 in all 4 drive motors
 - Uses Kraken x45 in all 4 steer motors
 - Should have logging mechanism compatibility with 2026 Advantage Kit
 - Use generated Tuner Constraints https://github.com/hackbots-3414/2027_Preseason/blob/main/src/main/java/frc/robot/generated/TunerConstants.java
 - Make it be able to Swerve Drive
 - Make it possible to go through VSCode 2026
 - be able to update the field, where we can view the robot be simulated on GLASS



### Constraints
<!-- Robot: WPILib / Phoenix 6 / best practices / IO layer / sim. Tool: platform, users, data, offline? -->

 - DO NOT MODIFY Generated Tuner Constraints: https://github.com/hackbots-3414/2027_Preseason/blob/main/src/main/java/frc/robot/generated/TunerConstants.java

 - Make it be able to Swerve Drive
 - Make it possible to go through VSCode 2026


### Components
<!-- One line each: Role · Part · CAN ID / port · limits · notes -->
- 

### Safety
<!-- Current/soft limits, behavior when disabled or a sensor fails; no secrets or personal info -->

 - Look for specific Battery Voltage, and make sure the Code is Power efficient thus giving better usage is never below 7
 - If Brownout level less than 7 log it
 - If any failure that is harmful to the robot or other humans around it IMMIDIEATELY STOP and log it

### How I Want the AI to Work
<!-- Paste prompt-library/standard-ai-instructions.md here, plus any additions for this challenge -->

 - Build based on specifications above
 - Run it on a simulation
 - If error occurs re-make and retest 
 - when it is good send it to me
 - I will deceide wether it needs any more adjustments and you repeat the whole process again

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
