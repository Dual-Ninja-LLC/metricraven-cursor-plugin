# MetricRaven for Cursor

The Cursor plugin for [MetricRaven](https://metricraven.com), privacy-friendly web analytics with revenue
attribution: see which traffic actually pays. It connects Cursor to your MetricRaven account through
MetricRaven's remote MCP server, so you can ask about your websites in plain language without leaving
the editor, and get answers and charts back:

- "Chart my visitors and revenue for the last 30 days."
- "Which channels brought the most revenue this month?"
- "Which referrers brought paying customers in the last 90 days?"
- "Show my top pages by visitors this week."

You need a MetricRaven account with a website: sign up at https://metricraven.com.

## Install

Add the MCP server in `~/.cursor/mcp.json` (or `.cursor/mcp.json` for one project):

```json
{
  "mcpServers": {
    "metricraven": { "url": "https://metricraven.com/api/mcp" }
  }
}
```

Or in one click from the [MCP docs](https://metricraven.com/docs/mcp#cursor) ("Add MetricRaven to Cursor").
In Cursor's web agents (cursor.com/agents): **+ → MCP → Add MCP → Custom MCP**, enter the server URL,
then **Connect**.

## What's inside

- `.cursor-plugin/marketplace.json`: the marketplace manifest listing the plugin.
- `plugins/metricraven/.cursor-plugin/plugin.json`: the plugin manifest.
- `plugins/metricraven/mcp.json`: the MetricRaven MCP server, `https://metricraven.com/api/mcp` (remote, Streamable HTTP over HTTPS).
- `plugins/metricraven/skills/get-started`: tells the agent which MetricRaven tools to use for charts, numbers, goals and funnels.
- `scripts/validate-template.mjs`: checks the manifests (`node scripts/validate-template.mjs`).

The plugin contains no hooks or local servers. It runs nothing on your computer.

## What you can ask about

Traffic, revenue and MRR by channel, referrer, campaign, page and country; goals, funnels and paths to
payment; realtime visitors; AI crawlers and AI visibility; search keywords, ad spend and page speed. The
full list of tools and their inputs is in the [tool reference](https://metricraven.com/docs/mcp-tools).

## Sign-in and permissions

The first time a MetricRaven tool runs, Cursor opens MetricRaven's sign-in (OAuth 2.1 with PKCE). You choose the access (read reports by default; visitor details and write access are optional) and which websites the connection can read. Write access adds websites, chart notes, alerts, funnels, segments and goals; the server never deletes anything or changes your team or billing. Disconnect any time on the API & MCP page in MetricRaven.

## Privacy

The agent's tool requests (website, period, filters) go to MetricRaven at `https://metricraven.com/api/mcp`, and MetricRaven returns analytics for the websites you approved. Without visitor details access, reports never include names, emails or visitor IDs. The plugin sends data nowhere else and stores nothing itself. See the [privacy policy](https://metricraven.com/legal/privacy).

## Links

- Docs: https://metricraven.com/docs/mcp
- Tool reference: https://metricraven.com/docs/mcp-tools
- Dashboard and sign-up: https://metricraven.com
- Privacy policy: https://metricraven.com/legal/privacy
- Terms: https://metricraven.com/legal/terms
- Support: support@metricraven.com

## License

MIT. See [LICENSE](LICENSE). Published by Dual Ninja LLC.
