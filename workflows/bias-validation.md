# Bias Validation Workflow

## Step-by-Step Bias Detection and Validation Process

### Step 1: Initial Bias Assessment
1. Analyze signal direction and confidence level
2. Check recent signal history for directional bias
3. Assess portfolio position balance
4. Evaluate market regime alignment

### Step 2: Contrarian Analysis Generation
1. Generate opposing viewpoint for the signal
2. Find supporting evidence for contrarian scenario
3. Assess crowd positioning and sentiment
4. Calculate contrarian probability

### Step 3: Reality Check Validation
1. Validate patterns against historical data
2. Check multi-timeframe coherence
3. Assess statistical significance
4. Flag potential hallucinations

### Step 4: Bias Correction Implementation
1. Apply confidence adjustments based on bias level
2. Implement position size reductions if needed
3. Add monitoring requirements
4. Document bias detection results

## Detailed Bias Validation Steps

### Signal-Level Bias Detection
```yml
step_1_1_directional_bias_check:
  process:
    - Count signals by direction in last 24 hours
    - Calculate long vs short percentage
    - Compare against 50/50 baseline
    - Flag if >70% one direction
  
  bias_thresholds:
    green: "<50% directional bias"
    yellow: "50-60% directional bias"
    orange: "60-70% directional bias"
    red: ">70% directional bias"
  
step_1_2_confidence_bias_check:
  process:
    - Assess signal confidence level
    - Compare against recent confidence average
    - Check for overconfidence pattern
    - Flag if >85% confidence
  
  confidence_rules:
    acceptable: "<75% confidence"
    caution: "75-85% confidence"
    excessive: ">85% confidence"
    maximum_allowed: "85% (hard cap)"

step_1_3_portfolio_bias_check:
  process:
    - Calculate current long vs short exposure
    - Assess position correlation
    - Check sector concentration
    - Validate against balance limits
  
  balance_thresholds:
    balanced: "40-60% each direction"
    moderate_bias: "60-70% one direction"
    high_bias: "70-80% one direction"
    excessive_bias: ">80% one direction"
```

### Contrarian Analysis Process
```yml
step_2_1_opposing_thesis_generation:
  required_elements:
    - Opposite direction technical analysis
    - Alternative market interpretation
    - Contrarian fundamental view
    - Risk scenario development
  
  contrarian_indicators:
    technical: "Hidden divergences, exhaustion patterns"
    sentiment: "Extreme positioning, crowded trades"
    fundamental: "Overvaluation, risk factors"
    timing: "Cycle analysis, seasonal factors"

step_2_2_crowd_sentiment_analysis:
  mcp_tools:
    - get_top_long_short_account_ratio: "Retail positioning"
    - get_taker_buy_sell_volume: "Volume flow analysis"
    - get_open_interest: "Positioning extremes"
  
  contrarian_signals:
    extreme_long: ">80% long positioning"
    extreme_short: ">80% short positioning"
    volume_exhaustion: "Decreasing volume in trend direction"
    positioning_extremes: "Historical positioning extremes"

step_2_3_contrarian_probability_assessment:
  factors:
    historical_reversal_rate: "Similar setups reversal probability"
    positioning_extreme_level: "Degree of crowd concentration"
    technical_divergence_strength: "Momentum divergence magnitude"
    fundamental_misalignment: "Price vs fundamental disconnect"
  
  probability_calculation:
    base_probability: "Historical reversal rate"
    positioning_adjustment: "+/- based on crowd extremes"
    technical_adjustment: "+/- based on divergences"
    final_probability: "Weighted combination of factors"
```

### Reality Validation Integration
```yml
step_3_1_pattern_reality_check:
  validation_process:
    - Identify claimed pattern or setup
    - Search historical data for similar patterns
    - Calculate historical success rate
    - Assess statistical significance
  
  reality_flags:
    validated: ">60% historical success rate"
    questionable: "30-60% historical success rate"
    unreliable: "<30% historical success rate"
    insufficient_data: "<20 historical occurrences"

step_3_2_multi_timeframe_coherence:
  coherence_check:
    - Verify signal consistency across timeframes
    - Check for conflicting indicators
    - Assess trend alignment
    - Validate support/resistance levels
  
  coherence_scoring:
    high_coherence: ">80% timeframe agreement"
    moderate_coherence: "60-80% timeframe agreement"
    low_coherence: "40-60% timeframe agreement"
    incoherent: "<40% timeframe agreement"

step_3_3_hallucination_detection:
  hallucination_flags:
    overfitting: "Pattern too specific or complex"
    cherry_picking: "Selective evidence presentation"
    confirmation_bias: "Ignoring contradictory evidence"
    regime_misalignment: "Pattern invalid in current regime"
```

