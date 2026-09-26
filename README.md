# Memoir — Your personal memory for Cursor

Your life. Remembered.

Let Cursor remember your life. Share your daily thoughts, experiences and updates. Memoir securely saves what matters and lets Cursor use your personal history to give you more relevant answers and insights. Just talk. Memoir remembers.

- **Talk** — Tell Cursor about your day.
- **Remember** — Memoir saves what matters.
- **Ask** — Search your personal history.
- **Understand** — Discover patterns over time.

## Set up

1. Open [app.memoir.florent-tech.com](https://app.memoir.florent-tech.com) and sign in with your email.
2. Click **Create a token** and copy it. It starts with `memoir_` and is shown once.
3. Install the Memoir plugin in Cursor and paste the token into **Memoir token** (`MEMOIR_TOKEN`).
4. Reload MCP. Tell Cursor about your day. In a new chat, ask what happened yesterday.

No plugin? Add this to `~/.cursor/mcp.json` instead:

```json
{
  "mcpServers": {
    "memoir": {
      "url": "https://app.memoir.florent-tech.com/mcp",
      "headers": { "Authorization": "Bearer memoir_…" }
    }
  }
}
```

## What is inside

| Part | What it does |
|---|---|
| `mcp.json` | Connects Cursor to your Vault. Four tools: `memoir_capture`, `memoir_ask`, `memoir_forget`, `memoir_who_am_i`. |
| `rules/memoir.mdc` | Tells the Agent when to save a life-thing and when to Recall before answering. |
| `skills/evening-capture` | "Tell Memoir about today" in one true sentence. |

## Your Vault

- Stored in the EU. We don't train on it. We don't sell it. No ads.
- Forget any Memory from Cursor or from the album.
- Take your Vault with you: the album exports it as markdown.
- Revoke a token from the album at any time.

Privacy: [app.memoir.florent-tech.com/privacy](https://app.memoir.florent-tech.com/privacy)
