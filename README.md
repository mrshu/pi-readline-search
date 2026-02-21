# pi-readline-search

GNU [Readline](https://en.wikipedia.org/wiki/GNU_Readline)-style reverse history search for [pi](https://www.npmjs.com/package/@mariozechner/pi-coding-agent).

Press **Ctrl+R** in the editor to search previous prompts and user bash commands (`!` / `!!`).

## Features

- **Ctrl+R** opens reverse search
- Type to filter history
- **Ctrl+R** or **↑** for older matches
- **Ctrl+S** or **↓** for newer matches
- **Enter** to insert selected match into the editor
- **Esc** or **Ctrl+G** to cancel

## Install

### From local path

```bash
pi install ./
```

### From git

```bash
pi install git:github.com/mrshu/pi-readline-search
```

## Dev / quick test

```bash
pi -e ./extensions/readline-search.ts
```

## Package manifest

This repo is a **pi package** via `package.json`:

- `pi.extensions: ["./extensions"]`
- extension entry: `extensions/readline-search.ts`

## Publish to npm

```bash
npm login
npm whoami
npm publish --dry-run
npm publish --access public
```
