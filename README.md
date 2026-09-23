# Dynamoi Agent Plugins

**Music marketing for AI agents.** Official Dynamoi plugins for **Claude** (Claude Code and Claude Cowork) and **Gemini CLI**.

[Dynamoi](https://dynamoi.com) is a music marketing platform for artists, labels, and managers. These plugins connect your agent to Dynamoi's hosted MCP server. They also include skills that teach the agent to:

- create free Spotify Smart Links and artist hubs
- review campaign performance
- check platform connections
- handle music-distribution applications

## Claude

```text
/plugin marketplace add getDynamoi/agent-plugins
/plugin install dynamoi@dynamoi
```

Then run `/mcp`, choose **dynamoi**, and sign in to Dynamoi in your browser.

The Claude plugin connects to `https://dynamoi.com/mcp/directory`, the review-safe tool set:

- Smart Links
- campaign and analytics reads
- platform status
- distribution applications

Paid campaign launches, budget changes, and billing stay in the [Dynamoi dashboard](https://dynamoi.com/dashboard). For the full tool set in Claude Code, including campaign launch and budget changes, add the server directly instead:

```text
claude mcp add --transport http dynamoi https://dynamoi.com/mcp
```

## Gemini CLI

```text
gemini extensions install https://github.com/getDynamoi/agent-plugins --auto-update
```

Then run `/mcp auth dynamoi` and sign in to Dynamoi in your browser. The Gemini extension connects to the full server at `https://dynamoi.com/mcp`.

## Skills

| Skill | What it does |
|---|---|
| `dynamoi-smart-links` | Create, inspect, and update free Smart Links and artist hubs |
| `dynamoi-campaign-review` | Report campaign status, analytics, and platform connection health |
| `dynamoi-distribution` | Check distribution eligibility and submit applications, only with your explicit confirmation |

## How it works

- **Server:** `https://dynamoi.com/mcp`, supporting MCP protocol 2026-07-28 and 2025-era clients.
- **Sign-in:** OAuth 2.1 with PKCE. Client ID Metadata Documents and Dynamic Client Registration are both supported.
- **Payments:** agents never receive payment credentials.
- **Documentation:** https://dynamoi.com/docs/mcp-server
- **Package and source:** [`@dynamoi/mcp`](https://github.com/getDynamoi/mcp)

## Support

- Help center: https://dynamoi.com/support
- Email: support@dynamoi.com (we reply within 24 hours)
- Privacy policy: https://dynamoi.com/privacy-policy
- Terms of service: https://dynamoi.com/terms-of-service

## License

MIT
