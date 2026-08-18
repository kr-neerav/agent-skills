---
name: "prompt-driven-development"
description: "A meta-agent skill that guides users through a Prompt-Driven Development (PDD) workflow to turn rough ideas into detailed designs and implementation plans."
---

# Prompt-Driven Development (PDD) Meta-Agent

## Trigger
Use this skill when the user asks to start a Prompt-Driven Development (PDD) workflow, act as a meta-agent, create a detailed design and implementation plan from a rough idea, or explicitly invokes the PDD meta-agent.

## Overview
This skill guides you through the process of transforming a rough idea into a detailed design document with an implementation plan and todo list. It follows the Prompt-Driven Development methodology to systematically refine the idea, conduct necessary research, create a comprehensive design, and develop an actionable implementation plan. The process is designed to be iterative, allowing movement between requirements clarification and research as needed.

## Parameters

When starting the process, acquire the following parameters:
- **rough_idea** (required): The initial concept or idea you want to develop into a detailed design
- **project_dir** (optional, default: "planning"): The base directory where all project files will be stored
- **checkpointing** (optional, default: "false"): Enable progress checkpointing during implementation. Options:
  - "false" or "none": No checkpointing (default)
  - "notes-only" or "notes": Create checkpoint notes only
  - "git-only" or "git": Create git commits only
  - "both": Create both checkpoint notes and git commits

**Constraints for parameter acquisition:**
- You MUST ask for all required parameters upfront in a single prompt rather than one at a time.
- You MUST support multiple input methods including direct text input, file path, URL, or other accessible resources.
- You MUST use appropriate tools (e.g., `read`, `web_fetch`) to access content based on the input method.
- You MUST confirm successful acquisition of all parameters before proceeding.
- You SHOULD save the acquired rough idea to a consistent location for use in subsequent steps.
- You MUST NOT overwrite the existing project directory to prevent data loss.
- You MUST ask for `project_dir` if it is not given and the default "planning" directory already exists and has contents from a previous iteration.

## Steps

### 1. Create Project Structure

Set up a directory structure to organize all artifacts created during the process.

**Constraints:**
- You MUST create the specified project directory if it doesn't already exist.
- You MUST create the following files (using `write`):
  - `{project_dir}/rough-idea.md` (containing the provided rough idea)
  - `{project_dir}/idea-honing.md` (for requirements clarification)
- You MUST create the following subdirectories:
  - `{project_dir}/research/` (directory for research notes)
  - `{project_dir}/design/` (directory for design documents)
  - `{project_dir}/implementation/` (directory for implementation plans)
- You MUST notify the user when the structure has been created.
- You MUST prompt the user to ensure these files are tracked or available in their context.

### 2. Initial Process Planning

Determine the initial approach and sequence for requirements clarification and research.

**Constraints:**
- You MUST ask the user if they prefer to:
  - Start with requirements clarification (default)
  - Start with preliminary research on specific topics
  - Provide additional context or information before proceeding
- You MUST adapt the subsequent process based on the user's preference.
- You MUST explain that the process is iterative.
- You MUST wait for explicit user direction before proceeding to any subsequent step.

### 3. Requirements Clarification

Guide the user through a series of questions to refine the initial idea and develop a thorough specification.

**Constraints:**
- You MUST create an empty `{project_dir}/idea-honing.md` file if it doesn't already exist.
- You MUST ask ONLY ONE question at a time and wait for the user's response before asking the next.
- You MUST NOT list multiple questions at once.
- You MUST NOT pre-populate answers.
- You MUST follow this exact process for each question:
  1. Formulate a single question.
  2. Append the question to `{project_dir}/idea-honing.md`.
  3. Present the question to the user in the conversation.
  4. Wait for the user's complete response.
  5. Append the user's answer (or final decision) to `{project_dir}/idea-honing.md`.
  6. Only then proceed to formulating the next question.
- You MUST continue asking questions until sufficient detail is gathered (cover edge cases, UX, technical constraints, success criteria).
- You MUST explicitly ask the user if they feel the requirements clarification is complete before moving to the next step.
- You MUST offer the option to conduct research if questions arise.
- You MUST NOT proceed with any other steps until explicitly directed by the user.

### 4. Research Relevant Information

Conduct research on relevant technologies, libraries, or existing code.

**Constraints:**
- You MUST identify areas where research is needed.
- You MUST propose an initial research plan to the user.
- You MUST ask the user for input on the research plan (additional topics, specific resources).
- You MUST document research findings in separate markdown files in the `{project_dir}/research/` directory.
- You MUST include mermaid diagrams when documenting system architectures or component relationships in research.
- You MUST include links to relevant references and sources.
- You MUST periodically check with the user during the research process to share findings and ask for feedback.
- You MUST ask the user if the research is sufficient before proceeding to the next step.
- You MUST wait for the user to decide the next step after completing research.

### 5. Iteration Checkpoint

Determine if further requirements clarification or research is needed before proceeding to design.

**Constraints:**
- You MUST summarize the current state of requirements and research.
- You MUST explicitly ask the user if they want to proceed to detailed design, return to requirements, or conduct additional research.
- You MUST NOT proceed to the design step without explicit user confirmation.

### 6. Create Detailed Design

Develop a comprehensive design document based on the requirements and research.

**Constraints:**
- You MUST create a detailed design document at `{project_dir}/design/detailed-design.md`.
- You MUST include the following sections: Overview, Detailed Requirements (consolidated), Architecture Overview, Components and Interfaces, Data Models, Error Handling, Testing Strategy, Appendices.
- You MUST include mermaid diagrams for architectural overviews, data flow, and component relationships.
- You MUST review the design with the user and iterate based on feedback.

### 7. Develop Implementation Plan

Create a structured implementation plan with a series of steps.

**Constraints:**
- You MUST create an implementation plan at `{project_dir}/implementation/plan.md`.
- You MUST include a checklist at the beginning.
- You MUST format the plan as a numbered series of detailed steps.
- Each step MUST begin with "Step N:" and include:
  - A clear objective
  - General implementation guidance
  - Test requirements
  - Integration with previous work
  - **Demo** - explicit description of working functionality
- You MUST ensure each step results in working, demoable functionality.
- You MUST sequence steps so that core end-to-end functionality is available as early as possible.
- If checkpointing is enabled, You MUST include checkpoint instructions (see Step 7.1).

### 7.1. Add Checkpoint Instructions (if checkpointing enabled)

If the user enabled checkpointing, add instructions to the implementation plan.
- **For Notes Checkpointing**: Add instructions to create a checkpoint file at `{project_dir}/implementation/checkpoint-step-N-complete.md` documenting Completed Work, Technical Details, Test Results, Next Steps, and Files Status.
- **For Git Checkpointing**: Add instructions to create descriptive git commits (`git add src/ test/`, `git commit -m "feat: implement [description]..."`).

### 8. Summarize and Present Results

Provide a summary of all artifacts created and next steps.

**Constraints:**
- You MUST create a summary document at `{project_dir}/summary.md`.
- You MUST list all artifacts created.
- You MUST provide a brief overview of the design and implementation plan.
- You MUST present this summary to the user.

### 9. Implementation Checkpoint Execution (if checkpointing enabled)

Execute checkpointing during the implementation phase when following the prompt plan.

**Constraints:**
- You MUST create checkpoints after completing each step.
- You MUST follow the instructions created in Step 7.1.

## Troubleshooting
- **Clarification Stalls**: Suggest moving to a different aspect, provide examples, or suggest research.
- **Research Limitations**: Document missing information, suggest alternative approaches, and continue with available info.
- **Design Complexity**: Suggest breaking it down into smaller components or a phased approach.
