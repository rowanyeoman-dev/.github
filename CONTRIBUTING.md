# Contributing

Short version: work is tracked as GitHub issues, and an issue moves through three stages on the
[Social Lean Canvas project board](https://github.com/orgs/rowanyeoman-dev/projects/1).
The board's `Status` field is the only place a status lives — never a label.

## The three stages

### Triage — `Unplanned → Todo`

Owned by the maintainer. An issue leaves `Unplanned` only once it is planned to a spec: the type
is set, requirements are pinned to a source (a doc URL, a spec section, an existing file),
acceptance criteria are checkable, the exact verification commands are written down, and what is
deliberately out of scope is named.

### Coding — `Todo → In progress → In review`

The agent's stage, and it ends at the pull request.

- Work in a git worktree, never in the primary checkout.
- The pull request must target `main`, or `Closes #N` is silently ignored and merging changes
  nothing.
- Tests pass locally before the PR is opened, not after.
- Read your own diff before handing it over. Self-review is not a substitute for the review gate,
  and the review gate is not a substitute for reading your own work.

### Review — `In review → Done`

Owned by the maintainer: checks green, machine review, approval, merge. Nothing merges on an
approval given for something else.

## Issue types

`Bug`, `Feature` and `Task` are GitHub's native issue types on this organisation — use them
rather than labels. A `Bug` or a `Feature` is an origin. A `Task` is a child of one of those, or,
as a last resort, an ad-hoc chore that serves neither and says so.

## Commands

Each repository's `AGENTS.md` lists its commands and which of them must pass before a pull request.