### Bias Correction Implementation
```yml
step_4_1_confidence_adjustment:
  adjustment_rules:
    no_bias: "No confidence adjustment"
    moderate_bias: "Reduce confidence by 10-20%"
    high_bias: "Reduce confidence by 20-40%"
    critical_bias: "Reduce confidence by 40%+ or skip trade"
  
  adjustment_formula:
    base_confidence: "Original signal confidence"
    bias_penalty: "Percentage reduction based on bias level"
    contrarian_weight: "Contrarian probability impact"
    final_confidence: "base_confidence * (1 - bias_penalty - contrarian_weight)"

step_4_2_position_size_adjustment:
  size_reduction_rules:
    yellow_bias: "Reduce size by 25%"
    orange_bias: "Reduce size by 50%"
    red_bias: "Reduce size by 75% or skip"
    contrarian_high_probability: "Additional 25% reduction"
  
  minimum_thresholds:
    minimum_position_size: "$10 USDT equivalent"
    maximum_reduction: "90% of original size"
    skip_threshold: "If final size <$10 or >90% reduction"

step_4_3_monitoring_requirements:
  enhanced_monitoring:
    bias_flagged_trades: "Hourly position review"
    contrarian_scenarios: "Watch for reversal signals"
    high_confidence_trades: "Monitor for overconfidence"
    crowded_trades: "Track positioning changes"
  
  alert_conditions:
    adverse_movement: ">50% of stop-loss distance"
    contrarian_confirmation: "Opposing signals developing"
    crowd_shift: "Positioning changing rapidly"
    regime_change: "Market regime showing signs of change"
```

## Decision Trees for Bias Scenarios

### High Directional Bias Detected
```yml
scenario_1_high_long_bias:
  if: ">70% long signals in 24h"
  actions:
    - "Generate mandatory short scenario analysis"
    - "Reduce all long signal confidence by 30%"
    - "Look actively for short opportunities"
    - "Reduce long position sizes by 50%"
  
scenario_2_high_short_bias:
  if: ">70% short signals in 24h"
  actions:
    - "Generate mandatory long scenario analysis"
    - "Reduce all short signal confidence by 30%"
    - "Look actively for long opportunities"
    - "Reduce short position sizes by 50%"
```

### Overconfidence Pattern
```yml
scenario_3_overconfidence:
  if: "Average confidence >80% or individual signal >90%"
  actions:
    - "Cap all confidence levels at 75%"
    - "Require additional confirmation"
    - "Include uncertainty statements"
    - "Reduce position sizes by 25%"
    - "Increase monitoring frequency"
```

### Crowd Positioning Extremes
```yml
scenario_4_crowd_extreme:
  if: "Long/short ratio >80% either direction"
  actions:
    - "Generate contrarian analysis"
    - "Consider fade-the-crowd strategy"
    - "Reduce position sizes in crowd direction"
    - "Monitor for positioning shift"
    - "Include crowd reversal scenarios"
```

## Integration with Memory System
```yml
bias_tracking:
  save_format: "BIAS_VALIDATION:{timestamp}:{symbol}:{bias_type}:{level}:{action}"
  recall_format: "Retrieve bias history for pattern analysis"
  
contrarian_tracking:
  save_format: "CONTRARIAN_ANALYSIS:{timestamp}:{symbol}:{probability}:{outcome}"
  recall_format: "Track contrarian analysis success rate"
  
validation_tracking:
  save_format: "REALITY_CHECK:{timestamp}:{pattern}:{success_rate}:{outcome}"
  recall_format: "Improve pattern validation accuracy"
```

## Success Metrics for Bias Validation
- Bias detection accuracy: >85%
- False positive rate: <15%
- Contrarian analysis value: Improve win rate by >10%
- Reality check effectiveness: Reduce false patterns by >50%
- Overall bias correction impact: Improve risk-adjusted returns by >20%
