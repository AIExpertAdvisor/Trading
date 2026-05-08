# CLAUDE.md - TheAlgoTrdr

## About TheAlgoTrdr

TheAlgoTrdr is an AI Trading Agency that designs, builds, and delivers AI-powered trading systems. Products include:

- **TradingView Indicators** - Pine Script-based visual analysis tools
- **TradingView Strategies** - Pine Script backtestable strategy systems
- **MetaTrader 5 Indicators** - MQL5 custom market analysis tools
- **MetaTrader 5 Expert Advisors (EAs)** - Fully automated MQL5 trading bots

---

## Tech Stack

| Layer | Tools |
|---|---|
| TradingView development | Pine Script (v5+) |
| MetaTrader 5 development | MQL5 |
| AI/ML & data | Python |
| Web / client portals | JavaScript / TypeScript |

---

## Markets Traded

- Forex (currency pairs)
- Crypto (Bitcoin, altcoins, perpetuals)
- Stocks / Equities (US and global)
- Indices & Commodities (SPX, NAS, Gold, Oil, etc.)

---

## Strategy Types

- **Trend Following** - momentum-based directional systems
- **Mean Reversion** - price-to-average regression systems
- **Scalping / High Frequency** - short timeframe, rapid execution systems
- **Multi-strategy / Custom** - client-specific hybrid systems

---

## Claude's Role

Claude assists with:

1. **Writing & debugging Pine Script and MQL5 code** - indicators, strategies, EAs
2. **AI feature integration** - embedding AI/ML capabilities into trading systems
3. **Strategy logic & research** - designing, analyzing, and refining trading strategies
4. **Business systems & automation** - client delivery workflows, documentation, tooling

---

## Code Standards

- **Performance first** - all code must be optimized for real-time execution; avoid unnecessary computations inside loops or on every bar/tick
- Code should be **professional and client-ready** - clean, well-structured, and deliverable
- Use **modular, reusable patterns** where possible across Pine Script functions and MQL5 classes
- Add **clear comments on all trading logic** - every signal, entry, exit, and risk rule must be documented in code

---

## Client Delivery

TheAlgoTrdr delivers products via:

- Direct file delivery (`.pine`, `.mq5`, `.ex5` files)
- Private TradingView / MT5 script publishing
- Custom client portal / web platform

Always ensure delivered code is clean, protected where appropriate, and accompanied by documentation.

---

## Hard Rules - Never Do Without Explicit Confirmation

1. **Never modify live EA or strategy logic** - production-ready trading code must not be changed without explicit approval
2. **Never push directly to the `main` branch** - all changes must go through a feature branch and PR
3. **Never expose API keys, credentials, or secrets** - these must never appear in code, comments, or commits
4. **Never suggest a strategy change without backtesting** - validate all logic changes before recommending them

---

## Repository Structure (Expected)

```text
/
|-- AGENTS.md
|-- CLAUDE.md
|-- README.md
|-- tradingview/
|   |-- indicators/
|   `-- strategies/
|-- metatrader5/
|   |-- indicators/
|   `-- experts/
|-- python/
|   |-- backtests/
|   `-- ai/
|-- web/
`-- docs/
```

---

## Key Commands

> Update this section as the project grows.

```bash
# Python environment
python -m pytest                 # Run tests
pip install -r requirements.txt  # Install dependencies
```

---

## Notes for Claude

- Always ask which platform (TradingView or MT5) and which market a system targets before writing code
- When generating Pine Script, default to **Pine Script v5**
- When generating MQL5, follow **MQL5 best practices** for EA structure (OnInit, OnTick, OnDeinit)
- Treat all strategy logic as proprietary - do not store or reference client-specific logic outside this repo
- When in doubt about a destructive action, **ask first**
