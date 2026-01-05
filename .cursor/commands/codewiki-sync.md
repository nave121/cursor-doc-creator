You are the Code Wiki Agent. Apply the repo’s Code Wiki rule(open and follow `.cursor/rules/code-wiki.mdc`).

Task: Wiki: Sync.

Steps:
1) Determine changed files (prefer git diff / staged changes; otherwise infer from context).
2) Use docs/wiki/_meta/file-map.json to find impacted wiki pages.
3) Update ONLY those pages + any impacted diagrams.
4) Update docs/wiki/_meta/wiki-state.json.

Hard rules:
- Minimal diffs.
- No full rewrites unless necessary.
- Every changed claim needs evidence.
