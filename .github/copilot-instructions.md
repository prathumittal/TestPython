## Goal for AI coding agents

Be minimal and concrete: this repository contains three tiny Python scripts (learning/examples). Your edits should be focused, low-risk, and directly tied to the user's request.

## Big picture (what this repo is)
- Location: repository root contains three Python programs: `MyFirstProgram.py`, `MySecondProgram.py`, and `ThirdProgram.py`.
- Purpose: simple demonstration scripts that print to stdout. There is no packaging, tests, or CI present.

## How to run locally (Windows PowerShell)
- Run a single file:

```powershell
python .\MyFirstProgram.py
# or
py .\MyFirstProgram.py
```

- Run all .py files quickly (PowerShell):

```powershell
Get-ChildItem -Filter *.py | ForEach-Object { python $_.Name }
```

## Repo-specific patterns and examples
- The programs are plain scripts that perform prints. Example (from `MyFirstProgram.py`):

- When modifying or adding code, prefer adding new modules at repo root and keep file names descriptive (e.g., `NewFeature.py`).
- Keep changes minimal: many files are single-purpose scripts; large refactors are unexpected unless requested.

## What the AI should do when asked to implement changes
- If asked to add behavior, create a new file or update the requested script only. Include a short comment at the top describing intent.
- Preserve existing output lines unless the user asks to change them — these prints appear to be the main observable behavior.
- If adding runnable code, include a minimal verification (e.g., a short run instruction in the commit message or in the file's header comment).

## Integration points & external dependencies
- None detected. The scripts use only the Python standard runtime (print statements). Do not add external dependencies without explicit instructions.

## Commit / PR guidance for AI
- Use small commits. Example commit message style: `feat: add <short description>` or `fix: correct <file>`.
- If adding examples or new scripts, update the repository README (if present) to reference them.

## Files to inspect for context
- `MyFirstProgram.py` — simple prints (greeting strings).
- `MySecondProgram.py` — prints and small iterative comment lines used during branching experiments.
- `ThirdProgram.py` — another small script printing a single line.

## When to ask for clarification
- Ask the user if they want: tests, packaging (setup/requirements), or CI integration. These are not present and require specification.

---
If any section is unclear or you want the instructions tailored for a different agent style (more prescriptive tests, or acceptance criteria), tell me which parts to expand or modify.
