# pidgn_vscode

Syntax highlighting for pidgn template files in VS Code.

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)

A VS Code extension that provides syntax highlighting, auto-closing pairs, and code folding for `.html.pidgn` template files used by the pidgn web framework.

## Features

- Full HTML syntax highlighting (inherited from VS Code's built-in HTML grammar)
- Pidgn template expression highlighting:
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
ln -s "$(pwd)" ~/.vscode/extensions/pidgn-templates

# Then reload VS Code (Cmd+Shift+P -> "Reload Window")
```

### From VSIX

```bash
# Install vsce if needed
npm install -g @vscode/vsce

# Package the extension
cd pidgn_vscode
vsce package

# Install the .vsix file
code --install-extension pidgn-templates-0.1.0.vsix
```

## Supported File Extensions

- `.html.pidgn` -- HTML templates with pidgn expressions
- `.pidgn` -- standalone pidgn templates

## Ecosystem

| Package | Description |
|---------|-------------|
| [pidgn.zig](https://github.com/seemsindie/pidgn) | Core web framework |
| [pidgn_db](https://github.com/seemsindie/pidgn_db) | Database ORM (SQLite + PostgreSQL) |
| [pidgn_jobs](https://github.com/seemsindie/pidgn_jobs) | Background job processing |
| [pidgn_mailer](https://github.com/seemsindie/pidgn_mailer) | Email sending |
| [pidgn_template](https://github.com/seemsindie/pidgn_template) | Template engine |
| [pidgn_cli](https://github.com/seemsindie/pidgn_cli) | CLI tooling |

## License

MIT License -- Copyright (c) 2026 Ivan Stamenkovic
