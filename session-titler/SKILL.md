---
name: "session-titler"
description: "Update session titler skill to use CLI instead of sessions_list for visibility"
---

# Session Titler Skill

## Description
A background task that periodically scans for new or unnamed sessions, analyzes their first message using an LLM, and assigns a human-readable, unique title.

## Behavior

### 1. Identification
The agent looks for sessions that meet these criteria:
- The session lacks a custom title (derivedTitle).
- The current session title is the default (e.g., a UUID or "New Chat").
- The last activity was an assistant response (ensuring the first turn is complete).

*Note: Because of OpenClaw's session visibility restrictions (tools.sessions.visibility=tree), the agent MUST use the CLI `openclaw sessions list --json` via the `exec` tool to find sessions, rather than the `sessions_list` tool.*

### 2. Title Generation
The agent reads the first user message by parsing the session transcript from `~/.openclaw/agents/main/sessions/<sessionId>.jsonl` using the `exec` tool (e.g., `grep '"role":"user"' ... | head -n 1`). It analyzes the content using an LLM (typically a lightweight local model) and generates a concise, friendly, and descriptive title for the chat session.

### 3. Execution (Renaming)
Since OpenClaw does not yet have a native API tool for agents to directly rename sessions, this skill uses a dedicated Node.js script located at `scripts/rename_session.js`. 
The agent executes this script via the `exec` tool:
`node /Users/neerav/Documents/Projects/scripts/rename_session.js "<sessionKey>" "<newTitle>"`

The script reads the Gateway's `sessions.json` file, applies the generated title as the session's `label`, and saves it. The UI immediately uses this `label` as the display title.

## Implementation Strategy
This runs as a periodic background `cron` job via the Gateway, checking for un-titled sessions every 30 minutes.

## Example
*   **User Input:** "How do I bake a chocolate cake?"
*   **LLM Suggestion:** "Chocolate Cake Baking"
*   **Action:** Exec `node scripts/rename_session.js "agent:main:dashboard:xyz123" "Chocolate Cake Baking"`
