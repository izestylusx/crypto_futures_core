# Signal Template

## Signal Configuration
```yml
signal:
  symbol: {SYMBOL}
  direction: {LONG/SHORT}
  strategy: {STRATEGY_NAME}
  timeframe: {PRIMARY_TIMEFRAME}
  timestamp: {SIGNAL_TIMESTAMP}
  analyst: {ANALYST_ID}
```

## Signal Details (EXACT FORMAT REQUIRED)
```yml
entry_details:
  entry_price: {PRICE}
  entry_type: {MARKET/LIMIT}
  stop_loss: {STOP_PRICE}
  take_profit: {TARGET_PRICE}
  risk_reward_ratio: {RATIO}
  position_size: {SIZE_PERCENTAGE}%
  
confidence_assessment:
  initial_confidence: {PERCENTAGE}%
  bias_adjusted_confidence: {ADJUSTED_PERCENTAGE}%
  final_confidence: {FINAL_PERCENTAGE}% (max 85%)
  
timing:
  signal_valid_until: {EXPIRY_TIME}
  optimal_execution_window: {TIME_WINDOW}
  market_session: {ASIAN/EUROPEAN/AMERICAN}
```

## Technical Analysis Basis
```yml
primary_indicators:
  trend: 
    - indicator: {EMA/SMA}
    - value: {VALUE}
    - signal: {BULLISH/BEARISH/NEUTRAL}
  
  momentum:
    - indicator: {RSI/MACD/STOCH}
    - value: {VALUE}
    - signal: {BULLISH/BEARISH/NEUTRAL}
  
  volatility:
    - indicator: {BB/ATR}
    - value: {VALUE}
    - signal: {EXPANDING/CONTRACTING/NEUTRAL}
  
  volume:
    - indicator: {VOLUME_SMA/OBV}
    - value: {VALUE}
    - signal: {CONFIRMING/DIVERGING/NEUTRAL}

key_levels:
  support: [{LEVEL_1}, {LEVEL_2}, {LEVEL_3}]
  resistance: [{LEVEL_1}, {LEVEL_2}, {LEVEL_3}]
  pivot_points: [{PP}, {S1}, {S2}, {R1}, {R2}]
```

## Bias Validation Section (MANDATORY)
```yml
bias_assessment:
  directional_bias_check:
    recent_signals_long: {COUNT}
    recent_signals_short: {COUNT}
    bias_percentage: {PERCENTAGE}%
    bias_level: {GREEN/YELLOW/ORANGE/RED}
  
  confidence_bias_check:
    average_recent_confidence: {PERCENTAGE}%
    overconfidence_flag: {TRUE/FALSE}
    confidence_adjustment: {PERCENTAGE}% reduction
  
  portfolio_bias_check:
    current_long_exposure: {PERCENTAGE}%
    current_short_exposure: {PERCENTAGE}%
    balance_flag: {BALANCED/BIASED}
    
  crowd_positioning:
    long_short_ratio: {PERCENTAGE}% long
    positioning_extreme: {TRUE/FALSE}
    contrarian_signal: {TRUE/FALSE}
```

## Contrarian Analysis (Required if confidence >75%)
```yml
contrarian_scenario:
  opposing_direction: {OPPOSITE_DIRECTION}
  contrarian_thesis: "{DETAILED_OPPOSING_VIEWPOINT}"
  supporting_evidence:
    - "{CONTRARIAN_FACTOR_1}"
    - "{CONTRARIAN_FACTOR_2}"
    - "{CONTRARIAN_FACTOR_3}"
  
  contrarian_probability: {PERCENTAGE}%
  impact_on_signal:
    confidence_reduction: {PERCENTAGE}%
    size_reduction: {PERCENTAGE}%
    monitoring_level: {STANDARD/ENHANCED/CRITICAL}
```

