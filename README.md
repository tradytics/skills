# Tradytics for Claude and coding agents

Options flow, dark pool prints, dealer exposure, volatility, prices, fundamentals, SEC filings, insider and Congress trades, and Kalshi and Polymarket odds, from Tradytics. One plugin for Claude (chat, Cowork and Claude Code) and one skill for any agent that reads `SKILL.md`.

## Install

In Claude, add **Tradytics** from the plugin directory. In Claude Code:

```text
/plugin marketplace add tradytics/skills
/plugin install tradytics@tradytics
```

For Codex, Cursor and other agents:

```bash
npx skills add tradytics/skills
```

## Use it

Ask in plain words: what the options flow says about NVDA today, where SPY's gamma walls are, the largest dark pool prints in TSLA this week, who reports earnings this week, or why a stock is moving. Claude answers from the Tradytics connector's tools. In code, the `tradytics` skill teaches the agent all 79 endpoints of the [Tradytics API](https://tradytics.com/docs), their parameters and fields.

| Piece | What it does |
| --- | --- |
| [Connector](.mcp.json) | The Tradytics MCP server, https://tradytics.com/mcp. You sign in with your Tradytics account |
| [Skill](skills/tradytics/SKILL.md) | When and how to call each endpoint, with one reference file per data area |

Market data answers on Tradytics Pro.

## Data

The connector sends the tickers, dates and filters of each request to tradytics.com and returns market data; you sign in through Tradytics' OAuth page, and the connection shows on your [API keys](https://tradytics.com/developer/keys) page, where you can end it. Without the connector, the skill sends requests to `https://tradytics.com/api/public/v1` with the API key you give it. Nothing is sent anywhere else, and the plugin stores nothing. [Privacy policy](https://tradytics.com/privacy-policy).

Generated from the Tradytics docs, so it changes with the API.
