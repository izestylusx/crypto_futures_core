# Bias Detector Utility

## Purpose
Monitor and detect directional bias in trading decisions

## Detection Metrics (EXACT CALCULATIONS)
```yml
bias_metrics:
  directional_bias:
    calculation: "long_signals / total_signals * 100"
    warning_threshold: 70
    critical_threshold: 80
  
  confidence_tracking:
    average_confidence: "sum(confidence) / count(signals)"
    overconfidence_threshold: 85
    overconfidence_count: "signals > 90% confidence"
    
  position_balance:
    long_exposure: "sum(long_positions) / total_exposure * 100"
    short_exposure: "sum(short_positions) / total_exposure * 100"
    balance_threshold: 70  # Warning if >70% one direction
    
  temporal_bias:
    daily_bias: "Track bias within 24h periods"
    session_bias: "Track bias by trading session"
    regime_bias: "Track bias by market regime"
```

## Bias Detection Functions
```yml
detection_functions:
  signal_bias_check:
    input: "signal_direction, confidence_level"
    output: "bias_warning, bias_percentage"
    process: 
      - "Count signals by direction in last 24h"
      - "Calculate directional percentage"
      - "Flag if >70% one direction"
      
  confidence_bias_check:
    input: "confidence_level"
    output: "overconfidence_warning"
    process:
      - "Track average confidence levels"
      - "Flag signals >85% confidence"
      - "Require justification for >90% confidence"
      
  portfolio_bias_check:
    input: "current_positions"
    output: "portfolio_balance_warning"
    process:
      - "Calculate long vs short exposure"
      - "Flag if >70% one direction"
      - "Suggest rebalancing actions"
      
  regime_bias_check:
    input: "market_regime, signal_direction"
    output: "regime_alignment_warning"
    process:
      - "Check if signal aligns with regime"
      - "Flag contrarian signals appropriately"
      - "Validate regime-strategy fit"
```

## Warning System
```yml
warning_levels:
  green: "Bias levels normal (<50%)"
  yellow: "Moderate bias detected (50-70%)"
  orange: "High bias warning (70-80%)"
  red: "Critical bias alert (>80%)"
  
warning_actions:
  yellow_level:
    - "Include contrarian analysis in next signal"
    - "Reduce position sizes by 25%"
    - "Increase scrutiny of same-direction signals"
    
  orange_level:
    - "Mandatory contrarian analysis for all signals"
    - "Reduce position sizes by 50%"
    - "Require 3+ confirming indicators"
    - "Include regime validation"
    
  red_level:
    - "Suspend same-direction signals"
    - "Force opposite-direction analysis"
    - "Reduce maximum confidence to 60%"
    - "Emergency portfolio review"
```

## MCP Integration
```yml
memory_tools:
  - mcp_openmemory_search-memories: "Retrieve bias history"
  - mcp_openmemory_add-memory: "Store bias detection results"
  
memory_storage_format:
  bias_detection: "BIAS_ALERT:{date}:{type}:{percentage}:{action_taken}"
  signal_tracking: "SIGNAL_BIAS:{symbol}:{direction}:{confidence}:{date}"
  portfolio_balance: "PORTFOLIO_BIAS:{date}:{long_pct}:{short_pct}:{warning_level}"
```

## Bias Correction Protocols
```yml
correction_actions:
  signal_level:
    - "Generate opposite direction analysis"
    - "Reduce signal confidence by bias percentage"
    - "Require additional confirmation"
    - "Include uncertainty statements"
    
  portfolio_level:
    - "Suggest position rebalancing"
    - "Recommend opposite direction opportunities"
    - "Adjust risk allocation"
    - "Implement correlation limits"
    
  system_level:
    - "Activate contrarian engine"
    - "Increase reality validation requirements"
    - "Reduce maximum leverage"
    - "Enable emergency protocols"
```

## Integration with Trading Agents
- CFT Master: Include bias check in all analysis commands
- Market Analyst: Mandatory bias detection before signal generation
- Risk Manager: Include bias assessment in risk calculations
- Execution Trader: Pre-execution bias validation
- Performance Tracker: Track bias-related performance impact
