# Memoir — personal memory for Cursor and Claude Code

Your life. Remembered.

Ask Memoir to save ordinary life details, then Recall them in a future conversation. The same Memoir account reaches the same Vault in compatible Clients.

## Connect

The endpoint is `https://app.memoir.florent-tech.com/mcp`; connect with OAuth using your Memoir account.

Cursor discovers `.cursor-plugin/plugin.json`, `mcp.json`, rules and skills in this folder. Claude Code discovers `.claude-plugin/plugin.json`, `.mcp.json` and the same skills. Root marketplace manifests in the Memoir repository locate this folder. These are direct-distribution packages, not proof of official marketplace approval.

For a local Claude Code trial from the extracted package directory, run `claude --plugin-dir .`, then authenticate through `/mcp`. The evening-capture skill helps record a day after you explicitly start the session. Avoid installing the same remote MCP twice.

The standalone public distribution is [memoir-cursor-plugin](https://github.com/FlorentLP/memoir-cursor-plugin). In Claude Code, add it with `/plugin marketplace add FlorentLP/memoir-cursor-plugin`, then `/plugin install memoir@memoir` after that repository has received this release. For a local Cursor trial, copy the complete package to `~/.cursor/plugins/local/memoir` (preserving any existing installation) and reload Cursor.

For a direct Cursor connection, add this server to its MCP configuration and sign in:

```json
{"mcpServers":{"memoir":{"url":"https://app.memoir.florent-tech.com/mcp"}}}
```

For a direct Claude Code connection, use `claude mcp add --transport http memoir https://app.memoir.florent-tech.com/mcp`, then `/mcp` to authenticate. [Cursor documentation](https://cursor.com/docs/mcp) · [Claude documentation](https://code.claude.com/docs/en/mcp).

## What Memoir does

Four tools: `memoir_capture`, `memoir_ask`, `memoir_forget`, `memoir_who_am_i`. Capture can Amend an existing Memory; Recall returns current active Memories. The shared per-Vault limit is 60 commands per hour.

Forget removes a Memory from future Recall; it is not immediate erasure of stored history. Export in the album downloads current active Memories as Markdown. Supabase stores the Vault, Cloudflare serves requests, and the AI Client's own data policies also apply. Keep secrets, payment details, government identifiers and sensitive medical records out.

[Privacy](https://app.memoir.florent-tech.com/privacy) · [Terms](https://app.memoir.florent-tech.com/terms) · [Support](https://app.memoir.florent-tech.com/support)
