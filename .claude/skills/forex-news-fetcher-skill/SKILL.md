---
name: forex-news-fetcher
description: Fetches and summarizes the latest forex market updates, currency movements, and relevant economic events. Use when you need current information about foreign exchange markets, currency pairs, and economic events affecting forex trading.
argument-hint: [currency-pair] [date-range]
context: fork
agent: general-purpose
allowed-tools: WebSearch, WebFetch
---

# Forex News Fetcher

Fetches and summarizes the latest forex market updates, currency movements, and relevant economic events.

## What this skill does

Provides information about:
- Daily forex market updates and analysis
- Historical forex data and trends
- Current currency pair movements and trends
- Economic events affecting forex markets
- Central bank announcements and decisions
- Market volatility and trading opportunities

## Input
Optional parameters:
- Currency pair (e.g., EUR/USD, GBP/JPY, USD/CAD)
- Date range for news (e.g., "today", "last week", "this month", "past month", "historical")
- Timeframe specifications (e.g., "daily updates", "weekly summary", "monthly report")

## Output
A structured summary containing:
- 🔼 Currency pairs gaining value
- 🔽 Currency pairs declining in value
- 📢 Major economic events and announcements
- 💡 Trading insights and market sentiment
- 📊 Key market indicators and data
- 📅 Daily forex updates when requested
- 📉 Historical forex data when requested

## Instructions

Fetch the latest forex market news and updates based on $ARGUMENTS. If no specific currency pair is provided, give a general overview of major currency movements. If a specific currency pair is mentioned, focus the summary on that pair and related market factors.

When requesting daily updates, provide the most recent market movements and news from the current trading day.

When requesting historical data, specify the time period and relevant market changes during that period, including major economic events that influenced currency movements.

Use reliable financial news sources and provide timestamps for important events. Include both technical analysis and fundamental factors affecting the markets.