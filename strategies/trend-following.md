# Trend Following Strategy

## Strategy Configuration
```yml
strategy:
  name: trend_following
  type: trend_following
  timeframes: [1h, 4h, 1d]
  risk_level: medium
```

## Entry Conditions (BOTH DIRECTIONS REQUIRED)
```yml
entry_conditions:
  long:
    - Price above EMA 20
    - EMA 20 above EMA 50
    - EMA 50 above EMA 200
    - ADX > 25 (strong trend)
    - Volume above average
    - RSI > 50 (bullish momentum)
  short:
    - Price below EMA 20
    - EMA 20 below EMA 50
    - EMA 50 below EMA 200
    - ADX > 25 (strong trend)
    - Volume above average
    - RSI < 50 (bearish momentum)
```

## Exit Conditions
```yml
exit_conditions:
  long:
    - Price closes below EMA 20
    - MACD bearish crossover
    - RSI > 80 (overbought)
    - Stop-loss: 2% below entry
    - Take-profit: 4% above entry (2:1 ratio)
  short:
    - Price closes above EMA 20
    - MACD bullish crossover
    - RSI < 20 (oversold)
    - Stop-loss: 2% above entry
    - Take-profit: 4% below entry (2:1 ratio)
```

## Bias Prevention (MANDATORY)
```yml
bias_checks:
  - require_contrarian_analysis: true
  - validate_regime_alignment: true
  - confidence_cap: 85%
  - position_balance_check: true
  - regime_filtering: "Avoid mean reversion in strong trends"
  - volume_confirmation: "Require volume support for breakouts"
```

## Market Regime Filtering
```yml
preferred_regimes:
  - trending_bull: "Use long trend following"
  - trending_bear: "Use short trend following"
avoid_regimes:
  - ranging_high_vol: "High false breakout risk"
  - ranging_low_vol: "Insufficient momentum"
  - choppy_uncertain: "No clear trend direction"
```

## Risk Management
```yml
risk_parameters:
  position_size: 2% of portfolio per trade
  max_leverage: 5x
  stop_loss: 2% from entry
  take_profit: 4% from entry (minimum 2:1 ratio)
  max_positions: 3 concurrent trend following positions
  correlation_limit: 50% maximum correlation between positions
```

## MCP Tool Requirements
```yml
primary_tools:
  - get_klines: "For EMA and indicator calculation"
  - get_24hr_ticker: "For volume and price data"
  - get_mark_price: "For current price reference"
secondary_tools:
  - get_market_overview: "For market regime detection"
  - get_top_long_short_account_ratio: "For contrarian analysis"
  - place_bracket_order: "For execution with TP/SL"
```

## Implementation Notes
- Calculate EMAs using 20, 50, 200 periods on primary timeframe
- Confirm trend strength with ADX indicator
- Validate volume support for all signals
- Include multi-timeframe confirmation (higher timeframe bias)
- Mandatory bias detection before entry
- Generate contrarian analysis for high-confidence signals
