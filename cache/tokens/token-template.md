# {TOKEN} Profile Template

## Token Basic Information
```yml
token_info:
  symbol: {SYMBOL}
  full_name: {FULL_TOKEN_NAME}
  market_cap_rank: #{RANK}
  exchange: "binance_futures"
  base_currency: "USDT"
  minimum_quantity: {MIN_QTY}
  price_precision: {DECIMAL_PLACES}
  quantity_precision: {DECIMAL_PLACES}
```

## Market Data Summary
```yml
current_market_data:
  price: ${CURRENT_PRICE}
  change_24h: {PERCENTAGE}%
  volume_24h: ${VOLUME}
  market_cap: ${MARKET_CAP}
  circulating_supply: {SUPPLY}
  max_supply: {MAX_SUPPLY}
  
  price_ranges:
    day_high: ${HIGH}
    day_low: ${LOW}
    week_high: ${WEEK_HIGH}
    week_low: ${WEEK_LOW}
    month_high: ${MONTH_HIGH}
    month_low: ${MONTH_LOW}
    ath: ${ALL_TIME_HIGH}
    atl: ${ALL_TIME_LOW}
```

## Technical Analysis Profile
```yml
technical_characteristics:
  volatility_profile: {HIGH/MEDIUM/LOW}
  average_daily_range: {PERCENTAGE}%
  typical_volume: ${AVERAGE_VOLUME}
  liquidity_rating: {EXCELLENT/GOOD/FAIR/POOR}
  
  support_resistance_levels:
    major_support: [{LEVEL_1}, {LEVEL_2}, {LEVEL_3}]
    major_resistance: [{LEVEL_1}, {LEVEL_2}, {LEVEL_3}]
    key_psychological_levels: [{LEVEL_1}, {LEVEL_2}]
    
  trend_characteristics:
    trending_tendency: {STRONG/MODERATE/WEAK}
    mean_reversion_tendency: {STRONG/MODERATE/WEAK}
    breakout_reliability: {HIGH/MEDIUM/LOW}
    false_breakout_frequency: {HIGH/MEDIUM/LOW}
```

## Trading Strategy Effectiveness
```yml
strategy_performance:
  trend_following:
    effectiveness: {EXCELLENT/GOOD/FAIR/POOR}
    best_timeframes: [{TF_1}, {TF_2}]
    success_rate: {PERCENTAGE}%
    notes: "{SPECIFIC_NOTES}"
    
  mean_reversion:
    effectiveness: {EXCELLENT/GOOD/FAIR/POOR}
    best_timeframes: [{TF_1}, {TF_2}]
    success_rate: {PERCENTAGE}%
    notes: "{SPECIFIC_NOTES}"
    
  momentum:
    effectiveness: {EXCELLENT/GOOD/FAIR/POOR}
    best_timeframes: [{TF_1}, {TF_2}]
    success_rate: {PERCENTAGE}%
    notes: "{SPECIFIC_NOTES}"
    
  grid_trading:
    effectiveness: {EXCELLENT/GOOD/FAIR/POOR}
    typical_range: {PERCENTAGE}%
    success_rate: {PERCENTAGE}%
    notes: "{SPECIFIC_NOTES}"
```

## Bias and Behavioral Patterns
```yml
bias_characteristics:
  directional_bias_tendency: {LONG/SHORT/NEUTRAL}
  confidence_bias_risk: {HIGH/MEDIUM/LOW}
  common_false_patterns:
    - pattern: "{PATTERN_NAME}"
      failure_rate: {PERCENTAGE}%
      notes: "{FAILURE_CHARACTERISTICS}"
      
  sentiment_sensitivity:
    news_impact: {HIGH/MEDIUM/LOW}
    social_media_impact: {HIGH/MEDIUM/LOW}
    whale_movement_impact: {HIGH/MEDIUM/LOW}
    
  crowd_behavior:
    retail_favorite: {TRUE/FALSE}
    institutional_interest: {HIGH/MEDIUM/LOW}
    typical_positioning_extremes: {DESCRIPTION}
```

## Risk Characteristics
```yml
risk_profile:
  volatility_ranking: {HIGH/MEDIUM/LOW}
  correlation_with_btc: {PERCENTAGE}%
  correlation_with_eth: {PERCENTAGE}%
  correlation_with_market: {PERCENTAGE}%
  
  risk_factors:
    liquidity_risk: {HIGH/MEDIUM/LOW}
    manipulation_risk: {HIGH/MEDIUM/LOW}
    news_sensitivity: {HIGH/MEDIUM/LOW}
    technical_reliability: {HIGH/MEDIUM/LOW}
    
  recommended_position_sizing:
    conservative: {PERCENTAGE}% of portfolio
    moderate: {PERCENTAGE}% of portfolio
    aggressive: {PERCENTAGE}% of portfolio
    maximum_recommended: {PERCENTAGE}% of portfolio
```

