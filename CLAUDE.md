# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## State of the repo

This is a minimal starter/sandbox project (remote: `opuopu/Claude_MCP` on GitHub, branch `main`). There is no build system, `package.json`, linter, or test suite yet, so there are no build/lint/test commands to run.

- `index.js` — defines `const p = "hello world"` and logs it. Run with `node index.js`.
- `index.html` — a static page; open it directly in a browser. It loads `index.js` as a classic script and renders the global `p` into `<p id="output">`, so `p` must stay a top-level declaration in `index.js`.
- `.claude/skills/hello/SKILL.md` — a project-level Claude Code skill invoked with `/hello`. It is marked `disable-model-invocation: true`, so it only runs when the user types the slash command.

When adding tooling (package.json, tests, a bundler, an MCP server), update this file with the real commands and architecture.
