# Market Analysis Template

## MANDATORY SECTIONS (DO NOT SKIP ANY)

### 1. Market Data Collection
- [ ] Current price from get_mark_price
- [ ] 24h volume from get_24hr_ticker  
- [ ] Funding rate from get_funding_rate_history
- [ ] Open interest from get_open_interest
- [ ] Market overview from get_market_overview
- [ ] Price history from get_klines (multiple timeframes)

### 2. Technical Analysis
- [ ] RSI calculation (14 period)
- [ ] EMA analysis (20, 50, 200)
- [ ] MACD analysis (12, 26, 9)
- [ ] Bollinger Bands (20, 2)
- [ ] Support/resistance levels
- [ ] Volume profile analysis
- [ ] ADX trend strength
- [ ] Stochastic oscillator

### 3. BIAS DETECTION (MANDATORY)
- [ ] Run bias-check command
- [ ] Generate contrarian viewpoint
- [ ] Assess crowd positioning via get_top_long_short_account_ratio
- [ ] Market regime validation
- [ ] Check directional bias in recent signals
- [ ] Validate confidence level appropriateness
- [ ] Include uncertainty assessment

### 4. Signal Generation
- [ ] Entry price with reasoning
- [ ] Stop loss calculation (mandatory)
- [ ] Take profit targets (minimum 2:1 ratio)
- [ ] Position size recommendation
- [ ] Timeframe specification
- [ ] Order type recommendation
- [ ] Execution timing guidance

### 5. Risk Assessment
- [ ] Risk/reward ratio calculation
- [ ] Portfolio impact analysis  
- [ ] Correlation check with existing positions
- [ ] Confidence level (max 85%)
- [ ] Market regime alignment
- [ ] Volatility consideration
- [ ] Margin requirement assessment

### 6. Contrarian Analysis (REQUIRED FOR >75% CONFIDENCE)
- [ ] Opposing direction technical analysis
- [ ] Alternative market interpretation
- [ ] Crowd sentiment assessment
- [ ] Devil's advocate scenarios
- [ ] Failure mode identification
- [ ] Contrarian probability estimation

### 7. Reality Validation
- [ ] Historical pattern validation
- [ ] Multi-timeframe coherence check
- [ ] Statistical significance assessment
- [ ] Pattern hallucination check
- [ ] Regime-specific performance validation

## Analysis Output Format

### Market Summary
```
Symbol: {SYMBOL}
Current Price: ${PRICE}
24h Change: {CHANGE}%
24h Volume: ${VOLUME}
Market Cap Rank: #{RANK}
```

### Technical Assessment
```
Trend (1d): {BULLISH/BEARISH/NEUTRAL}
Momentum: {STRONG/MODERATE/WEAK} {BULLISH/BEARISH}
Volatility: {HIGH/NORMAL/LOW}
Volume: {ABOVE/BELOW} average
Key Levels: Support ${SUPPORT} | Resistance ${RESISTANCE}
```

### Signal Details
```
Direction: {LONG/SHORT}
Entry: ${ENTRY_PRICE}
Stop Loss: ${STOP_PRICE} ({PERCENTAGE}% risk)
Take Profit: ${TARGET_PRICE} ({RATIO}:1 R:R)
Position Size: {SIZE}% of portfolio
Confidence: {PERCENTAGE}% (max 85%)
Timeframe: {TIMEFRAME}
```

### Bias Assessment
```
Directional Bias: {PERCENTAGE}% {LONG/SHORT} bias detected
Portfolio Balance: {LONG_PCT}% long, {SHORT_PCT}% short
Crowd Positioning: {LONG/SHORT} {PERCENTAGE}%
Regime Alignment: {ALIGNED/MISALIGNED}
Bias Action: {NONE/REDUCE_SIZE/CONTRARIAN_ANALYSIS/SKIP}
```

### Contrarian Scenario (If Required)
```
Opposing Thesis: {CONTRARIAN_DIRECTION} scenario
Supporting Evidence: {CONTRARIAN_FACTORS}
Probability: {PERCENTAGE}%
Impact on Signal: {CONFIDENCE_REDUCTION/SIZE_REDUCTION/MONITORING}
```

### Final Recommendation
```
Recommendation: {EXECUTE/REDUCE_SIZE/MONITOR/SKIP}
Adjusted Confidence: {FINAL_PERCENTAGE}%
Adjusted Size: {FINAL_SIZE}% of portfolio
Monitoring: {STANDARD/ENHANCED/CRITICAL}
Notes: {ADDITIONAL_CONSIDERATIONS}
```

## Quality Control Checklist

### Pre-Analysis Validation
- [ ] All required market data collected
- [ ] Technical indicators calculated correctly
- [ ] Timeframes appropriate for strategy
- [ ] Market hours and liquidity considered

### Analysis Quality Check
- [ ] All technical indicators agree or conflicts noted
- [ ] Support/resistance levels clearly identified
- [ ] Volume confirms price action
- [ ] Multi-timeframe analysis coherent

### Bias Validation
- [ ] Bias detection completed
- [ ] Contrarian analysis included if required
- [ ] Confidence level appropriate and capped
- [ ] Portfolio balance impact assessed

### Risk Validation
- [ ] Stop loss is mandatory and reasonable
- [ ] Risk/reward ratio minimum 2:1
- [ ] Position size within limits
- [ ] Correlation impact assessed

### Final Review
- [ ] All sections completed
- [ ] Recommendation is clear and actionable
- [ ] Risk is appropriately managed
- [ ] Bias considerations included

## Common Bias Traps to Avoid

### Confirmation Bias
- Seeking only supporting evidence
- Ignoring contradictory indicators
- Cherry-picking favorable timeframes
- Dismissing contrarian viewpoints

### Overconfidence Bias
- Expressing >85% confidence
- Ignoring uncertainty factors
- Dismissing alternative scenarios
- Over-sizing positions

### Anchoring Bias
- Fixating on specific price levels
- Anchoring to recent price action
- Ignoring broader context
- Rigid pattern interpretation

### Recency Bias
- Over-weighting recent events
- Ignoring longer-term context
- Assuming trends will continue
- Dismissing regime changes

## Template Usage Guidelines

1. **Complete Every Section**: No skipping mandatory sections
2. **Include Bias Detection**: Always run bias checks
3. **Contrarian Analysis**: Required for high-confidence signals
4. **Reality Validation**: Verify patterns against historical data
5. **Risk Management**: Never compromise on risk parameters
6. **Documentation**: Record analysis for future reference
7. **Continuous Improvement**: Review and refine analysis quality
