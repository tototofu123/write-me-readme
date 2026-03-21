---
name: auto-readme
description: Auto-generate and update README.md with rich formatting - tables, emojis, colors, code blocks, and more
license: MIT
compatibility: opencode
metadata:
  audience: developers
  workflow: documentation
---

## What I do

Automatically generate/update README.md with **rich formatting**:
- ✅ Tables for features, scripts, commands
- ✅ Emojis for visual appeal (:rocket:, :book:, :wrench:, etc.)
- ✅ Code blocks with syntax highlighting
- ✅ Bold/italic text for emphasis
- ✅ Badges/shields-style formatting
- ✅ Collapsible sections
- ✅ Badges for CI, license, version
- ✅ Auto-detect repo structure

## Rich Formatting Features

### Available Elements
```
| Tables | are | supported |
|--------|-----|-----------|
| **Bold** | *italic* | `code` |
```

- **Emojis**: :rocket:, :book:, :wrench:, :sparkles:, :warning:, :bulb:
- **Badges**: ![version](badge), ![license](badge)
- **Code blocks**: ```bash, ```javascript, ```json
- **Callouts**: > [!NOTE], > [!TIP], > [!WARNING]

### Output Sections

1. **Header** - Title with emoji, version badge, description
2. **Quick Stats** - Table with repo info (stars, forks, license)
3. **Features** - Bulleted list with emojis
4. **Commands** - Table format
5. **Installation** - Code blocks
6. **File Structure** - Tree with icons
7. **Scripts** - Table format
8. **Badges** - License, version, CI status

## Trigger

- Before `git push`
- `/update-readme`
- After significant changes

## Usage

```
User: "update the README for this repo"
→ Generate rich README with all formatting options

User: "make it simple"
→ Generate basic README without fancy formatting
```

## Tool Usage

Use `glob`, `read`, `bash (git)`, `write` tools to:
1. Scan repo structure
2. Detect skills/commands/plugins
3. Read package.json, VERSIONING.md
4. Get git info
5. Generate and write README.md
