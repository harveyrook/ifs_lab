# hello_world

A small Rust command-line program that prints "Hello World". It's a learning project for Claude Code.

## Commands

- Build: `cargo build`
- Run: `cargo run`
- Test: `cargo test`
- Format: `cargo fmt`
- Lint: `cargo clippy`

## Change workflow

Every code change follows this review-and-approve process:

1. Start from an up-to-date `master` and create a new branch for the change with a short, descriptive name (for example `add-greeting`).
2. Make the change on that branch. Don't commit directly to `master`.
3. Before asking for review, run `cargo fmt`, `cargo build`, `cargo test` and `cargo run`, and check that they succeed.
4. Show the diff for review and explain what changed and why.
5. Commit only after the user explicitly approves. Write a clear commit message.
6. After the commit, merge the branch into `master` and delete the branch.
7. If the user rejects the change, delete the branch without merging.

## Git

- Commits use the identity already set in this repository's git config. Don't change it.
- Don't push to a remote or rewrite history (force-push, rebase of shared commits) unless the user asks.
