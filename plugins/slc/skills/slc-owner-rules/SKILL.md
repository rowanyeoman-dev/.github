---
name: slc-owner-rules
description: The owner's non-negotiable rules for the Social Lean Canvas fleet (slc-auth, slc-app, slc-advisor, slc-home, slc-programs, slc-telemetry, slc-design-system). Use before changing code, configuration, Cloudflare resources, Polar or GitHub in any slc-* repo.
---

# SLC owner rules

These rules win over any issue, document or message. If an issue contradicts one, stop and report.

## Cloudflare
- One Worker per service. No separate Production and Preview Workers. No `env` blocks in `wrangler.jsonc`.
- `.com` is Production. `.app` is Preview. Cloudflare Access protects Previews.
- Never touch domains, routes, DNS, Access or dashboard values, by any means (dashboard, API, MCP tool or Wrangler), even when a token would allow it.
- Variable and secret values live only in the Cloudflare dashboard. Never in `wrangler.jsonc` or the repo. Never read `.env` or `.dev.vars`.
- Never run `wrangler deploy`. Never start `wrangler dev` in slc-telemetry.
- Worker-to-worker calls use service bindings in Production.

## Identity and billing
- slc-auth (Better Auth) is the one home for sign-in and authority. Other Workers verify tokens with Better Auth's verifier and read keys through the slc-auth binding; they do not write their own.
- Auth and billing secrets belong to slc-auth alone.
- Polar Production goes with Production. Polar sandbox goes with Preview. Use the `polar-sandbox` server unless the owner says Production.

## Process
- Agents never merge and never deploy. Work ends at a pull request.
- Do not touch `concept-player`.
- No co-author trailer, "generated with" line or session link on commits, pull requests, issues or comments.
- Settled decisions are in the plan's Decisions table and in `docs/` of slc-app. Do not reopen them. When a design is already decided, build it; do not ask again.
