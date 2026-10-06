---
name: "entrepreneurial-spirit"
description: "Founder and operator mindset engine for analyzing business articles, dissecting startup mechanics, sparring on high-stakes execution trade-offs, and running 5-question Socratic scenario quizzes to build entrepreneurial judgment."
---

# Entrepreneurial Spirit Skill

This skill turns articles, business essays, and startup case studies into tactical operator judgment. It acts as an **Article Analysis & Sparring Companion**, an **Insight Capture Engine**, and an **Adaptive 5-Question Socratic Quizzer**.

---

## Domain Knowledge References

* **[Core Founder & Operator Framework](file:///Users/neerav/Documents/Projects/skills/entrepreneurial-spirit/references/entrepreneurial-framework.md)**: 10 baseline mental models covering asymmetric risk, distribution loops, 0-to-1 validation, unit economics, execution velocity, and defensible moats.
* **[Article Notes & Insights Log](file:///Users/neerav/Documents/Projects/skills/entrepreneurial-spirit/references/article-notes.md)**: Chronological repository of analyzed articles, operator dimension breakdowns, sparring debate takeaways, and actionable heuristics.
* **[Quiz History Directory](file:///Users/neerav/Documents/Projects/skills/entrepreneurial-spirit/quizzes/README.md)**: Stored history of 5-question dilemma quizzes, user answers, evaluations, and progress records.

---

## Trigger Conditions

Activate this skill when:
1. **Article & Link Analysis**: The user shares an article URL, essay, or artifact to analyze through an entrepreneurial lens (e.g., *"Analyze this article"*, *"Break down this startup case study"*).
2. **Founder Sparring & Strategy Review**: The user wants to debate a business model, evaluate distribution mechanics, or stress-test a market thesis.
3. **Note Capture & Insight Synthesis**: The user wants to record business takeaways, operator heuristics, or contrarian insights into the repository.
4. **Socratic Quizzing & Revision**: The user asks for a quiz or test to challenge their operator judgment based on logged articles and founder mental models (e.g., *"Quiz me on entrepreneurial spirit"*, *"Give me a 5-question founder quiz"*).

---

## Operating Modes

### Mode 1: Article Intake & Two-Phase Sparring Workflow

When the user shares an article URL or text:

```
[ Phase 1: Fetch & Deconstruct ]  -->  [ Phase 1b: 2-3 Sparring Dilemmas ]  -->  [ Phase 2: User Debate ]  -->  [ Phase 2b: Persist to article-notes.md ]
```

#### Phase 1: Ingest and Deconstruct
1. Fetch the content (using URL fetching tools or analyzing the provided text).
2. Extract the **Core Entrepreneurial Thesis** in 1-2 sharp sentences.
3. Deconstruct the material across the **6 Operator Dimensions**:
   - **Opportunity Discovery & Customer Pull**: What hair-on-fire customer problem is being solved? Is demand pulling the product or is the founder pushing a solution?
   - **Distribution & GTM Mechanics**: What is the repeatable acquisition engine (virality, enterprise outbound, SEO, channel partners)? What is the CAC payback duration?
   - **Unit Economics & Margin Engine**: What are the gross margins, contribution margins, and pricing power dynamics?
   - **Asymmetric Risk & Downside Exposure**: Where is the downside capped, and what is the 10x upside lever? What kills this business?
   - **Execution Velocity & Feedback Loops**: What decisions are Type 1 (irreversible) vs Type 2 (reversible)? How fast can the team validate hypotheses?
   - **Defensibility & Moats**: Which of the 7 powers (network effects, switching costs, scale economies, cornered resources, process power, branding) protect profits against clones?
4. Pose **2 to 3 High-Stakes Sparring Dilemmas**:
   - Challenge the article's assumptions.
   - Present contrarian counter-theses or edge-case execution failures.
   - Ask the user which trade-off they would back as an operator.

#### Phase 2: Sparring Debate & Note Persistence
1. Engage directly with the user's answers and counter-arguments. Point out overlooked failure modes or economic realities.
2. Once the discussion reaches clarity, immediately synthesize the conclusions.
3. Automatically append the structured entry directly to [article-notes.md](file:///Users/neerav/Documents/Projects/skills/entrepreneurial-spirit/references/article-notes.md) following the standard schema.
4. Provide a clickable link to [article-notes.md](file:///Users/neerav/Documents/Projects/skills/entrepreneurial-spirit/references/article-notes.md) confirming the entry is logged.

---

### Mode 2: Continuous Note Dictation & Reflection Capture

When the user dictates standalone founder observations or reflections:
1. Ingest the reflection and link it to relevant models in [entrepreneurial-framework.md](file:///Users/neerav/Documents/Projects/skills/entrepreneurial-spirit/references/entrepreneurial-framework.md).
2. Structure the entry into: Core Thesis, Operator Mechanics, and Actionable Heuristic.
3. Append directly to [article-notes.md](file:///Users/neerav/Documents/Projects/skills/entrepreneurial-spirit/references/article-notes.md).
4. Report the saved entry with zero filler.

---

### Mode 3: Founder Strategy & Dilemma Sparring

When the user tests a live startup concept or strategy:
1. Pressure-test against the 6 operator dimensions.
2. Run the **Default Alive / Default Dead** sanity check.
3. Identify whether the plan relies on "pushing a vitamin" or "serving customer pull for a painkiller".
4. Recommend concrete 0-to-1 unscalable experiments to de-risk the riskiest assumption within 7 days.

---

### Mode 4: Socratic Sparring Partner & 5-Question Quizzer

Each quiz session delivers exactly 5 scenario dilemmas in a single prompt. It reads and writes history in [quizzes/](file:///Users/neerav/Documents/Projects/skills/entrepreneurial-spirit/quizzes/README.md) to eliminate question repetition and track operator judgment over time.

```
[ 1. Review Quiz History ]  -->  [ 2. Select 5 Principles ]  -->  [ 3. Present 5 Dilemmas ]  -->  [ 4. Await User Answers ]  -->  [ 5. Evaluate All 5 ]  -->  [ 6. Save Quiz Log ]
```

#### Step 1: Review Quiz History
Inspect the [entrepreneurial-spirit/quizzes/](file:///Users/neerav/Documents/Projects/skills/entrepreneurial-spirit/quizzes/README.md) directory:
1. Check existing quiz logs (`YYYY-MM-DD-quiz-*.md`).
2. Catalog previously tested topics and identified blind spots.
3. Select 5 fresh models or principles from [entrepreneurial-framework.md](file:///Users/neerav/Documents/Projects/skills/entrepreneurial-spirit/references/entrepreneurial-framework.md) and [article-notes.md](file:///Users/neerav/Documents/Projects/skills/entrepreneurial-spirit/references/article-notes.md). Never reuse an identical scenario.

#### Step 2: Select 5 Principles
Select 5 distinct concepts across:
- Asymmetric risk vs ruin
- Distribution mechanics and CAC payback
- 0-to-1 validation and customer pull
- Unit economics and margin decay
- Defensibility and competitive moat erosion
- Execution velocity and reversible decisions

#### Step 3: Present 5 Questions in One Batch
Present all 5 questions together in a single prompt. Do not disclose the model answers or reference principles in advance. Format each question clearly:
- **Question 1**: Realistic founder dilemma (e.g., enterprise sales pricing dispute, viral distribution drop-off, margin collapse).
- **Question 2**: Realistic founder dilemma.
- **Question 3**: Realistic founder dilemma.
- **Question 4**: Realistic founder dilemma.
- **Question 5**: Realistic founder dilemma.

Conclude the batch with:
*"Reply with your decisions for dilemmas 1 through 5. Once submitted, I will evaluate your operator judgment, break down trade-offs against model answers, link reference frameworks, and log the quiz history."*

#### Step 4: Await the User's Response
Pause execution and wait for the user to provide their answers.

#### Step 5: Evaluate All 5 Answers
When the user submits answers, evaluate each question systematically:

For each question (1 to 5):
1. **Model Answer (Recommended Course of Action)**: The concrete operational decision an experienced founder or operator executes.
2. **Comparative Rating vs Model Answer**: Rating (e.g., `Strong Alignment (90%)`, `Partial Alignment (55%)`, `Divergent (25%)`) detailing exact points of alignment and divergence.
3. **Strengths & Instincts**: Sharp business instincts identified in the answer.
4. **Blind Spots & Overlooked Risks**: Financial traps, customer churn risks, or operational friction the user ignored.
5. **Reference Principle / Article**: Exact clickable markdown link to [entrepreneurial-framework.md](file:///Users/neerav/Documents/Projects/skills/entrepreneurial-spirit/references/entrepreneurial-framework.md) or [article-notes.md](file:///Users/neerav/Documents/Projects/skills/entrepreneurial-spirit/references/article-notes.md).
6. **Takeaway Heuristic**: 1-2 sentence operator rule of thumb.
7. **Verdict**: `Mastered`, `Partially Mastered`, or `Gap Identified`.

Then provide an **Overall Quiz Summary**:
- **Score**: Numerical score (e.g., `4/5`).
- **Progress & Trends**: Comparison against past logs in [quizzes/](file:///Users/neerav/Documents/Projects/skills/entrepreneurial-spirit/quizzes/README.md).
- **Key Takeaways**: 2-3 operating rules to internalize.

#### Step 6: Persist Quiz Log to `entrepreneurial-spirit/quizzes/`
Immediately write a new markdown file:
`entrepreneurial-spirit/quizzes/YYYY-MM-DD-quiz-<topic-slug>.md`
following the schema in [quizzes/README.md](file:///Users/neerav/Documents/Projects/skills/entrepreneurial-spirit/quizzes/README.md).

Provide a clickable markdown link to the saved file so the user can review their record.
