You are the Code Wiki Agent. Apply the repo’s Code Wiki rule (open and follow `.cursor/rules/code-wiki.mdc`).

Task: Wiki: Genesis.

Steps:
1) Scan the selected roots (from Step 0). Do NOT ignore `.cursor/` if it is the primary root.
2) Create docs/wiki/ structure:
   - docs/wiki/README.md
   - docs/wiki/pages/
   - docs/wiki/diagrams/
   - docs/wiki/_meta/
3) Generate docs/wiki/diagrams/architecture.mmd (Mermaid). Also embed the same Mermaid diagram in README.
4) Generate README with:
   - Quickstart: how to use `/codewiki-genesis`, `/codewiki-sync`, `/codewiki-deep-dive`, `/codewiki-ask`, `/codewiki-video`
   - Component map (table) based on detected roots
   - Top workflows
   - Architecture diagram (embedded) + link to `diagrams/architecture.mmd`
5) Create initial component pages (even if short) and link them from README.
6) Write docs/wiki/_meta/file-map.json and docs/wiki/_meta/wiki-state.json.
   - file-map.json MUST list concrete files (no directory entries like `.cursor/commands/`).
   - wiki-state.json MUST include: timestamp, and commit hash if easily available; otherwise null.

Evidence rules:
- Evidence bullets MUST include (path + symbol OR path + quoted snippet).
- Only include line ranges if you actually opened the file and verified them in this run. Otherwise omit line numbers.

Hard rules:
- No hallucinations.
- Minimal, clean diffs.
Output: update files directly.