## Risk Assessment
```yml
risk_metrics:
  position_risk: {PERCENTAGE}% of portfolio
  portfolio_correlation: {CORRELATION_COEFFICIENT}
  maximum_loss: ${MAX_LOSS_AMOUNT}
  margin_requirement: ${MARGIN_AMOUNT}
  leverage_used: {LEVERAGE}x
  
risk_validation:
  within_position_limit: {TRUE/FALSE}
  within_portfolio_limit: {TRUE/FALSE}
  correlation_acceptable: {TRUE/FALSE}
  margin_sufficient: {TRUE/FALSE}
  
stop_loss_validation:
  stop_distance: {PERCENTAGE}%
  stop_rationale: "{TECHNICAL/VOLATILITY/FIXED_PERCENTAGE}"
  trailing_stop: {TRUE/FALSE}
  break_even_level: {PRICE}
```

## Market Context
```yml
market_regime:
  current_regime: {TRENDING_BULL/TRENDING_BEAR/RANGING_HIGH_VOL/RANGING_LOW_VOL/CHOPPY}
  regime_confidence: {PERCENTAGE}%
  strategy_alignment: {ALIGNED/MISALIGNED}
  regime_risk: {LOW/MEDIUM/HIGH}
  
market_conditions:
  volatility_environment: {HIGH/NORMAL/LOW}
  volume_environment: {HIGH/NORMAL/LOW}
  funding_rate: {RATE}% {8h}
  open_interest_trend: {INCREASING/DECREASING/STABLE}
```

## Execution Plan
```yml
execution_details:
  order_type: {MARKET/LIMIT/STOP}
  limit_price: {PRICE} (if applicable)
  execution_timing: {IMMEDIATE/WAIT_FOR_PULLBACK/BREAKOUT_CONFIRMATION}
  size_scaling: {FULL_SIZE/SCALE_IN/SPLIT_ORDERS}
  
monitoring_plan:
  key_levels_to_watch: [{LEVEL_1}, {LEVEL_2}, {LEVEL_3}]
  indicators_to_monitor: [{INDICATOR_1}, {INDICATOR_2}]
  exit_signals: [{SIGNAL_1}, {SIGNAL_2}]
  time_stop: {TIME_LIMIT} (if applicable)
  
position_management:
  profit_taking_levels: [{LEVEL_1}, {LEVEL_2}, {LEVEL_3}]
  stop_adjustment_plan: "{STOP_MANAGEMENT_STRATEGY}"
  position_scaling_plan: "{SCALING_STRATEGY}"
```

## Signal Validation Checklist
- [ ] Symbol and direction clearly specified
- [ ] Entry price and reasoning provided
- [ ] Stop-loss level mandatory and reasonable
- [ ] Take-profit target with minimum 2:1 R:R
- [ ] Position size within risk limits
- [ ] Confidence level appropriate (max 85%)
- [ ] Bias detection completed
- [ ] Contrarian analysis included (if >75% confidence)
- [ ] Risk assessment validates all parameters
- [ ] Market regime alignment confirmed
- [ ] Execution plan detailed and actionable

## Signal Quality Ratings
```yml
signal_quality:
  technical_quality: {A/B/C/D}
  bias_validation: {PASSED/FAILED}
  risk_assessment: {EXCELLENT/GOOD/POOR}
  overall_rating: {HIGH/MEDIUM/LOW}
  
recommendation:
  action: {EXECUTE/REDUCE_SIZE/MONITOR/SKIP}
  priority: {HIGH/MEDIUM/LOW}
  urgency: {IMMEDIATE/WITHIN_HOUR/END_OF_DAY}
```

## Documentation Requirements
- All signals must be saved to memory system
- Include timestamp and analyst identification
- Record bias detection results
- Track signal outcomes for performance analysis
- Update pattern success rates based on results

## Signal Expiry and Invalidation
```yml
expiry_conditions:
  time_expiry: {HOURS/DAYS}
  technical_invalidation: "{CONDITIONS_THAT_INVALIDATE}"
  market_condition_change: "{REGIME_CHANGE_INVALIDATION}"
  bias_threshold_breach: "Skip if bias >80%"
  
invalidation_actions:
  cancel_pending_orders: {TRUE/FALSE}
  close_partial_positions: {TRUE/FALSE}
  reassess_signal: {TRUE/FALSE}
  generate_new_analysis: {TRUE/FALSE}
```
