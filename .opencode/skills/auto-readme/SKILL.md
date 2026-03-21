---
name: auto-readme
description: Auto-generate and update README.md based on repo structure, skills, commands, and git changes. Triggers automatically before git push.
license: MIT
compatibility: opencode
metadata:
  audience: developers
  workflow: documentation
---

## What I do

Automatically generate/update README.md when pushing to GitHub by:
1. Scanning repo structure (files, folders, skills, commands, plugins)
2. Detecting git changes since last commit
3. Reading version info from package.json
4. Detecting available commands from `.opencode/commands/`
5. Detecting skills from `.opencode/skills/*/SKILL.md`
6. Generating clean markdown documentation

## Trigger conditions

**Auto-trigger (any of):**
- Before `git push` operation detected
- Version bump scripts detected changes
- New skills/commands added
- After significant file changes in `.opencode/`

**Skip conditions:**
- Repo has no `.opencode/` directory
- No significant changes detected
- README.md was manually updated recently

## Output rules

Generate README with these sections:
1. Title block with repo name and version
2. Description from package.json or opencode.json
3. Auto-detected commands list
4. Auto-detected skills list
5. File structure tree map
6. Scripts section (if package.json exists)
7. Quick start instructions

## Integration

This skill works alongside task-workflow to auto-update docs before pushes.
