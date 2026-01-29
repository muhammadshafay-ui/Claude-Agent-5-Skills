---
name: crypto-market-updates
description: Fetches and summarizes the latest cryptocurrency market updates, price movements, and relevant blockchain events. Use when you need current information about digital assets, cryptocurrency prices, and market trends.
argument-hint: [crypto-symbol] [timeframe]
context: fork
agent: general-purpose
allowed-tools: WebSearch, WebFetch
---

# Crypto Market Updates

Fetches and summarizes the latest cryptocurrency market updates, price movements, and relevant blockchain events.

## What this skill does

Provides information about:
- Daily cryptocurrency market updates and analysis
- Historical crypto market data and trends
- Cryptocurrency price movements and trends
- Market capitalization changes
- Blockchain developments and upgrades
- Regulatory news affecting crypto markets
- Trading volume and liquidity updates
- DeFi and NFT market movements

## Input
Optional parameters:
- Crypto symbol (e.g., BTC, ETH, ADA, SOL)
- Timeframe for news (e.g., "today", "last 24 hours", "this week", "past month", "historical")
- Time period specifications (e.g., "daily updates", "weekly summary", "monthly report", "past performance")

## Output
A structured summary containing:
- 📈 Top performing cryptocurrencies
- 📉 Cryptos showing decline
- 🆕 New developments and announcements
- 💡 Trading insights and market sentiment
- 📊 Key market indicators and data
- 📅 Daily crypto market updates when requested
- 📉 Historical crypto market data when requested

## Instructions

Fetch the latest cryptocurrency market news and updates based on $ARGUMENTS. If no specific cryptocurrency is provided, give a general overview of major market movements. If a specific cryptocurrency is mentioned, focus the summary on that coin/token and related market factors.

When requesting daily updates, provide the most recent market movements and news from the current trading day.

When requesting historical data, specify the time period and relevant market changes during that period, including major events that influenced crypto prices.

Use reliable cryptocurrency news sources, exchanges, and market data platforms. Include price changes in percentages and USD values where available, and note any significant market-moving events or announcements.