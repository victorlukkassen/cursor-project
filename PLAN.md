# Cursor Project Plan

## Objective
Create an AI agent that can see the screen, understand a high-level goal, and use the mouse and keyboard to achieve it.

---

### Phase 1: Core - Visual Control
- **Goal:** Give the agent eyes and hands.
- **Tasks:**
  1.  Implement reliable screen capture.
  2.  Use a vision model to identify UI elements, their positions, and what they do.
  3.  Implement OS-level cursor movement, clicking, and typing.
- **First Test:** "Find the price of the first item on amazon.com for 'coffee maker'."

### Phase 2: The Brain - Planning
- **Goal:** Break down a complex task into a sequence of actions.
- **Tasks:**
  1.  Develop task decomposition logic.
  2.  Create a system to log the plan, current action, and outcome.

### Phase 3: The Team - Multi-Agent System
- **Goal:** Use a hierarchy of agents to manage complex workflows.
- **Tasks:**
  1.  Define an Orchestrator agent (the manager).
  2.  Define Worker agents for specialized tasks (e.g., browsing, image analysis).
  3.  Establish a communication protocol between them.

### Phase 4: The Conscience - Self-Critique
- **Goal:** Build a feedback loop for continuous improvement.
- **Tasks:**
  1.  Create a Validator agent to review work.
  2.  Integrate the feedback into the Orchestrator's planning loop.

---

## Project Log

**2026-01-28:**
- Initialized project, created plan, and pushed to GitHub.
- Installed `cliclick` for mouse control and granted permissions.
- **ROADBLOCK:** Attempts to use the native macOS `screencapture` command are failing. It only captures the desktop wallpaper, not any open application windows. This prevents vision-based analysis.
- **NEXT STEP:** Fall back to using the `browser` tool to get a reliable view of the webpage to complete the first test. The `screencapture` issue will be revisited as a separate technical challenge.
