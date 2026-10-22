# Dynamoi Agent Plugins

**Music promotion and distribution, built for AI agents.**

Official [Dynamoi](https://dynamoi.com) plugins for **Claude Code**, **Claude
Cowork** and **Gemini CLI**. Each one connects your agent to Dynamoi's hosted
MCP server and adds skills that teach it how to promote music well: build
free Smart Links, review Spotify and YouTube campaign results, check platform
connections, and, if the artist wants it, apply for distribution. Dynamoi
works with any distributor.

## Install

<details open>
<summary><b>Claude Code and Claude Cowork</b></summary>

```text
/plugin marketplace add getDynamoi/agent-plugins
/plugin install dynamoi@dynamoi
```

Run `/mcp`, choose **dynamoi**, and sign in to Dynamoi in your browser.

The plugin connects to `https://dynamoi.com/mcp/directory`, the review-safe
tool set: Smart Links, campaign and analytics reads, platform status and
distribution applications. Campaign launches, budget changes and billing need
the full server, which you add in Claude Code with:

```text
claude mcp add --transport http dynamoi https://dynamoi.com/mcp
```

</details>

<details open>
<summary><b>Gemini CLI</b></summary>

```text
gemini extensions install https://github.com/getDynamoi/agent-plugins --auto-update
```

Run `/mcp auth dynamoi` and sign in. The extension connects to the full server
at `https://dynamoi.com/mcp`.

</details>

Using Codex, Cursor, VS Code, ChatGPT or another client? Connect the server
directly with the [MCP server instructions](https://github.com/getDynamoi/dynamoi#connect).

## Try asking

> Make a Smart Link for this Spotify single and give me the link.

> How are my campaigns doing this month? Anything that needs attention?

> Is my Meta and YouTube connection set up correctly?

> Am I eligible for Dynamoi distribution yet? What is still missing?

## Skills

| Skill | Use it to |
| --- | --- |
| `dynamoi-smart-links` | Create, inspect and update free Smart Links and artist hubs |
| `dynamoi-campaign-review` | Report campaign status, analytics and platform connection health |
| `dynamoi-distribution` | Check optional distribution eligibility and apply, only after you confirm |

## Safety

- Sign-in is OAuth 2.1 in your browser. There are no API keys to paste.
- Agents never receive payment details, and paid actions need the artist's
  explicit consent.
- The skills tell the agent to report only what Dynamoi returns, never
  invented results or eligibility numbers.

## Support

- Docs: [dynamoi.com/docs/mcp-server](https://dynamoi.com/docs/mcp-server)
- Help: [dynamoi.com/support](https://dynamoi.com/support) or
  support@dynamoi.com (we reply within 24 hours)
- [Privacy policy](https://dynamoi.com/privacy-policy) and
  [terms of service](https://dynamoi.com/terms-of-service)

MIT licensed. See [LICENSE](./LICENSE).

---

**Part of Dynamoi** · [MCP server](https://github.com/getDynamoi/dynamoi) · [CLI](https://github.com/getDynamoi/dynamoi/tree/main/cli) · [Agent plugins](https://github.com/getDynamoi/agent-plugins) · [Homebrew tap](https://github.com/getDynamoi/homebrew-tap) · [Chrome extension](https://github.com/getDynamoi/browser-extension) · [dynamoi.com](https://dynamoi.com) · [Docs](https://dynamoi.com/docs) · [Support](https://dynamoi.com/support)
