# Mean Reversion Strategy

## Strategy Configuration
```yml
strategy:
  name: mean_reversion
  type: mean_reversion
  timeframes: [15m, 1h, 4h]
  risk_level: medium
```

## Entry Conditions (BOTH DIRECTIONS REQUIRED)
```yml
entry_conditions:
  long:
    - RSI < 30 (oversold)
    - Price at lower Bollinger Band
    - Price below EMA 20 by >2%
    - Volume spike (>150% average)
    - No strong downtrend (ADX < 25)
    - Bullish divergence (price vs RSI)
  short:
    - RSI > 70 (overbought)
    - Price at upper Bollinger Band
    - Price above EMA 20 by >2%
    - Volume spike (>150% average)
    - No strong uptrend (ADX < 25)
    - Bearish divergence (price vs RSI)
```

## Exit Conditions
```yml
exit_conditions:
  long:
    - RSI > 50 (return to neutral)
    - Price reaches EMA 20
    - Price reaches upper Bollinger Band
    - Stop-loss: 1.5% below entry
    - Take-profit: 3% above entry (2:1 ratio)
  short:
    - RSI < 50 (return to neutral)
    - Price reaches EMA 20
    - Price reaches lower Bollinger Band
    - Stop-loss: 1.5% above entry
    - Take-profit: 3% below entry (2:1 ratio)
```

## Bias Prevention (MANDATORY)
```yml
bias_checks:
  - require_contrarian_analysis: true
  - validate_regime_alignment: true
  - confidence_cap: 85%
  - position_balance_check: true
  - regime_filtering: "Avoid mean reversion in strong trends"
  - divergence_confirmation: "Require RSI divergence confirmation"
```

## Market Regime Filtering
```yml
preferred_regimes:
  - ranging_high_vol: "Perfect for mean reversion"
  - ranging_low_vol: "Good for tight range trading"
avoid_regimes:
  - trending_bull: "Strong trends don't revert"
  - trending_bear: "Strong trends don't revert"
  - choppy_uncertain: "Unclear range boundaries"
```

## Risk Management
```yml
risk_parameters:
  position_size: 1.5% of portfolio per trade
  max_leverage: 3x
  stop_loss: 1.5% from entry
  take_profit: 3% from entry (2:1 ratio)
  max_positions: 4 concurrent mean reversion positions
  correlation_limit: 30% maximum correlation between positions
```

## MCP Tool Requirements
```yml
primary_tools:
  - get_klines: "For RSI and Bollinger Band calculation"
  - get_24hr_ticker: "For volume analysis"
  - get_mark_price: "For current price reference"
secondary_tools:
  - get_market_overview: "For regime detection"
  - get_taker_buy_sell_volume: "For volume spike confirmation"
  - place_bracket_order: "For execution with tight TP/SL"
```

## Implementation Notes
- Calculate RSI using 14-period setting
- Use Bollinger Bands with 20-period SMA and 2 standard deviations
- Confirm volume spikes for entry validation
- Avoid mean reversion during strong trending conditions
- Include regime filtering to prevent strategy misalignment
- Mandatory bias detection before entry
- Look for divergence patterns between price and RSI
