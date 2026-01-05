# Component: Cursor Commands

## Purpose
The **Cursor Commands** collection provides the interface for the user to interact with the Code Wiki system. Each command file contains a specific prompt that sets the task and context for the Code Wiki Agent.

## Entry Points
- Users invoke these via the Cursor Command Palette (e.g., `/codewiki-genesis`).
- Located in [.cursor/commands/](../../.cursor/commands/).

## Key Responsibilities
- **Task Definition**: Each file defines a specific "Task" (e.g., "Wiki: Genesis", "Wiki: Sync").
- **Step-by-Step Instructions**: Provides precise steps the agent must follow to complete the task.
- **Hard Rules**: Re-iterates critical constraints (e.g., "No hallucinations") specific to the command context.

## Key Code Locations
- [.cursor/commands/codewiki-genesis.md](../../.cursor/commands/codewiki-genesis.md): Initializes the wiki structure.
- [.cursor/commands/codewiki-sync.md](../../.cursor/commands/codewiki-sync.md): Synchronizes docs with code changes.
- [.cursor/commands/codewiki-deep-dive.md](../../.cursor/commands/codewiki-deep-dive.md): Generates deep-dive documentation.
- [.cursor/commands/codewiki-onboard.md](../../.cursor/commands/codewiki-onboard.md): Creates onboarding guides.
- [.cursor/commands/codewiki-ask.md](../../.cursor/commands/codewiki-ask.md): Handles Q&A.
- [.cursor/commands/codewiki-video.md](../../.cursor/commands/codewiki-video.md): Generates video content.

## Key Flows
1.  **Genesis Flow**:
    - User types `/codewiki-genesis`.
    - Cursor loads `codewiki-genesis.md`.
    - Agent executes "Scan repo" -> "Create structure" -> "Generate README".

## Evidence
- `.cursor/commands/codewiki-genesis.md` — `Task: Wiki: Genesis.` — Defines the genesis task.
- `.cursor/commands/` — Directory listing shows all command files.
