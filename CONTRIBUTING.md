# Contributing

Short version: work is tracked as GitHub issues, and an issue moves through three stages.
An issue is open or closed; its type, its parent and its linked pull request say the rest.
No label carries a status.

## The three stages

### Triage

Owned by the maintainer. An issue is ready for coding only once it is planned to a spec: the type
is set, requirements are pinned to a source (a doc URL, a spec section, an existing file),
acceptance criteria are checkable, the exact verification commands are written down, and what is
deliberately out of scope is named.

### Coding

The agent's stage, and it ends at the pull request.

- Work in a git worktree, never in the primary checkout.
- The pull request must target `main`, or `Closes #N` is silently ignored and merging changes
  nothing.
- Tests pass locally before the PR is opened, not after.
- Read your own diff before handing it over. Self-review is not a substitute for the review gate,
  and the review gate is not a substitute for reading your own work.

### Review

Owned by the maintainer: checks green, machine review, approval, merge. Nothing merges on an
approval given for something else.

## Issue types

`Bug`, `Feature` and `Task` are GitHub's native issue types on this organisation — use them
rather than labels. A `Bug` or a `Feature` is an origin. A `Task` is a child of one of those, or,
as a last resort, an ad-hoc chore that serves neither and says so.

## Commands

Every repository with a `package.json` has `npm run check`, which runs its typecheck, lint and tests. Each repository's `AGENTS.md` lists its other commands and which of them must pass before a pull request.
