# Component: Core Rules

## Purpose
The **Core Rules** component defines the behavior, style, and output format for the Code Wiki Agent. It serves as the "brain" of the documentation system, ensuring consistency across all generated wiki pages.

## Entry Points
- The rule is applied when the user invokes any of the `codewiki-*` commands or explicitly triggers the agent.
- Defined in [.cursor/rules/code-wiki.mdc](../../.cursor/rules/code-wiki.mdc).

## Key Responsibilities
1.  **Philosophy Enforcement**: Enforces "Code is Source of Truth" and "Zero Hallucination".
2.  **Output Structuring**: Dictates the `docs/wiki/` directory structure.
3.  **Analysis Capabilities**: Defines how to scan imports, trace data flow, and identify invariants.
4.  **Formatting**: Specifies the Markdown structure, evidence blocks, and diagramming rules.
5.  **State Management**: Defines how to maintain `_meta/file-map.json` and `_meta/wiki-state.json`.

## Key Code Locations
- [.cursor/rules/code-wiki.mdc](../../.cursor/rules/code-wiki.mdc): The single source of truth for the agent's instructions.
    - **Section 0**: Core Philosophy.
    - **Section 1**: Output Location.
    - **Section 4**: Wiki Page Template.
    - **Section 6**: Incremental Sync.

## Invariants / Assumptions
- **Assumption**: The agent has read access to the entire repository.
- **Assumption**: The user uses a Markdown-compatible viewer (like Cursor's preview or GitHub).
- **Invariant**: Every claim in the wiki must be backed by an "Evidence" section.

## Evidence
- `.cursor/rules/code-wiki.mdc` — `Role: Code Wiki Agent` — Defines the persona.
- `.cursor/rules/code-wiki.mdc` — `Zero hallucination` — Defines the core constraint.
