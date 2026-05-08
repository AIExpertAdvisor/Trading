# New Trading System

Use this skill to scaffold a new trading system for TheAlgoTrdr.

## Instructions

Ask the user the following questions one at a time before writing any code:

1. **System name** — What is the name of this indicator/strategy/EA?
2. **Platform** — Is this for TradingView (Pine Script) or MetaTrader 5 (MQL5)?
3. **Product type** — Is it an Indicator, Strategy (TradingView only), or Expert Advisor (MT5 only)?
4. **Market / Asset class** — Which market is it designed for? (Forex, Crypto, Stocks, Indices, Commodities, or multi-market?)
5. **Timeframe** — What is the primary timeframe? (e.g. M1, M5, M15, H1, H4, D1)
6. **Strategy type** — What type of system is this? (Trend Following, Mean Reversion, Scalping, or Custom/Hybrid?)
7. **Core logic** — Briefly describe the entry and exit logic. What conditions trigger a buy/sell signal?
8. **Risk rules** — Are there any specific risk management rules? (e.g. stop loss, take profit, max daily loss, lot sizing)
9. **Client delivery** — Is this for internal use or client delivery?

## Once all questions are answered:

- Scaffold the appropriate file in the correct folder:
  - TradingView Indicator → `tradingview/indicators/`
  - TradingView Strategy → `tradingview/strategies/`
  - MT5 Indicator → `metatrader5/indicators/`
  - MT5 Expert Advisor → `metatrader5/experts/`

- Use **Pine Script v6** for all TradingView work
- Use **MQL5 best practices** for all MT5 work (OnInit, OnTick, OnDeinit structure)
- Code must be **performance optimised** and **client-ready**
- Add **clear comments** on all trading logic — every signal, entry, exit, and risk rule
- Never hardcode API keys, broker credentials, or account-specific data

## Output

Produce the full scaffolded file and confirm:
- File name and save location
- A brief summary of what was built
- Any assumptions made during development
- Suggested next steps (e.g. backtest, add alerts, parameter optimisation)
