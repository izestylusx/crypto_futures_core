# Momentum Strategy

## Strategy Configuration
```yml
strategy:
  name: momentum
  type: momentum
  timeframes: [5m, 15m, 1h]
  risk_level: high
```

## Entry Conditions (BOTH DIRECTIONS REQUIRED)
```yml
entry_conditions:
  long:
    - Price breakout above resistance with >2% move
    - Volume spike >200% of average
    - RSI > 60 (momentum confirmation)
    - MACD bullish crossover
    - EMA 20 > EMA 50 (trend alignment)
    - Market regime supportive of momentum
  short:
    - Price breakdown below support with >2% move
    - Volume spike >200% of average
    - RSI < 40 (momentum confirmation)
    - MACD bearish crossover
    - EMA 20 < EMA 50 (trend alignment)
    - Market regime supportive of momentum
```

## Exit Conditions
```yml
exit_conditions:
  long:
    - Momentum exhaustion (RSI > 80)
    - Volume declining below average
    - MACD bearish divergence
    - Stop-loss: 2.5% below entry
    - Take-profit: 5% above entry (2:1 ratio)
    - Trailing stop: 1.5% below highest high
  short:
    - Momentum exhaustion (RSI < 20)
    - Volume declining below average
    - MACD bullish divergence
    - Stop-loss: 2.5% above entry
    - Take-profit: 5% below entry (2:1 ratio)
    - Trailing stop: 1.5% above lowest low
```

## Bias Prevention (MANDATORY)
```yml
bias_checks:
  - require_contrarian_analysis: true
  - validate_regime_alignment: true
  - confidence_cap: 85%
  - position_balance_check: true
  - breakout_validation: "Confirm volume and follow-through"
  - false_breakout_check: "Validate against recent failed breakouts"
```

## Market Regime Filtering
```yml
preferred_regimes:
  - trending_bull: "Strong momentum potential"
  - trending_bear: "Short momentum opportunities"
avoid_regimes:
  - ranging_high_vol: "False breakout risk high"
  - ranging_low_vol: "Insufficient momentum"
  - choppy_uncertain: "Conflicting momentum signals"
```

## Risk Management
```yml
risk_parameters:
  position_size: 3% of portfolio per trade
  max_leverage: 8x
  stop_loss: 2.5% from entry
  take_profit: 5% from entry (2:1 ratio)
  trailing_stop: 1.5% from favorable extreme
  max_positions: 2 concurrent momentum positions
  correlation_limit: 40% maximum correlation between positions
```

## MCP Tool Requirements
```yml
primary_tools:
  - get_klines: "For breakout and indicator analysis"
  - get_24hr_ticker: "For volume spike detection"
  - get_aggregate_trades: "For momentum confirmation"
secondary_tools:
  - get_market_overview: "For market regime assessment"
  - get_top_gainers_losers: "For momentum scanning"
  - place_bracket_order: "For execution with trailing stops"
```

## Implementation Notes
- Identify breakout levels using recent support/resistance
- Confirm breakouts with significant volume increase
- Use multiple timeframe confirmation for higher probability
- Implement trailing stops to capture extended momentum moves
- Include bias detection to avoid FOMO trades
- Validate momentum sustainability before entry
- Monitor for momentum exhaustion signals
