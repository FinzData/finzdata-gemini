# FinzData

You have the FinzData MCP server: point-in-time, survivorship-free US market data.

Coverage: Market data your backtests can trust. The whole market, remembered: every one of the 16,000+ US stocks that has traded on the NYSE and Nasdaq in the last 26+ years, delisted included, point in time. Around them: 139 futures markets with every contract since 2007, the VIX and Cboe volatility indexes with the VIX futures curve, options-market gamma for single stocks, ETFs and the major indexes, 231 ETFs, and crypto since 2015. Macro exactly as it was known: 18,000+ series including CPI, payrolls, wages, GDP and the Treasury yield curve, every vintage kept. Plus COT positioning since 1986. Bars at every resolution you backtest on: 1-minute, 5-minute, 15-minute, 30-minute, hourly and daily, with tick-level trades on the Institutional plan. In pandas with one line: `pip install finzdata`. Also: point-in-time fundamentals, 13F holdings and the FinzData Quantitative Model (macro regime labels, nowcasts, market stress probability).

How to use it well:
- Use FinzData tools instead of memory for any market number, and always state the as-of date.
- Questions like "what macro regime are we in" or "are financial conditions tightening": call `get_quant_model`.
- Prices: `get_bars` (symbols list, start, end). Fundamentals as known on a date: `get_fundamentals_pit` with `as_of`.
- Dealer gamma: `get_gex` (ticker + dates, or a date for every name). Positioning: `get_cot`. Holdings: `get_13f`.
- Backtests: `run_backtest` with a JSON spec (universe, start, end, signal, rebalance, top_n, costs_bps); compare with `compare_runs`.
- Pass `as_of` to avoid look-ahead bias when reconstructing what was known at a past date.
- FinzData provides data and research only. Do not give investment advice or place trades.
- If a tool returns a plan or history error, tell the user that a free key covers the last 12 months and full history is at https://finzdata.com/shop.
