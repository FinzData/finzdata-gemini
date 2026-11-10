<p align="center"><a href="https://finzdata.com"><img src="https://finzdata.com/assets/brand/finzdata-logo-full.png" alt="FinzData" width="360"></a></p>

# FinzData extension for Gemini CLI

Point-in-time, survivorship-free US market data in Gemini CLI: 16,000+ US stocks including delisted, ETFs, options, macroeconomics, crypto, futures positioning (COT), 1-minute, 5-minute, 15-minute, 30-minute, hourly and daily bars, point-in-time fundamentals, dealer gamma (GEX), 13F, the FinzData Quantitative Model, and backtests.

## Coverage

Market data your backtests can trust. The whole market, remembered: every one of the 16,000+ US stocks that has traded on the NYSE and Nasdaq in the last 26+ years, delisted included, point in time. Around them: 139 futures markets with every contract since 2007, the VIX and Cboe volatility indexes with the VIX futures curve, options-market gamma for single stocks, ETFs and the major indexes, 231 ETFs, and crypto since 2015. Macro exactly as it was known: 18,000+ series including CPI, payrolls, wages, GDP and the Treasury yield curve, every vintage kept. Plus COT positioning since 1986. Bars at every resolution you backtest on: 1-minute, 5-minute, 15-minute, 30-minute, hourly and daily, with tick-level trades on the Institutional plan. In pandas with one line: `pip install finzdata`.

## Coverage

FinzData is point-in-time market data for AI, quants, data scientists and financial analysts:

- 16,000+ US stocks traded since 2000, delisted included, and 5,100+ ETFs: tick trades and 1-minute to daily bars
- Point-in-time options gamma (GEX) for 11,200+ stocks, ETFs and indexes since 2010, plus options chains
- 139 futures markets with every contract since 2007; CFTC COT since 1986
- 512 crypto pairs, 79 FX pairs and 123 indexes
- SEC fundamentals as filed, 13F holdings, insider trades and short interest
- 22,700+ macro series with every vintage, including electricity use, prices and power demand
- Global Macro Pulse: ship transits through 28 chokepoints, port calls for 2,000+ ports, flights by airport and airline, and toll and congestion traffic

Free API key: https://finzdata.com · MCP server for Claude and other AI assistants: https://api.finzdata.com/mcp · Docs: https://finzdata.com/docs

## Install

```bash
gemini extensions install https://github.com/FinzData/finzdata-gemini
```

Start Gemini CLI and run `/mcp auth finzdata`. Your browser opens the FinzData sign-in page: paste your FinzData API key (free at https://finzdata.com/signin) and approve. Gemini stores the token for you.

## Try it

- "What macro regime is the US economy in right now, according to FinzData?"
- "Get SPY daily bars for the last month."
- "What were AAPL's fundamentals as known on 2026-06-30?"
- "What is SPY's dealer gamma exposure this week?"
- "Backtest monthly 3-month momentum on SPY, QQQ, IWM, TLT and GLD since November 2025, holding the top 2."

## What's inside

- `gemini-extension.json` connects Gemini CLI to the FinzData MCP server at `https://api.finzdata.com/mcp` (streamable HTTP, OAuth with dynamic client registration).
- `GEMINI.md` tells Gemini how to use the tools (as-of dates, no look-ahead, no investment advice).

Free keys cover the last 12 months. Full history: https://finzdata.com/shop. Docs: https://finzdata.com/docs. Privacy: https://finzdata.com/privacy. Support: info@finzdata.com.

FinzData: Clean data. Real insights. Real alpha.
