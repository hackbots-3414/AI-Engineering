# AI-Engineering

Hackbots 3414's workspace for learning to build software with AI: robot code, team tools, and things we haven't thought of yet.

Students and mentors are learning this together. The goal isn't just working code. It's becoming engineers who can **describe a problem clearly, judge what the AI gives back, and own the result.**

## What's here

```
AI-Engineering/
├── README.md                              ← you are here: what the repo is and how we work
├── HOWTO-ai-engineering-notebook.md       ← how to name, fill in, and refine your notebook
├── TEMPLATE-ai-engineering-notebook.md    ← the short entry sketch you copy for each challenge
├── notebooks/                             ← one AI Engineering Notebook per student
├── prompt-library/                        ← standard AI instructions + reusable prompt pieces
└── tools/                                 ← small non-robot tools, until one earns its own repo
```

- **Notebooks** are each student's running log of challenges, prompts, results, and lessons. They carry over from season to season.
- **The prompt library** collects what works. When a notebook entry's *Prompt lessons* would help everyone, it gets copied here.
- **Tools** hold small projects that don't belong in the robot repo, such as scouting helpers, pit checklists, and data scripts. When a tool grows up, it moves to its own repo and leaves a link behind.
- **Robot code doesn't live here.** It goes in that season's robot repo. Notebook entries link to the robot PR, and the robot PR links back to the entry.

## Getting started

Everything about **naming your notebook, filling in entries, and what each section means** lives in [`HOWTO-ai-engineering-notebook.md`](HOWTO-ai-engineering-notebook.md). That file is the source of truth, so read it first. [`TEMPLATE-ai-engineering-notebook.md`](TEMPLATE-ai-engineering-notebook.md) is the short sketch you copy for each entry. This README covers only how the repo and the workflow fit together.

## Suggested workflow

### One-time setup

1. Clone this repo, or open it in GitHub Codespaces.
2. Create a branch for your notebook.
3. Copy the template into `notebooks/`, renaming it as the HOWTO describes.
4. Commit, push, and open a pull request. A mentor merges it, and your notebook now exists on `main`.

### For each challenge

```
 Write the entry ──► Mentor review ──► Run the prompt ──► Review & test ──► Explain-back ──► Log the outcome ──► Merge
        ▲                                                                                                       │
        └──────────────────────────── Refine: new entry at the top ◄────────────────────────────────────────────┘
```

1. **Branch.** Make a short-lived branch for the entry, e.g. `<your-notebook-prefix>/<challenge-short-name>`.
2. **Write the entry before any code exists.** Fill in the Challenge, Prompt, and Validation Plan sections. Thinking it through *before* prompting is most of the skill.
3. **Open a draft PR** and ask a mentor to look at it. Mentors may push back on the prompt before it runs, and that's part of the learning.
4. **Run the prompt.** For now, Mr. Z or Mr. Brown copies the Prompt section into the AI tool and shares the conversation with you.
5. **Review and test** against your Validation Plan. Generated code goes where it belongs: the robot repo (its own branch and PR) or `tools/` here. It never goes into your notebook.
6. **Explain-back.** Walk a mentor or teammate through the code. If you can't explain it yet, ask the AI to help you understand it, then try again.
7. **Log the outcome** in the entry, including Pluses, Deltas, and any AI mistakes you caught.
8. **Mark the PR ready and merge.** Merge often. Small notebook PRs are easy to review and rarely conflict.
9. **Refine.** If it needs another round, start a new entry at the top of your notebook that links back to this one.

### Contributing to the prompt library

If a lesson from your entry would help the whole team, open a PR that adds it to `prompt-library/` and links back to your notebook entry as the source.

## Ground rules

- **Only edit your own notebook.** Comment on someone else's through a PR review.
- **No secrets or personal information.** That means no passwords, API keys, phone numbers, or full names in notebooks, prompts, or code. This repo is public.
- **Abandoned is a valid status.** Experiments that didn't work out are worth keeping, because they teach the next person what not to try.

## Resources

- [Hackbots FRC Programming Reference](https://therekrab.github.io/frc-programming-reference/)
- [WPILib documentation](https://docs.wpilib.org/)
