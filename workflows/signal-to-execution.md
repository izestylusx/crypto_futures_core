# Signal-to-Execution Workflow

## Step-by-Step Process (FOLLOW EXACTLY)

### Step 1: Market Analysis
1. Call market-analyst agent
2. Use get_klines for technical analysis
3. Generate initial signal
4. **MANDATORY**: Run bias-check on signal

### Step 2: Bias Validation  
1. Call bias-detector utility
2. Run contrarian-engine analysis
3. Check directional bias percentage
4. Apply confidence adjustments

### Step 3: Risk Validation
1. Call risk-manager agent
2. Use get_position_info and get_balance
3. Calculate position sizing
4. Validate against risk limits

### Step 4: Execution Decision
1. If all validations pass → proceed
2. If bias detected → reduce size or skip
3. Call execution-trader agent
4. Use place_bracket_order for execution

## Detailed Workflow Steps

### Market Analysis Phase
```yml
step_1_1_data_collection:
  required_data:
    - Current price via get_mark_price
    - Historical data via get_klines (multiple timeframes)
    - Volume data via get_24hr_ticker
    - Market overview via get_market_overview
  
step_1_2_technical_analysis:
  indicators_required:
    - Trend: EMA 20, 50, 200
    - Momentum: RSI, MACD
    - Volatility: Bollinger Bands, ATR
    - Volume: Volume SMA, OBV
  
step_1_3_signal_generation:
  output_required:
    - Direction (long/short)
    - Entry price
    - Stop-loss level
    - Take-profit target
    - Confidence level (initial)
    - Reasoning/justification
```

### Bias Validation Phase (CRITICAL)
```yml
step_2_1_bias_detection:
  bias_checks:
    - Directional bias: Check last 24h signal distribution
    - Confidence bias: Validate against overconfidence threshold
    - Position bias: Check portfolio balance
    - Regime bias: Validate signal against market regime
  
step_2_2_contrarian_analysis:
  required_analysis:
    - Generate opposite direction thesis
    - Find supporting evidence for contrarian view
    - Assess crowd positioning using get_top_long_short_account_ratio
    - Calculate probability of contrarian scenario
  
step_2_3_reality_validation:
  validation_steps:
    - Check pattern against historical data
    - Validate multi-timeframe coherence
    - Assess statistical significance
    - Flag potential pattern hallucination
  
step_2_4_confidence_adjustment:
  adjustment_rules:
    - Reduce confidence by bias percentage if >50% directional bias
    - Cap confidence at 85% maximum
    - Require additional confirmation if bias detected
    - Apply contrarian probability weighting
```

### Risk Validation Phase
```yml
step_3_1_portfolio_assessment:
  required_checks:
    - Current positions via get_position_info
    - Available balance via get_balance
    - Margin utilization via get_account_info
    - Correlation analysis with existing positions
  
step_3_2_position_sizing:
  calculation_method:
    - Risk percentage: 2% of portfolio default
    - Account for correlation with existing positions
    - Adjust for market volatility (ATR-based)
    - Consider leverage impact on risk
  
step_3_3_risk_limits_validation:
  limits_to_check:
    - Maximum portfolio risk: 10%
    - Maximum position risk: 5%
    - Maximum leverage: 20x (recommended 5x)
    - Maximum correlation: 70% between positions
    - Drawdown threshold: 20%
  
step_3_4_margin_requirements:
    - Calculate required margin via margin_requirement
    - Validate against available balance
    - Account for potential adverse moves
    - Include buffer for market volatility
```

### Execution Decision Phase
```yml
step_4_1_final_validation:
  go_no_go_criteria:
    - All bias checks passed or acceptable
    - Risk limits within parameters
    - Sufficient margin available
    - Market conditions favorable
    - No conflicting positions
  
step_4_2_execution_preparation:
  order_parameters:
    - Symbol and direction
    - Position size (validated)
    - Entry price (market or limit)
    - Stop-loss level (mandatory)
    - Take-profit target (recommended 2:1 ratio)
    - Order type selection
  
step_4_3_execution:
  execution_method:
    - Use place_bracket_order for complete setup
    - Include stop-loss and take-profit
    - Monitor execution quality
    - Confirm order placement
    - Update position tracking
  
step_4_4_post_execution:
  required_actions:
    - Confirm order execution
    - Update portfolio tracking
    - Set monitoring alerts
    - Record execution details
    - Plan position management
```

## Decision Trees for Different Scenarios

### Bias Detection Outcomes
```yml
no_bias_detected:
  confidence_adjustment: "No adjustment needed"
  position_size: "Standard size calculation"
  execution: "Proceed with normal execution"
  
moderate_bias_detected:
  confidence_adjustment: "Reduce confidence by 10-20%"
  position_size: "Reduce size by 25%"
  execution: "Proceed with enhanced monitoring"
  
high_bias_detected:
  confidence_adjustment: "Reduce confidence by 30-50%"
  position_size: "Reduce size by 50%"
  execution: "Require additional confirmation"
  
critical_bias_detected:
  confidence_adjustment: "Reduce confidence by 50%+"
  position_size: "Consider skipping trade"
  execution: "Manual review required"
```

### Risk Validation Outcomes
```yml
risk_acceptable:
  action: "Proceed to execution"
  monitoring: "Standard position monitoring"
  
risk_elevated:
  action: "Reduce position size"
  adjustment: "Reduce size until risk acceptable"
  monitoring: "Enhanced risk monitoring"
  
risk_excessive:
  action: "Skip trade"
  alternative: "Look for lower-risk opportunities"
  monitoring: "Continue market monitoring"
```

## Integration with MCP Tools
```yml
market_analysis_tools:
  - get_klines: "Multi-timeframe technical analysis"
  - get_24hr_ticker: "Volume and price movement data"
  - get_mark_price: "Current price reference"
  - get_market_overview: "Market regime assessment"
  
bias_validation_tools:
  - get_top_long_short_account_ratio: "Crowd sentiment analysis"
  - mcp_openmemory_search-memories: "Historical bias tracking"
  - mcp_openmemory_add-memory: "Save bias analysis results"
  
risk_assessment_tools:
  - get_position_info: "Current position analysis"
  - get_balance: "Available capital assessment"
  - get_account_info: "Account status and margins"
  - get_leverage_brackets: "Leverage validation"
  
execution_tools:
  - place_bracket_order: "Complete order with TP/SL"
  - place_order: "Alternative order placement"
  - get_open_orders: "Execution confirmation"
```

## Error Handling and Monitoring
```yml
error_scenarios:
  insufficient_margin:
    response: "Reduce position size or skip trade"
    monitoring: "Alert user to margin constraint"
    
  market_closure:
    response: "Queue order for market open"
    monitoring: "Track market session status"
    
  execution_failure:
    response: "Retry with adjusted parameters"
    monitoring: "Alert user to execution issue"
    
  bias_override_request:
    response: "Require explicit user confirmation"
    monitoring: "Log override decision for analysis"
```

## Success Metrics
- Execution success rate: >95%
- Bias detection accuracy: >80%
- Risk limit adherence: 100%
- Average execution time: <30 seconds
- Signal-to-execution conversion: >70% when all validations pass
