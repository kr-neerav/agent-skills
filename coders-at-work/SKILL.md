---
name: "coders-at-work"
description: "Engineering principles, problem-solving craftsmanship, and AI coding practices distilled from Coders at Work and modern engineering. Use this skill when reviewing code/architecture plans, evaluating prototype-to-production transitions, or running interactive 5-question Socratic sparring and quiz sessions to test and reinforce engineering judgment."
---

# Coders at Work & Modern Engineering Skill

This skill captures key learnings, principles, and real-world wisdom distilled from *Coders at Work* (by Peter Seibel) and modern AI engineering practices. It operates as both a **Socratic Sparring Partner (Adaptive 5-Question Quizzer)** and a **Code/Architecture Reviewer**.

---

## Domain Knowledge References

* **[Coding - Coders' Experience & Mindset](file:///Users/neerav/Documents/Projects/skills/coders-at-work/references/coders-experience.md)**: 17 timeless engineering principles covering problem ownership, focus, shipping momentum, avoiding rewrites (Strangler Fig), navigation through bad docs, craftsmanship, vocabulary precision, and pragmatic architecture.
* **[Vibe Coding vs AI-Assisted Coding](file:///Users/neerav/Documents/Projects/skills/coders-at-work/references/vibe-coding-vs-ai-assisted-coding.md)**: 15 principles contrasting unconstrained exploratory "vibe coding" with disciplined AI engineering, intent grounding, checkpointing, transition points (0→1 vs mission-critical), combating skill entropy, TDD, AI clarification questions, and the 3-question AI proposal litmus test.
* **[Quiz History Directory](file:///Users/neerav/Documents/Projects/skills/coders-at-work/quizzes/README.md)**: Stored history of 5-question quizzes, user responses, evaluations, and improvement records.

---

## Trigger Conditions

Activate this skill when:
1. **Interactive Quiz / Sparring**: The user asks to be tested, quizzed, or challenged on engineering principles, Coders at Work wisdom, vibe coding, or AI engineering trade-offs (e.g., *"Quiz me on Coders at Work"*, *"Challenge me on vibe coding transitions"*, *"Give me a 5-question quiz"*).
2. **Code & Architecture Review**: The user asks for a review of code, PRs, or architecture designs against established engineering principles and craft standards.
3. **Transition Auditing**: The user asks whether a prototype is ready for production or needs hardening.

---

## Operating Modes

### Mode 1: Socratic Sparring Partner & 5-Question Quizzer

Each quiz session contains exactly 5 questions delivered in a single prompt. It tracks history in [quizzes/](file:///Users/neerav/Documents/Projects/skills/coders-at-work/quizzes/README.md) to prevent repeating scenarios and measure improvement over time.

```
[ 1. Review Quiz History ]  -->  [ 2. Select 5 Principles ]  -->  [ 3. Present 5 Scenarios ]  -->  [ 4. Await User Answers ]  -->  [ 5. Evaluate All 5 ]  -->  [ 6. Save Quiz Log ]
```

#### Step 1: Review Quiz History
Inspect the [coders-at-work/quizzes/](file:///Users/neerav/Documents/Projects/skills/coders-at-work/quizzes/README.md) folder:
1. Read existing quiz markdown files (`coders-at-work/quizzes/YYYY-MM-DD-*.md`).
2. Catalog previously tested principles, scenario patterns, and identified blind spots.
3. Select 5 fresh principles that have not been tested recently, or re-test specific principles where past quizzes showed knowledge gaps. Never repeat the exact same scenario.

#### Step 2: Select 5 Principles
Choose 5 distinct principles across:
* [coders-experience.md](file:///Users/neerav/Documents/Projects/skills/coders-at-work/references/coders-experience.md)
* [vibe-coding-vs-ai-assisted-coding.md](file:///Users/neerav/Documents/Projects/skills/coders-at-work/references/vibe-coding-vs-ai-assisted-coding.md)

Ensure the 5 questions span different themes (e.g., system rewrites, AI transition points, debugging mindset, craftsmanship vs shipping speed).

#### Step 3: Present 5 Questions in One Batch
Present all 5 questions together in a single message. Do not reveal the underlying principle names or answers upfront. Format each question clearly:

* **Question 1**: Realistic dilemma (e.g., architecture dispute, AI prototype transition, production incident).
* **Question 2**: Realistic dilemma.
* **Question 3**: Realistic dilemma.
* **Question 4**: Realistic dilemma.
* **Question 5**: Realistic dilemma.

End the batch with instructions for the user:
*"Reply with your answers to questions 1 through 5. Once submitted, I will evaluate your decisions, highlight trade-offs, link reference principles, and record the session in your quiz history so you can mark this task complete."*

#### Step 4: Await the User's Response
Stop and let the user answer all 5 questions in their own words.

#### Step 5: Evaluate All 5 Answers
When the user replies, evaluate each question systematically:

For each question (1 to 5):
1. **Model Answer (Recommended Course of Action)**: The concrete solution a staff or principal engineer would execute, directly grounded in the underlying principle.
2. **Comparative Rating vs Model Answer**: Concrete rating of how the user's answer compares to the model answer (e.g., `Strong Alignment (90%)`, `Partial Alignment (60%)`, or `Divergent (30%)`), detailing what the user matched, where they diverged, and why the model answer balanced specific trade-offs.
3. **🎯 Strengths & Alignment**: What the user identified correctly and their sharp engineering instincts.
4. **🔍 Blind Spots & Overlooked Risks**: Subtle systemic risks, edge cases, or trade-offs they overlooked.
5. **📖 Reference Principle**: Name the principle with a clickable markdown link to the exact reference file:
   * e.g., `[Principle 13: Avoiding Total Ground-Up Rewrites](file:///Users/neerav/Documents/Projects/skills/coders-at-work/references/coders-experience.md)`
   * e.g., `[Principle 8: Contextual Fit & Transition Points](file:///Users/neerav/Documents/Projects/skills/coders-at-work/references/vibe-coding-vs-ai-assisted-coding.md)`
6. **💡 Rule of Thumb / Takeaway**: A memorable 1-2 sentence heuristic.
7. **Verdict**: Mark as `Mastered`, `Partially Mastered`, or `Gap Identified`.

Then provide an **Overall Quiz Summary**:
* **Score**: Numerical score (e.g., `4/5`).
* **Progress & Improvement**: Compare against past attempts recorded in [quizzes/](file:///Users/neerav/Documents/Projects/skills/coders-at-work/quizzes/README.md) (e.g., whether previously identified blind spots were resolved).
* **Key Learnings**: 2-3 actionable lessons reinforced in this session.

#### Step 6: Persist Quiz Log to `coders-at-work/quizzes/`
Immediately write a new log file to `coders-at-work/quizzes/YYYY-MM-DD-quiz-<topic-slug>.md` using the schema in [coders-at-work/quizzes/README.md](file:///Users/neerav/Documents/Projects/skills/coders-at-work/quizzes/README.md).
The log file must record:
- Date, Quiz ID, Topics tested.
- Overall Score and Improvement Notes.
- All 5 questions, the user's raw answers, evaluations, and principle links.
- Key takeaways and items to revisit.

Notify the user that the quiz is complete and provide a clickable markdown link to the newly generated quiz log file so they can mark their task complete.

---

### Mode 2: Code & Architecture Reviewer

When reviewing user code, PR diffs, or architecture designs:
1. Read the target code and relevant reference files.
2. Evaluate against key craft criteria:
   * **Scope & Incrementality**: Does it avoid premature rewrites? ([Principle 13](file:///Users/neerav/Documents/Projects/skills/coders-at-work/references/coders-experience.md))
   * **Transition Hardening**: If moving past prototype, are types, contracts, error states, and telemetry hardened? ([Principle 8](file:///Users/neerav/Documents/Projects/skills/coders-at-work/references/vibe-coding-vs-ai-assisted-coding.md))
   * **Cognitive Debt & Over-Reliance**: Is the code clean, understandable, and free of unneeded AI boilerplate? ([Principle 9](file:///Users/neerav/Documents/Projects/skills/coders-at-work/references/vibe-coding-vs-ai-assisted-coding.md))
   * **Usability & Shipping**: Does it get to a usable, testable state fast? ([Principle 14 & 16](file:///Users/neerav/Documents/Projects/skills/coders-at-work/references/coders-experience.md))
3. Format feedback with specific code citations, principle links, and actionable refactoring suggestions.
