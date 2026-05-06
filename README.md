# Symphony Sandbox

A throwaway repo used to smoke-test [openai/symphony](https://github.com/openai/symphony).

## Purpose

This repository exsts so we can verify that an autonomous Codex agent, orchestrated by
Symphony, can pick up a Linear issue, clone this repo, make a fix, open a pull request,
and respond to review feedback end-to-end.

## How it works

1. Symphony polls Linear for issues in active states.
2. When it finds an issue, it spawns a Codex `app-server` session in an isolated workspace.
3. The agent reads the issue, edits files in this repo, and pushes a PR.
4. The human reviews and merges.
