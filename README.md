# zzz_vscode

Syntax highlighting for zzz template files in VS Code.

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)

A VS Code extension that provides syntax highlighting, auto-closing pairs, and code folding for `.html.zzz` template files used by the zzz web framework.

## Features

- Full HTML syntax highlighting (inherited from VS Code's built-in HTML grammar)
- Zzz template expression highlighting:
  - Variables: `{{name}}`, `{{user.name}}`
  - Raw (unescaped) variables: `{{{content}}}`
  - Conditionals: `{{#if cond}}` / `{{else}}` / `{{/if}}`
  - Loops: `{{#each items}}` / `{{/each}}`
  - Comments: `{{! this is a comment }}`
- Auto-closing pairs for `{{ }}` and `{{{ }}}`
- Code folding for `{{#if}}` / `{{#each}}` blocks
- Embedded JavaScript and CSS highlighting within HTML

## Installation

### Local development (symlink)

```bash
# macOS / Linux
ln -s "$(pwd)" ~/.vscode/extensions/zzz-templates

# Then reload VS Code (Cmd+Shift+P -> "Reload Window")
```

### From VSIX

```bash
# Install vsce if needed
npm install -g @vscode/vsce

# Package the extension
cd zzz_vscode
vsce package

# Install the .vsix file
code --install-extension zzz-templates-0.1.0.vsix
```

## Supported File Extensions

- `.html.zzz` -- HTML templates with zzz expressions
- `.zzz` -- standalone zzz templates

## Ecosystem

| Package | Description |
|---------|-------------|
| [zzz.zig](https://github.com/seemsindie/zzz.zig) | Core web framework |
| [zzz_db](https://github.com/seemsindie/zzz_db) | Database ORM (SQLite + PostgreSQL) |
| [zzz_jobs](https://github.com/seemsindie/zzz_jobs) | Background job processing |
| [zzz_mailer](https://github.com/seemsindie/zzz_mailer) | Email sending |
| [zzz_template](https://github.com/seemsindie/zzz_template) | Template engine |
| [zzz_cli](https://github.com/seemsindie/zzz_cli) | CLI tooling |

## License

MIT License -- Copyright (c) 2026 Ivan Stamenkovic
