# Session Memory

## Purpose
Track current session analysis, decisions, and context for continuity

## Session Metadata
```yml
session_info:
  session_id: {UNIQUE_SESSION_ID}
  start_time: {TIMESTAMP}
  end_time: {TIMESTAMP}
  session_type: {SCALPING/SWING/POSITION/MIXED}
  market_session: {ASIAN/EUROPEAN/AMERICAN}
  user_id: {USER_IDENTIFIER}
```

## Market Context at Session Start
```yml
initial_market_state:
  major_pair_prices:
    BTCUSDT: {PRICE}
    ETHUSDT: {PRICE}
    BNBUSDT: {PRICE}
    
  market_regime: {REGIME_TYPE}
  volatility_level: {HIGH/MEDIUM/LOW}
  volume_environment: {HIGH/NORMAL/LOW}
  overall_sentiment: {BULLISH/BEARISH/NEUTRAL}
  
  key_levels:
    btc_support: [{LEVEL_1}, {LEVEL_2}]
    btc_resistance: [{LEVEL_1}, {LEVEL_2}]
    eth_support: [{LEVEL_1}, {LEVEL_2}]
    eth_resistance: [{LEVEL_1}, {LEVEL_2}]
```

## Session Analysis History
```yml
analysis_sequence:
  - timestamp: {TIME}
    analysis_type: {MARKET_OVERVIEW/SIGNAL_ANALYSIS/BIAS_CHECK}
    symbol: {SYMBOL}
    result: {ANALYSIS_SUMMARY}
    confidence: {PERCENTAGE}
    bias_flags: [{FLAG_1}, {FLAG_2}]
    
  - timestamp: {TIME}
    analysis_type: {CONTRARIAN_ANALYSIS}
    symbol: {SYMBOL}
    original_signal: {DIRECTION}
    contrarian_probability: {PERCENTAGE}
    impact: {CONFIDENCE_REDUCTION/SIZE_REDUCTION}
    
  # ... additional analysis entries
```

## Signal Generation Tracking
```yml
signals_generated:
  - signal_id: {UNIQUE_ID}
    timestamp: {TIME}
    symbol: {SYMBOL}
    direction: {LONG/SHORT}
    strategy: {STRATEGY_NAME}
    entry_price: {PRICE}
    confidence: {PERCENTAGE}
    bias_adjusted_confidence: {PERCENTAGE}
    status: {PENDING/EXECUTED/SKIPPED/EXPIRED}
    
  - signal_id: {UNIQUE_ID}
    timestamp: {TIME}
    symbol: {SYMBOL}
    direction: {LONG/SHORT}
    strategy: {STRATEGY_NAME}
    bias_flags: [{DIRECTIONAL_BIAS}, {OVERCONFIDENCE}]
    contrarian_analysis: {CONTRARIAN_SUMMARY}
    final_decision: {EXECUTE/SKIP/REDUCE_SIZE}
    
  # ... additional signals
```

## Bias Detection Session Summary
```yml
session_bias_metrics:
  total_analyses: {COUNT}
  long_signals: {COUNT}
  short_signals: {COUNT}
  directional_bias_percentage: {PERCENTAGE}
  bias_alerts_triggered: {COUNT}
  contrarian_analyses_required: {COUNT}
  confidence_adjustments: {COUNT}
  
bias_corrections_applied:
  - timestamp: {TIME}
    bias_type: {DIRECTIONAL/CONFIDENCE/PORTFOLIO}
    severity: {GREEN/YELLOW/ORANGE/RED}
    action_taken: {SIZE_REDUCTION/SKIP/CONTRARIAN_ANALYSIS}
    effectiveness: {SUCCESSFUL/UNSUCCESSFUL/PENDING}
    
  # ... additional corrections
```

## Trading Decisions and Outcomes
```yml
execution_decisions:
  - decision_time: {TIMESTAMP}
    signal_id: {SIGNAL_ID}
    decision: {EXECUTE/SKIP/MODIFY}
    reasoning: {DECISION_REASONING}
    risk_assessment: {ACCEPTABLE/ELEVATED/EXCESSIVE}
    bias_impact: {NONE/MINOR/MAJOR}
    
trades_executed:
  - trade_id: {UNIQUE_ID}
    signal_id: {SIGNAL_ID}
    execution_time: {TIMESTAMP}
    symbol: {SYMBOL}
    direction: {LONG/SHORT}
    size: {POSITION_SIZE}
    entry_price: {EXECUTED_PRICE}
    stop_loss: {STOP_PRICE}
    take_profit: {TARGET_PRICE}
    status: {OPEN/CLOSED/STOPPED}
    
positions_monitored:
  - position_id: {UNIQUE_ID}
    symbol: {SYMBOL}
    direction: {LONG/SHORT}
    entry_price: {PRICE}
    current_pnl: {VALUE}
    monitoring_notes: [{NOTE_1}, {NOTE_2}]
```

