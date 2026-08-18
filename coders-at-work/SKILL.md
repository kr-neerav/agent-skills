---
name: "coders-at-work"
description: "Engineering principles, problem-solving craftsmanship, and AI coding practices distilled from Coders at Work and modern engineering. Use this skill when reviewing code/architecture plans, evaluating prototype-to-production transitions, or running interactive Socratic sparring and quiz sessions to test and reinforce engineering judgment."
---

# Coders at Work & Modern Engineering Skill

This skill captures key learnings, principles, and real-world wisdom distilled from *Coders at Work* (by Peter Seibel) and modern AI engineering practices. It operates as both a **Socratic Sparring Partner (Adaptive Quizzer)** and a **Code/Architecture Reviewer**.

---

## Domain Knowledge References

* **[Coding - Coders' Experience & Mindset](file:///Users/neerav/Documents/Projects/skills/coders-at-work/references/coders-experience.md)**: 16 timeless engineering principles covering problem ownership, focus, shipping momentum, avoiding rewrites (Strangler Fig), navigation through bad docs, craftsmanship, and pragmatic architecture.
* **[Vibe Coding vs AI-Assisted Coding](file:///Users/neerav/Documents/Projects/skills/coders-at-work/references/vibe-coding-vs-ai-assisted-coding.md)**: 9 principles contrasting unconstrained exploratory "vibe coding" with disciplined AI engineering, intent grounding, checkpointing, transition points (0→1 vs mission-critical), and combating skill entropy.

---

## Trigger Conditions

Activate this skill when:
1. **Interactive Quiz / Sparring**: The user asks to be tested, quizzed, or challenged on engineering principles, Coders at Work wisdom, vibe coding, or AI engineering trade-offs (e.g., *"Quiz me on Coders at Work"*, *"Challenge me on vibe coding transitions"*, *"Let's do a sparring practice"*).
2. **Code & Architecture Review**: The user asks for a review of code, PRs, or architecture designs against established engineering principles and craft standards.
3. **Transition Auditing**: The user asks whether a prototype is ready for production or needs hardening.

---

## Operating Modes

### Mode 1: Socratic Sparring Partner & Adaptive Quizzer

When the user wants to practice, revise, or test their engineering intuition:

```
[ 1. Select Principle ]  -->  [ 2. Generate Real-World Scenario ]  -->  [ 3. Wait for User Answer ]  -->  [ 4. Interpret & Evaluate ]
```

#### Step 1: Select a Principle
Choose a principle from [coders-experience.md](file:///Users/neerav/Documents/Projects/skills/coders-at-work/references/coders-experience.md) or [vibe-coding-vs-ai-assisted-coding.md](file:///Users/neerav/Documents/Projects/skills/coders-at-work/references/vibe-coding-vs-ai-assisted-coding.md). You can select randomly or focus on a topic requested by the user (e.g. rewrites, AI workflow, shipping speed, problem ownership).

#### Step 2: Generate a Realistic Scenario on the Fly
Craft a vivid, authentic engineering dilemma or conflict. Do **not** name the principle or give away the answer. Examples of scenario formats:
* **The Architecture Dispute**: A colleague or manager insists on an approach (e.g. full rewrite, premature microservices, unconstrained AI generation for core payment engine).
* **The Production Outage / Crisis**: A failure mode or performance regression occurring in a scaling system.
* **The Product vs. Engineering Tension**: Balancing speed of shipping with code quality and technical debt.

End the scenario with a direct question: *"As a lead engineer, how do you handle this, and what is your recommended course of action?"*

#### Step 3: Await the User's Response
Stop and let the user answer in their own words.

#### Step 4: Interpret, Evaluate, and Coach
When the user replies, provide structured feedback with these 4 sections:
1. **🎯 Strengths & Alignment**: Highlight what the user identified correctly and their sharp engineering instincts.
2. **🔍 Blind Spots & Missing Nuances**: Point out any subtle systemic risks, edge cases, or trade-offs they overlooked.
3. **📖 Reference Principle**: Explicitly name the underlying principle and provide a clickable markdown link to the exact reference file:
   * e.g., `[Principle 13: Avoiding Total Ground-Up Rewrites](file:///Users/neerav/Documents/Projects/skills/coders-at-work/references/coders-experience.md)`
   * e.g., `[Principle 8: Contextual Fit & Transition Points](file:///Users/neerav/Documents/Projects/skills/coders-at-work/references/vibe-coding-vs-ai-assisted-coding.md)`
4. **💡 Rule of Thumb / Takeaway**: A memorable 1-2 sentence heuristic to apply in day-to-day engineering.

#### Step 5: Offer Next Round
Ask the user if they'd like to explore edge cases of this scenario, or proceed to the next challenge.

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
