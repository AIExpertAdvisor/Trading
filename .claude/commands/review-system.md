# Review Trading System

Use this skill to audit and review a completed trading system before delivery or live deployment.

## Instructions

Ask the user for the following before starting the review:

1. **File location** — Which file should be reviewed? (provide path or paste the code)
2. **Platform** — Is this Pine Script (TradingView) or MQL5 (MetaTrader 5)?
3. **Product type** — Is it an Indicator, Strategy, or Expert Advisor?
4. **Intended logic** — Briefly describe what the system is supposed to do (entry, exit, risk rules)
5. **Delivery target** — Is this for internal use or client delivery?

---

## Review Checklist

Once the code is provided, audit against all of the following:

### Logic & Correctness
- [ ] Does the entry logic match the intended strategy description?
- [ ] Does the exit logic (take profit, stop loss, trailing stop) work correctly?
- [ ] Are there any off-by-one errors, lookahead bias, or repainting issues?
- [ ] Are all conditions properly sequenced (e.g. signal confirmed before order placed)?
- [ ] Are edge cases handled (no data, gaps, holidays, low liquidity)?

### Risk Management
- [ ] Is stop loss implemented and correctly calculated?
- [ ] Is take profit implemented and correctly calculated?
- [ ] Is lot sizing / position sizing logic sound?
- [ ] Is there a maximum drawdown or daily loss limit?
- [ ] Are risk parameters configurable via inputs (not hardcoded)?

### Performance
- [ ] Are there any unnecessary calculations running on every bar/tick?
- [ ] Are heavy computations cached or calculated only when needed?
- [ ] Are arrays, loops, and series used efficiently?
- [ ] Is the code free of redundant or duplicate logic?

### Code Quality
- [ ] Are all inputs documented with clear descriptions and sensible defaults?
- [ ] Is trading logic commented clearly — every signal, entry, exit, and risk rule?
- [ ] Are variable and function names descriptive and consistent?
- [ ] Is the code structure clean and easy to follow?
- [ ] Are there any hardcoded values that should be inputs?

### Platform-Specific (Pine Script)
- [ ] Is the script using Pine Script v5?
- [ ] Are alerts configured correctly if required?
- [ ] Is repainting behaviour documented and intentional?
- [ ] Are `request.security()` calls used correctly to avoid lookahead?

### Platform-Specific (MQL5)
- [ ] Are OnInit, OnTick, OnDeinit structured correctly?
- [ ] Are orders managed safely (no duplicate orders, correct magic number)?
- [ ] Is symbol and timeframe handling correct?
- [ ] Are trade errors handled gracefully?
- [ ] Is the EA safe to run on multiple pairs simultaneously?

### Client Readiness
- [ ] Is the code free of any API keys, credentials, or private data?
- [ ] Is the code professional and presentable for delivery?
- [ ] Are there any debug prints or test artefacts left in the code?
- [ ] Is documentation or a usage guide needed?

---

## Output

Provide a structured review report with:

1. **Overall verdict** — Ready for delivery / Needs fixes / Major issues found
2. **Issues found** — List each issue with severity (Critical / Major / Minor)
3. **Suggested fixes** — For each issue, provide the corrected code or clear instructions
4. **Performance notes** — Any optimisation recommendations
5. **Client readiness score** — Rate out of 10 with brief justification
6. **Next steps** — What should be done before this system is deployed or delivered
