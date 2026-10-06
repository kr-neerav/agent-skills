# Generations - Quiz History

This directory stores historical records of completed 5-question quizzes for [generations](file:///Users/neerav/Documents/Projects/skills/generations/SKILL.md).

## Purpose
1. **Prevent Repeated Questions**: Every new quiz run scans existing logs in this directory to avoid reusing previously tested scenarios or archetypal dynamics.
2. **Track Learning Progress**: Logs capture the exact scenarios presented, the user's answers, strengths, blind spots, and scores over time.
3. **Reinforce Weak Areas**: Identifies archetypes, turnings, and lifecycle dynamics where previous answers revealed blind spots so future quizzes can test retention with fresh scenarios.

## File Naming Convention
Files are named using the date and topic slug:
`YYYY-MM-DD-quiz-<topic-slug>.md`
Example: `2026-10-05-quiz-nomad-hero-leadership-clashes.md`

## Quiz Log Schema
Each quiz log must follow this structure:

```markdown
# Quiz Log: YYYY-MM-DD - [Topic Slug]

- **Date**: YYYY-MM-DD
- **Skill**: generations
- **Score**: X / 5
- **Concepts & Notes Tested**:
  1. [Concept / Note Title](file:///Users/neerav/Documents/Projects/skills/generations/references/...)
  2. ...

## Questions, User Answers & Evaluations

### Question 1: [Scenario Title]
* **Scenario**: [Full scenario text]
* **User Answer**: [User's response]
* **Model Answer**: [Recommended leadership intervention grounded in generational theory]
* **Comparative Rating**: [Rating e.g. Strong Alignment (90%) and comparison breakdown vs model answer]
* **Evaluation**:
  - **Strengths**: [What generational instincts were identified accurately]
  - **Blind Spots & Overlooked Dynamics**: [What lifecycle or turning mechanics were missed]
  - **Reference Theory / Note**: [Clickable link to references]
  - **Takeaway**: [1-2 sentence heuristic]
* **Verdict**: Mastered | Partially Mastered | Gap Identified

[Repeat for Questions 2 through 5]

## Overall Learnings & Progress
- **Score Summary**: X/5 (Y%)
- **Comparison to Past Quizzes**: [Trends, persistent gaps, resolved weaknesses]
- **Key Takeaways**: [Summary of core generational principles reinforced]
- **Follow-up Targets**: [Specific concepts to re-test in next quiz]
```
