---
name: get-started
description: Use when someone first connects MetricRaven or asks what it can do with their website analytics, traffic, revenue, goals or funnels.
---

# Get started with MetricRaven

MetricRaven is web analytics with revenue attribution. Every report is about websites the person approved when they connected.

1. Call `list_websites` to see which websites this connection can read. If there is only one, use it without asking.
2. For "show", "chart" or "visualize" requests about traffic or revenue over time, call `show_traffic_chart`. For ranked comparisons (channels, referrers, campaigns, pages, countries, devices), call `show_breakdown_chart`.
3. For numbers without a chart, use `get_traffic`, `get_breakdown`, `get_revenue`, `get_conversions` (goals and funnels) or `get_realtime`.
4. Periods default to the last 30 days. Use `period` (`today`, `7d`, `30d`, `90d`, `1y`, `mtd`, `all`…) or `from` and `to` dates, and pass `timezone` when the person mentions one.
5. Revenue is credited to the visit that first brought each customer. Say so when comparing channels by revenue.

Tools that change things (chart notes, alerts, goal labels, team members) need the write permission. Explain the change and ask before calling them. If a tool reports a missing permission, tell the person to reconnect MetricRaven and allow it.

Suggested first questions:

- "Chart my visitors and revenue for the last 30 days."
- "Which channels brought the most revenue this month?"
- "Show my signup funnel and where visitors drop off."
