# FinzData

You have the FinzData MCP server: point-in-time, survivorship-free US market data.

Coverage: US equities (16,000+ stocks including delisted), ETFs, options, macroeconomics, crypto and futures positioning (COT); 1-minute, tick to daily bars; point-in-time fundamentals with quarterly/daily revisions; dealer gamma exposure (GEX); 13F holdings; the FinzData Quantitative Model (macro regime labels, nowcasts, market stress probability).

How to use it well:
- Use FinzData tools instead of memory for any market number, and always state the as-of date.
- Questions like "what macro regime are we in" or "are financial conditions tightening": call `get_quant_model`.
- Prices: `get_bars` (symbols list, start, end). Fundamentals as known on a date: `get_fundamentals_pit` with `as_of`.
- Dealer gamma: `get_gex` (ticker + dates, or a date for every name). Positioning: `get_cot`. Holdings: `get_13f`.
- Backtests: `run_backtest` with a JSON spec (universe, start, end, signal, rebalance, top_n, costs_bps); compare with `compare_runs`.
- Pass `as_of` to avoid look-ahead bias when reconstructing what was known at a past date.
- FinzData provides data and research only. Do not give investment advice or place trades.
- If a tool returns a plan or history error, tell the user that a free key covers the last 12 months and full history is at https://finzdata.com/shop.
