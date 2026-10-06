# Coders at Work - Quiz History

This directory stores historical records of completed 5-question quizzes for [coders-at-work](file:///Users/neerav/Documents/Projects/skills/coders-at-work/SKILL.md).

## Purpose
1. **Prevent Repeated Questions**: Every new quiz run scans existing logs in this directory to avoid reusing previously tested scenarios or principles.
2. **Track Learning Progress**: Logs capture the exact scenarios presented, the user's answers, strengths, blind spots, and scores over time.
3. **Reinforce Weak Areas**: Identifies principles where previous answers revealed blind spots so future quizzes can test retention with fresh scenarios.

## File Naming Convention
Files are named using the date and topic slug:
`YYYY-MM-DD-quiz-<topic-slug>.md`
Example: `2026-10-05-quiz-strangler-fig-and-vibe-transitions.md`

## Quiz Log Schema
Each quiz log must follow this structure:

```markdown
# Quiz Log: YYYY-MM-DD - [Topic Slug]

- **Date**: YYYY-MM-DD
- **Skill**: coders-at-work
- **Score**: X / 5
- **Principles Tested**:
  1. [Principle Name](file:///Users/neerav/Documents/Projects/skills/coders-at-work/references/...)
  2. ...

## Questions, User Answers & Evaluations

### Question 1: [Scenario Title]
* **Scenario**: [Full scenario text]
* **User Answer**: [User's response]
* **Model Answer**: [Recommended course of action grounded in principle]
* **Comparative Rating**: [Rating e.g. Strong Alignment (90%) and comparison breakdown vs model answer]
* **Evaluation**:
  - **Strengths**: [What was identified correctly]
  - **Blind Spots & Overlooked Risks**: [What was missed]
  - **Reference Principle**: [Clickable link to reference file]
  - **Takeaway**: [1-2 sentence heuristic]
* **Verdict**: Mastered | Partially Mastered | Gap Identified

[Repeat for Questions 2 through 5]

## Overall Learnings & Progress
- **Score Summary**: X/5 (Y%)
- **Comparison to Past Quizzes**: [Trends, persistent gaps, resolved weaknesses]
- **Key Takeaways**: [Summary of core principles reinforced]
- **Follow-up Targets**: [Specific principles to re-test in next quiz]
```
