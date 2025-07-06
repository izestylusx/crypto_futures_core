# Grid Trading Strategy

## Strategy Configuration
```yml
strategy:
  name: grid_trading
  type: grid
  timeframes: [15m, 1h, 4h]
  risk_level: low
```

## Entry Conditions (BOTH DIRECTIONS REQUIRED)
```yml
entry_conditions:
  long:
    - Price within defined range (support to resistance)
    - No strong trend (ADX < 20)
    - Bollinger Band width < 20th percentile
    - Place buy orders at support levels
    - Grid spacing: 1-2% between orders
    - Volume confirmation for range validation
  short:
    - Price within defined range (support to resistance)
    - No strong trend (ADX < 20)
    - Bollinger Band width < 20th percentile
    - Place sell orders at resistance levels
    - Grid spacing: 1-2% between orders
    - Volume confirmation for range validation
```

## Grid Configuration
```yml
grid_parameters:
  grid_spacing: 1.5%  # Distance between grid levels
  grid_levels: 10     # Number of grid levels each direction
  order_size: 0.5%    # Size per grid order (% of portfolio)
  range_detection:
    - support_level: "Recent swing low"
    - resistance_level: "Recent swing high"
    - range_validation: "Minimum 5% range width"
    - volatility_check: "BB width < 20th percentile"
```

## Exit Conditions
```yml
exit_conditions:
  range_break_long:
    - Price breaks above resistance by >2%
    - Strong volume confirmation
    - Close all short grid orders
    - Convert to trend following if confirmed
  range_break_short:
    - Price breaks below support by >2%
    - Strong volume confirmation
    - Close all long grid orders
    - Convert to trend following if confirmed
  profit_taking:
    - Each grid order has opposite side profit target
    - Take profit at next grid level
    - Reestablish grid after profit taking
```

## Bias Prevention (MANDATORY)
```yml
bias_checks:
  - require_contrarian_analysis: true
  - validate_regime_alignment: true
  - confidence_cap: 85%
  - position_balance_check: true
  - equal_grid_distribution: "Equal long and short grid orders"
  - range_confirmation: "Validate range boundaries"
```

## Market Regime Filtering
```yml
preferred_regimes:
  - ranging_low_vol: "Perfect for grid trading"
  - ranging_high_vol: "Good but wider grids needed"
avoid_regimes:
  - trending_bull: "Range breaks likely"
  - trending_bear: "Range breaks likely"
  - choppy_uncertain: "Unclear range boundaries"
```

## Risk Management
```yml
risk_parameters:
  total_grid_risk: 5% of portfolio maximum
  individual_order_size: 0.5% of portfolio
  max_leverage: 2x
  range_break_stop: 2% beyond range boundary
  correlation_limit: Grid orders are naturally correlated
  position_balance: Equal long and short exposure
```

## MCP Tool Requirements
```yml
primary_tools:
  - get_klines: "For range identification and ADX calculation"
  - place_multiple_orders: "For grid order placement"
  - get_book_ticker: "For current bid/ask reference"
secondary_tools:
  - cancel_all_orders: "For grid reset on range break"
  - get_open_orders: "For grid monitoring"
  - modify_order: "For grid adjustment"
```

## Implementation Notes
- Identify range boundaries using recent swing highs/lows
- Validate range with sufficient width (minimum 5%)
- Place equal number of buy and sell orders
- Monitor for range breaks with volume confirmation
- Automatically reset grid after range break
- Include bias prevention for directional grids
- Equal distribution of long and short orders mandatory
