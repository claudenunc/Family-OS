# Repository verification

These are repository checks, not application tests. Run PowerShell from the
repository root. A successful command must have a zero exit code unless noted.

## Local state

```powershell
git rev-parse --show-toplevel
git remote get-url origin
git branch --show-current
git status --short --branch
git log -1 --format=fuller
git ls-files
git diff --check
git diff --cached --check
Get-Content -LiteralPath AGENTS.md
Get-Content -LiteralPath .agents/skills/task-planning/SKILL.md
```

Expect the intended checkout, origin
https://github.com/claudenunc/Family-OS.git, branch main, and the foundation files.
A clean working tree should have no file changes. Empty src/ and tests/ are retained
using .gitkeep, which has no special runtime meaning.

## Exclusions

```powershell
git check-ignore --no-index -- .env .env.local .venv/example node_modules/example .local/private.txt memory/runtime/session.json private/example.txt "FAMILY OS Architecture Research.docx" "Open Source AI Capability System.docx"
git check-ignore --no-index -- AGENTS.md README.md .agents/skills/task-planning/SKILL.md docs/ROADMAP.md src/example.py tests/example.test.ts
```

The first command must print every listed sensitive/generated example and return
0. The second must print nothing and return 1: these project files must remain
trackable. Also review exact staged filenames and contents for secrets or personal
data; pattern checks alone cannot prove that arbitrary content is safe.

The original reports can be checked for preservation using their SHA-256 values in
[the research index](../../research/README.md).

## Skill format and behavior

If the host provides skill-creator, run its scripts/quick_validate.py against
.agents/skills/task-planning using an available Python with its required YAML
library. Do not install packages just to inspect this foundation.

Also verify matching folder/name, non-empty name and description, valid YAML,
draft metadata, and complete instructions. The bundled format validator is not a
behavioral evaluation. Use [skill validation](skill-validation.md) before promotion.

## GitHub publication

After the reviewed commit and authorized push:

```powershell
git fetch origin
git rev-parse HEAD
git rev-parse origin/main
git ls-remote origin refs/heads/main
git ls-tree -r --name-only origin/main
git diff --exit-code HEAD origin/main
git status --porcelain
```

The local HEAD, fetched origin/main, and live remote main must name the same
commit. Compare the remote file list with the reviewed local manifest; verify file
contents as well. A fresh fetch must succeed before treating origin/main as current.
If publication fails, report it explicitly rather than claiming setup completion.

Never force-push or replace existing project files to make these checks pass.
