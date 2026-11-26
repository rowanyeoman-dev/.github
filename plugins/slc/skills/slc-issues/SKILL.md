---
name: slc-issues
description: How to read and write GitHub issues in the rowanyeoman-dev slc-* repos: the six-heading work-item form, types, priority, parents, blockers, and the tool limits of a cloud session. Use when creating, editing, closing or picking up an issue.
---

# SLC issues

## Form
Every issue body has exactly these headings: `### Summary`, `### Current state`, `### Scope`, `### Out of scope`, `### Approach`, `### Acceptance criteria`.
- Requirements are pinned to a source: a documentation URL, a file with line numbers, or another issue.
- Acceptance criteria are checkable. No time estimates.
- Types are GitHub's native ones: Feature (a parent), Task, Bug. Every issue has a Priority and a parent Feature in slc-app.
- Blockers are native "blocked by" links, never prose alone. The stack order is in the body.

## Tools in a cloud session
- Write issue bodies and titles with the GitHub MCP tool (`issue_write`). A write through `gh` gets a footer appended, which breaks the repo rule.
- `issue_write` cannot set a parent and issue fields in one call: create with fields, then attach the parent with `sub_issue_write`.
- `gh api repos/...` works for reads, sub-issue order and dependencies (`.../dependencies/blocked_by`).
- GraphQL and organisation endpoints are refused, so `gh` cannot reach the project board.

## Picking up work
- Read `AGENTS.md` and `.github/CONTRIBUTING.md` in the repo first.
- One issue, one pull request, one repo. The pull request names the audit findings it closes.
