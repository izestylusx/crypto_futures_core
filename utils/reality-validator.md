# Reality Validator Utility

## Purpose
Validate patterns against historical data and detect pattern hallucination

## Reality Validation Functions
```yml
validation_functions:
  pattern_validation:
    input: "pattern_type, symbol, timeframe"
    output: "historical_success_rate, pattern_reliability"
    process:
      - "Search historical data for similar patterns"
      - "Calculate success rate of pattern"
      - "Assess pattern reliability score"
      - "Compare against random probability"
      
  breakout_validation:
    input: "breakout_signal, volume_data"
    output: "breakout_probability, false_breakout_risk"
    process:
      - "Analyze historical breakout success rates"
      - "Validate volume confirmation"
      - "Check for false breakout patterns"
      - "Calculate breakout sustainability"
      
  indicator_coherence:
    input: "multiple_indicators, timeframes"
    output: "coherence_score, conflicting_signals"
    process:
      - "Check indicator alignment across timeframes"
      - "Identify conflicting signals"
      - "Calculate overall coherence score"
      - "Flag inconsistent analysis"
      
  market_condition_validation:
    input: "signal, current_market_regime"
    output: "regime_alignment_score, historical_performance"
    process:
      - "Compare signal against similar market conditions"
      - "Validate strategy performance in current regime"
      - "Check historical precedent"
      - "Calculate regime-adjusted probability"
```

## Historical Data Validation
```yml
data_requirements:
  minimum_lookback: "90 days for pattern validation"
  sample_size: "Minimum 20 occurrences for statistical significance"
  timeframe_coverage: "Multiple timeframes for confirmation"
  regime_coverage: "Different market regimes represented"
  
validation_criteria:
  pattern_reliability:
    excellent: ">70% success rate"
    good: "50-70% success rate"
    poor: "30-50% success rate"
    unreliable: "<30% success rate"
    
  sample_significance:
    high_confidence: ">50 occurrences"
    medium_confidence: "20-50 occurrences"
    low_confidence: "10-20 occurrences"
    insufficient: "<10 occurrences"
```

## Pattern Hallucination Detection
```yml
hallucination_checks:
  overfitting_detection:
    - "Check if pattern is too specific"
    - "Validate against out-of-sample data"
    - "Test pattern robustness"
    - "Assess parameter sensitivity"
    
  confirmation_bias_check:
    - "Search for counter-examples"
    - "Validate negative cases"
    - "Check cherry-picking tendency"
    - "Assess selection bias"
    
  randomness_test:
    - "Compare against random patterns"
    - "Statistical significance testing"
    - "Monte Carlo validation"
    - "Null hypothesis testing"
    
  regime_dependency:
    - "Test pattern across different regimes"
    - "Validate regime-specific performance"
    - "Check regime change impact"
    - "Assess pattern stability"
```

## Multi-Timeframe Coherence
```yml
coherence_checks:
  timeframe_alignment:
    required_timeframes: [5m, 15m, 1h, 4h, 1d]
    alignment_threshold: "70% of timeframes must agree"
    weight_distribution:
      - "1d: 40% weight (primary trend)"
      - "4h: 30% weight (intermediate trend)"
      - "1h: 20% weight (short-term trend)"
      - "15m: 10% weight (execution timing)"
      
  signal_coherence:
    trend_alignment: "All timeframes show same trend direction"
    momentum_coherence: "Momentum indicators align across timeframes"
    volume_confirmation: "Volume supports signal across timeframes"
    support_resistance: "Key levels respected across timeframes"
    
  conflict_resolution:
    major_conflict: "Primary timeframes disagree"
    minor_conflict: "Secondary timeframes disagree"
    resolution_priority: "Higher timeframes take precedence"
    confidence_adjustment: "Reduce confidence for conflicts"
```

## Reality Check Protocols
```yml
validation_sequence:
  step_1_pattern_check:
    - "Identify claimed pattern"
    - "Search historical occurrences"
    - "Calculate success statistics"
    - "Assess statistical significance"
    
  step_2_regime_validation:
    - "Identify current market regime"
    - "Find similar historical regimes"
    - "Validate pattern performance in regime"
    - "Calculate regime-adjusted probability"
    
  step_3_coherence_validation:
    - "Check multi-timeframe alignment"
    - "Validate indicator coherence"
    - "Identify conflicting signals"
    - "Calculate overall coherence score"
    
  step_4_final_assessment:
    - "Combine all validation scores"
    - "Generate reliability rating"
    - "Provide confidence adjustment"
    - "Flag potential hallucinations"
```

## MCP Tools Integration
```yml
primary_tools:
  - get_klines: "Historical data for pattern validation"
  - get_24hr_ticker: "Current market condition validation"
  - get_market_overview: "Market regime identification"
  
validation_data_sources:
  price_data: "get_klines with extended lookback periods"
  volume_data: "get_24hr_ticker and get_aggregate_trades"
  market_regime: "get_market_overview and regime classification"
  positioning_data: "get_top_long_short_account_ratio"
```

## Reality Check Output
```yml
validation_report:
  pattern_reliability:
    pattern_type: "Identified pattern classification"
    historical_success_rate: "Success rate from historical data"
    sample_size: "Number of historical occurrences"
    statistical_significance: "P-value and confidence interval"
    
  regime_validation:
    current_regime: "Identified market regime"
    regime_performance: "Pattern performance in current regime"
    regime_stability: "Likelihood of regime continuation"
    
  coherence_assessment:
    timeframe_alignment: "Percentage of timeframes agreeing"
    indicator_coherence: "Indicator alignment score"
    conflict_flags: "Identified conflicting signals"
    
  final_assessment:
    reality_score: "Overall reality validation score (0-100)"
    confidence_adjustment: "Recommended confidence adjustment"
    hallucination_risk: "Risk level of pattern hallucination"
    recommendations: "Action recommendations based on validation"
```

## Integration Requirements
- Mandatory for all pattern-based signals
- Required for breakout confirmations
- Integrated with bias detection system
- Connected to contrarian engine for cross-validation
- Memory system integration for learning improvement
