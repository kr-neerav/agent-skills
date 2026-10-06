# The Knowing-Doing Gap - Quiz History

This directory stores historical records of completed 5-question quizzes for [knowing-doing-gap](file:///Users/neerav/Documents/Projects/skills/knowing-doing-gap/SKILL.md).

## Purpose
1. **Prevent Repeated Questions**: Every new quiz run scans existing logs in this directory to avoid reusing previously tested scenarios or principles.
2. **Track Learning Progress**: Logs capture the exact scenarios presented, the user's answers, strengths, blind spots, and scores over time.
3. **Reinforce Weak Areas**: Identifies principles and traps where previous answers revealed gaps so future quizzes can test retention with fresh scenarios.

## File Naming Convention
Files are named using the date and topic slug:
`YYYY-MM-DD-quiz-<topic-slug>.md`
Example: `2026-10-05-quiz-smart-talk-and-fear-barriers.md`

## Quiz Log Schema
Each quiz log must follow this structure:

```markdown
# Quiz Log: YYYY-MM-DD - [Topic Slug]

- **Date**: YYYY-MM-DD
- **Skill**: knowing-doing-gap
- **Score**: X / 5
- **Principles & Notes Tested**:
  1. [Principle / Note Title](file:///Users/neerav/Documents/Projects/skills/knowing-doing-gap/references/...)
  2. ...

## Questions, User Answers & Evaluations

### Question 1: [Scenario Title]
* **Scenario**: [Full scenario text]
* **User Answer**: [User's response]
* **Model Answer**: [Recommended operational course of action grounded in principles and notes]
* **Comparative Rating**: [Rating e.g. Strong Alignment (90%) and comparison breakdown vs model answer]
* **Evaluation**:
  - **Strengths**: [What was diagnosed correctly]
  - **Blind Spots & Overlooked Risks**: [What execution traps were missed]
  - **Reference Principle / Note**: [Clickable link to framework or reading notes]
  - **Takeaway**: [1-2 sentence heuristic]
* **Verdict**: Mastered | Partially Mastered | Gap Identified

[Repeat for Questions 2 through 5]

## Overall Learnings & Progress
- **Score Summary**: X/5 (Y%)
- **Comparison to Past Quizzes**: [Trends, persistent gaps, resolved weaknesses]
- **Key Takeaways**: [Summary of core execution principles reinforced]
- **Follow-up Targets**: [Specific traps to re-test in next quiz]
```
