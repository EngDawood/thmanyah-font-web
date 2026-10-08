---
description: Add the Thmanyah Arabic font to this project and save your choices in .claude/thmanyah-font.local.md
argument-hint: "[cdn|npm] [sans|serif-display|serif-text|all]"
allowed-tools: ["Read", "Write", "Edit", "Glob", "Grep", "Bash(npm install:*)", "Bash(pnpm add:*)", "Bash(yarn add:*)", "Bash(bun add:*)", "AskUserQuestion"]
---

# Thmanyah font setup

Add the Thmanyah (ثمانية) font to the current project. Follow the `thmanyah-font-web` skill for the CSS, class names and the license note. Arguments given: `$ARGUMENTS`

## Settings file

Per-project choices live in `.claude/thmanyah-font.local.md`:

```markdown
---
source: cdn            # cdn | npm
families: [sans]       # any of: sans, serif-display, serif-text (or [all])
body_family: sans      # family applied to <body>
heading_family: serif-display   # family applied to h1-h6, or "" to skip
rtl: true              # set lang="ar" dir="rtl" on <html>
---
```

## Steps

1. Read `.claude/thmanyah-font.local.md` if it exists and use its values as defaults. Explicit values in `$ARGUMENTS` override them.
2. For anything still unknown, ask once with AskUserQuestion (source, families, whether the page is RTL). Recommend `cdn` and `sans` when the user has no preference.
3. Detect the project type: look for `package.json` (framework and entry file), plain `index.html`, or a global CSS file.
4. Apply the font:
   - **cdn**: add `<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/@dawod/thmanyah-font-web/<file>.css" />` to the HTML head (or the framework's root layout). `<file>` is `index` for several families, otherwise `sans`, `serif-display` or `serif-text`.
   - **npm**: install `@dawod/thmanyah-font-web` with the project's package manager, then add the matching import (`import "@dawod/thmanyah-font-web/sans.css"` in JS/TS, or `@import` in CSS).
5. Add the `font-family` rules for `body_family` and `heading_family` to the project's main stylesheet. Always quote family names and give a fallback (`"Thmanyah Sans", sans-serif`).
6. If `rtl` is true, make sure `<html>` has `lang="ar" dir="rtl"`. Do not overwrite an existing `lang` or `dir` without asking.
7. Write or update `.claude/thmanyah-font.local.md` with the final values. Make sure `.claude/*.local.md` is in `.gitignore`; add it if missing.
8. Finish with a short summary of the files changed and how to verify: devtools Network tab, filter `woff2`, expect 200s from `cdn.jsdelivr.net`.

## Rules

- Never download or copy font binaries into the project here. This command only links to the CDN or installs the CSS package. If the user wants local files, point them to the skill's download section and repeat its license warning first.
- Keep edits minimal and match the project's existing style.
- If the project is not a web project, say so and stop.
