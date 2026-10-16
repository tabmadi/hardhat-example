# Agent guide

This guide is for any coding agent that works in this repo. **[README.md](README.md) ranks above this file.** It explains what the example shows and why.

- This repo is an example. It teaches one idea. Keep it small, and do not add what the README lists as deliberately missing.
- Every text follows Simple English: common words, short sentences, no emoji, no em dash, semicolon, or parentheses in prose. The full rules are [ADR-0001 in github-project-template](https://github.com/tabmadi/github-project-template/blob/master/docs/adr/0001-documentation-conventions.md).
- Run every command as `mise run <task>`. Before you finish a change, run `mise run check`.
- Commit messages are a Conventional Commits title only, with no body. Never push unless asked to.

## This example

- The example is incomplete: it has no contract yet. When you add one, update the README so that it no longer says so.
- Yarn runs no dependency build script. `keccak` and `secp256k1` fall back to JavaScript.
- The Yarn version is in `.mise.toml` and in `packageManager` in `package.json`. Change both together.
