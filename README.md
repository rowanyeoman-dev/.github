# rowanyeoman-dev

This repository holds the agent plugin marketplace for the Social Lean Canvas fleet. Both plugins are the vendors' official tools, unchanged.

Add it at claude.ai, Customize, Plugins, Add, Add marketplace: `rowanyeoman-dev/.github`.

| Plugin | Source | Contents |
|---|---|---|
| `polar` | [`polarsource/agent-toolkit`](https://github.com/polarsource/agent-toolkit) | MCP servers `polar` (`https://mcp.polar.sh/mcp/polar-mcp`) and `polar-sandbox` (`https://mcp.polar.sh/mcp/polar-sandbox`); skills `setup-polar`, `polar-integration`, `polar-testing`, `polar-migration`. See https://polar.sh/docs/agents/skills-and-plugins |
| `better-auth` | [`better-auth/skills`](https://github.com/better-auth/skills) | MCP server `better-auth` (`https://mcp.better-auth.com/mcp`); skills `best-practices`, `create-auth`, `emailAndPassword`, `organization`, `twoFactor`, `security`. See https://better-auth.com/docs/ai-resources/mcp and https://better-auth.com/docs/ai-resources/skills |

Better Auth's own marketplace lists only two of its six skills and no MCP server, so the `better-auth` entry here lists all six skills from the same repository and adds the documentation server Better Auth publishes.