## Learning and Insights
```yml
session_insights:
  successful_patterns:
    - pattern: {PATTERN_DESCRIPTION}
      success_rate: {PERCENTAGE}
      sample_size: {COUNT}
      notes: {INSIGHT_NOTES}
      
  failed_patterns:
    - pattern: {PATTERN_DESCRIPTION}
      failure_mode: {FAILURE_DESCRIPTION}
      lesson_learned: {LESSON}
      improvement_suggestion: {SUGGESTION}
      
  bias_detection_effectiveness:
    - bias_type: {DIRECTIONAL/CONFIDENCE/PORTFOLIO}
      detection_accuracy: {PERCENTAGE}
      false_positives: {COUNT}
      missed_detections: {COUNT}
      improvement_needed: {TRUE/FALSE}
```

## Market Regime Changes During Session
```yml
regime_changes:
  - change_time: {TIMESTAMP}
    from_regime: {PREVIOUS_REGIME}
    to_regime: {NEW_REGIME}
    trigger_event: {TRIGGER_DESCRIPTION}
    impact_on_strategies: {IMPACT_SUMMARY}
    adaptation_actions: [{ACTION_1}, {ACTION_2}]
    
volatility_events:
  - event_time: {TIMESTAMP}
    event_type: {SPIKE/DECLINE/SUSTAINED_HIGH}
    magnitude: {PERCENTAGE_CHANGE}
    duration: {MINUTES}
    impact_assessment: {LOW/MEDIUM/HIGH}
    response_actions: [{ACTION_1}, {ACTION_2}]
```

## Session Performance Metrics
```yml
session_performance:
  total_return: {PERCENTAGE}
  realized_pnl: {VALUE}
  unrealized_pnl: {VALUE}
  total_trades: {COUNT}
  winning_trades: {COUNT}
  losing_trades: {COUNT}
  win_rate: {PERCENTAGE}
  average_win: {VALUE}
  average_loss: {VALUE}
  profit_factor: {VALUE}
  maximum_drawdown: {PERCENTAGE}
  
strategy_performance:
  trend_following:
    trades: {COUNT}
    win_rate: {PERCENTAGE}
    pnl: {VALUE}
    
  mean_reversion:
    trades: {COUNT}
    win_rate: {PERCENTAGE}
    pnl: {VALUE}
    
  momentum:
    trades: {COUNT}
    win_rate: {PERCENTAGE}
    pnl: {VALUE}
    
  grid_trading:
    trades: {COUNT}
    win_rate: {PERCENTAGE}
    pnl: {VALUE}
```

## Action Items and Next Session Planning
```yml
session_conclusions:
  key_learnings: [{LEARNING_1}, {LEARNING_2}, {LEARNING_3}]
  improvement_areas: [{AREA_1}, {AREA_2}]
  successful_approaches: [{APPROACH_1}, {APPROACH_2}]
  areas_to_avoid: [{AVOID_1}, {AVOID_2}]
  
next_session_preparation:
  watchlist_updates: [{SYMBOL_1}, {SYMBOL_2}]
  strategy_adjustments: [{ADJUSTMENT_1}, {ADJUSTMENT_2}]
  bias_monitoring_focus: [{FOCUS_AREA_1}, {FOCUS_AREA_2}]
  risk_parameter_changes: [{CHANGE_1}, {CHANGE_2}]
  
carryover_items:
  open_positions: [{POSITION_1}, {POSITION_2}]
  pending_signals: [{SIGNAL_1}, {SIGNAL_2}]
  monitoring_alerts: [{ALERT_1}, {ALERT_2}]
  follow_up_analysis: [{ANALYSIS_1}, {ANALYSIS_2}]
```

## Memory Integration Commands
```yml
save_session_memory:
  command: "memory-save SESSION_DATA:{session_id}:{summary}"
  format: "Comprehensive session summary for future reference"
  
recall_session_context:
  command: "memory-recall SESSION:{date_range}"
  purpose: "Retrieve context from previous sessions"
  
update_session_insights:
  command: "memory-save SESSION_INSIGHT:{insight_type}:{details}"
  purpose: "Store learning insights for improvement"
```

## Session Continuity Features
```yml
session_resume:
  resume_context: "Restore previous session state and context"
  position_sync: "Sync current positions with session memory"
  analysis_continuation: "Continue interrupted analysis workflows"
  
cross_session_learning:
  pattern_tracking: "Track pattern performance across sessions"
  bias_improvement: "Improve bias detection based on session outcomes"
  strategy_optimization: "Optimize strategies based on session results"
```
