# MetricRaven for Cursor

[MetricRaven](https://metricraven.com) is privacy-friendly web analytics with revenue attribution. This Cursor plugin connects Cursor to your MetricRaven account through MetricRaven's remote MCP server, so you can ask about your websites in plain language:

- "Chart my visitors and revenue for the last 30 days."
- "Which channels brought the most revenue this month?"
- "Show my top pages by visitors this week."

## What's inside

- `plugins/metricraven/mcp.json`: the MetricRaven MCP server, `https://metricraven.com/api/mcp` (remote, HTTPS).
- `plugins/metricraven/skills/get-started`: tells the agent which MetricRaven tools to use for charts, numbers, goals and funnels.

## Sign-in and permissions

The first time a MetricRaven tool runs, Cursor opens MetricRaven's sign-in (OAuth 2.1 with PKCE). You choose the access (read reports by default; visitor details and write access are optional) and which websites the connection can read. Disconnect any time on the API & MCP page in MetricRaven.

Without the plugin, add the server yourself in `~/.cursor/mcp.json`:

```json
{
  "mcpServers": {
    "metricraven": { "url": "https://metricraven.com/api/mcp" }
  }
}
```

## Links

- Docs: https://metricraven.com/docs/mcp
- Privacy policy: https://metricraven.com/legal/privacy
- Terms: https://metricraven.com/legal/terms
- Support: support@metricraven.com

Published by Dual Ninja LLC.
