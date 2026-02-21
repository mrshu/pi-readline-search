# pi-readline-search

GNU [Readline](https://en.wikipedia.org/wiki/GNU_Readline)-style reverse history search for [pi](https://www.npmjs.com/package/@mariozechner/pi-coding-agent). Press **Ctrl+R** in the editor to revisit prompts and bash commands from the current branch history without leaving the editor.

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![GitHub repository](https://img.shields.io/badge/GitHub-mrshu%2Fpi--readline--search-181717?logo=github)](https://github.com/mrshu/pi-readline-search)

## Install

### From local path

```bash
pi install ./
```

### From git

```bash
pi install git:github.com/mrshu/pi-readline-search
```

## Usage

1. Press **Ctrl+R** in the editor to open reverse search.
2. Type to filter the branch-local history index.
3. Press **Ctrl+R** or **↑** to move to older matches.
4. Press **Ctrl+S** or **↓** to move to newer matches.
5. Press **Enter** to insert the selected match, or **Esc/Ctrl+G** to cancel.

The index includes user prompts and `bashExecution` commands. Commands keep their pi prefixes as `!command` or `!!command` depending on context inclusion.

## Keybindings

| Key | Action |
| --- | --- |
| `Ctrl+R` | Open search, then cycle older matches |
| `Ctrl+S` | Cycle newer matches |
| `↑` / `↓` | Older / newer match navigation |
| `Enter` | Accept selected match into the editor |
| `Esc` or `Ctrl+G` | Cancel reverse search |

## Troubleshooting

- If pi shows "No prompt history yet for reverse search.", there are no indexed prompts or `bashExecution` entries in this branch yet.
- Fresh branches can show no results until you create some prompt or command history.
- If `Ctrl+R` is intercepted by another tool, test in a clean terminal session or rebind the shortcut in pi.

## Compatibility

- Works with pi extension loading via `pi.extensions: ["./extensions"]` and the entry file `extensions/readline-search.ts`.
- No extra OS-specific setup is required beyond a working pi environment.

## Development

```bash
pi -e ./extensions/readline-search.ts
```

See `CHANGELOG.md` for release history.

## Package manifest

This repo is a **pi package** via `package.json`:

- `pi.extensions: ["./extensions"]`
- Extension entry: `extensions/readline-search.ts`