## Historical Analysis Results
```yml
analysis_history:
  - date: {DATE}
    analysis_type: {TREND/REVERSAL/BREAKOUT}
    signal_direction: {LONG/SHORT}
    confidence: {PERCENTAGE}%
    outcome: {SUCCESS/FAILURE}
    pnl: {VALUE}
    lesson_learned: "{LESSON}"
    
  - date: {DATE}
    analysis_type: {BIAS_DETECTION}
    bias_detected: {BIAS_TYPE}
    correction_applied: {CORRECTION}
    effectiveness: {SUCCESSFUL/UNSUCCESSFUL}
    notes: "{NOTES}"
    
  # ... additional historical entries
```

## Pattern Success Rates
```yml
technical_patterns:
  triangles:
    ascending: {SUCCESS_RATE}%
    descending: {SUCCESS_RATE}%
    symmetrical: {SUCCESS_RATE}%
    
  head_and_shoulders:
    standard: {SUCCESS_RATE}%
    inverse: {SUCCESS_RATE}%
    
  double_tops_bottoms:
    double_top: {SUCCESS_RATE}%
    double_bottom: {SUCCESS_RATE}%
    
  flags_pennants:
    bull_flag: {SUCCESS_RATE}%
    bear_flag: {SUCCESS_RATE}%
    pennant: {SUCCESS_RATE}%
    
  wedges:
    rising_wedge: {SUCCESS_RATE}%
    falling_wedge: {SUCCESS_RATE}%
```

## Optimal Trading Conditions
```yml
best_trading_conditions:
  market_regime: [{REGIME_1}, {REGIME_2}]
  volatility_environment: {HIGH/MEDIUM/LOW}
  volume_requirements: ">{VOLUME_THRESHOLD}"
  time_of_day: [{SESSION_1}, {SESSION_2}]
  
avoid_trading_conditions:
  market_regime: [{AVOID_REGIME_1}]
  volatility_environment: {AVOID_VOLATILITY}
  volume_conditions: "<{VOLUME_THRESHOLD}"
  news_events: [{EVENT_TYPE_1}, {EVENT_TYPE_2}]
```

## Key Levels and Zones
```yml
critical_levels:
  major_support_zones:
    - level: ${LEVEL}
      strength: {STRONG/MEDIUM/WEAK}
      test_count: {COUNT}
      last_test: {DATE}
      
  major_resistance_zones:
    - level: ${LEVEL}
      strength: {STRONG/MEDIUM/WEAK}
      test_count: {COUNT}
      last_test: {DATE}
      
  fibonacci_levels:
    - level: ${LEVEL}
      ratio: {FIBONACCI_RATIO}
      significance: {HIGH/MEDIUM/LOW}
```

## Funding Rate Characteristics
```yml
funding_rate_profile:
  average_funding_rate: {RATE}%
  funding_rate_volatility: {HIGH/MEDIUM/LOW}
  extreme_funding_events:
    - date: {DATE}
      rate: {EXTREME_RATE}%
      market_impact: {DESCRIPTION}
      
  funding_rate_signals:
    contrarian_threshold: {RATE}%
    trend_confirmation_threshold: {RATE}%
```

## Notes and Observations
```yml
trading_notes:
  key_observations:
    - "{OBSERVATION_1}"
    - "{OBSERVATION_2}"
    - "{OBSERVATION_3}"
    
  trading_tips:
    - "{TIP_1}"
    - "{TIP_2}"
    - "{TIP_3}"
    
  common_mistakes:
    - mistake: "{MISTAKE_DESCRIPTION}"
      solution: "{SOLUTION}"
      
  best_practices:
    - "{BEST_PRACTICE_1}"
    - "{BEST_PRACTICE_2}"
```

## Update History
```yml
profile_updates:
  - date: {DATE}
    update_type: {DATA_REFRESH/ANALYSIS_UPDATE/PATTERN_UPDATE}
    changes_made: "{CHANGES_DESCRIPTION}"
    updated_by: {ANALYST_ID}
    
  last_comprehensive_review: {DATE}
  next_scheduled_review: {DATE}
  update_frequency: {WEEKLY/MONTHLY/QUARTERLY}
```

## Integration with Memory System
```yml
memory_integration:
  save_format: "TOKEN_PROFILE:{symbol}:{update_date}:{summary}"
  recall_format: "Retrieve {symbol} trading characteristics and history"
  cross_reference: "Link with session memory and analysis history"
  learning_integration: "Update profile based on trading outcomes"
```
