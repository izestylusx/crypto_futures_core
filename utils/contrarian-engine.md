# Contrarian Engine Utility

## Purpose
Generate opposing viewpoints for any trading signal to combat confirmation bias

## Contrarian Analysis Functions
```yml
contrarian_functions:
  opposing_signal_analysis:
    input: "original_signal, symbol, timeframe"
    output: "contrarian_viewpoint, supporting_evidence"
    process:
      - "Generate opposite direction analysis"
      - "Find supporting technical indicators"
      - "Identify potential catalysts for opposite move"
      - "Assess probability of contrarian scenario"
      
  crowd_sentiment_analysis:
    input: "symbol"
    output: "crowd_positioning, contrarian_opportunity"
    tools: "get_top_long_short_account_ratio"
    process:
      - "Analyze retail trader positioning"
      - "Identify crowded trades"
      - "Assess contrarian potential"
      - "Generate fade-the-crowd signals"
      
  devil_advocate_analysis:
    input: "trade_thesis, confidence_level"
    output: "opposing_arguments, risk_scenarios"
    process:
      - "Challenge all assumptions"
      - "Identify potential failure modes"
      - "Generate worst-case scenarios"
      - "Assess thesis weak points"
      
  market_regime_contrarian:
    input: "current_regime, proposed_strategy"
    output: "regime_change_risk, contrarian_strategy"
    process:
      - "Assess regime stability"
      - "Identify regime change catalysts"
      - "Generate opposite regime strategy"
      - "Calculate regime change probability"
```

## Contrarian Triggers
```yml
mandatory_triggers:
  high_confidence: ">75% confidence signals"
  directional_bias: ">70% same direction signals"
  crowded_trades: "Long/short ratio >80%"
  momentum_extremes: "RSI >80 or <20"
  extended_trends: "Trend duration >30 days"
  
optional_triggers:
  moderate_confidence: "50-75% confidence signals"
  news_driven: "News-based signals"
  breakout_signals: "Technical breakout patterns"
  volatility_spikes: "Unusual volatility events"
```

## Contrarian Analysis Templates
```yml
opposing_technical_analysis:
  trend_reversal:
    - "Hidden divergences in momentum indicators"
    - "Exhaustion patterns in trend structure"
    - "Volume declining in trend direction"
    - "Support/resistance level approaches"
    
  mean_reversion_cases:
    - "Overbought/oversold conditions"
    - "Statistical regression to mean"
    - "Bollinger Band extremes"
    - "RSI divergence patterns"
    
  fundamental_contrarian:
    - "Overvaluation metrics"
    - "Sentiment extremes"
    - "Positioning crowding"
    - "Risk-off scenarios"
```

## Crowd Analysis Integration
```yml
sentiment_indicators:
  long_short_ratio:
    tool: "get_top_long_short_account_ratio"
    contrarian_signals:
      - ">80% long: Potential short opportunity"
      - ">80% short: Potential long opportunity"
      - "Extreme positioning: Fade the crowd"
      
  volume_analysis:
    tool: "get_taker_buy_sell_volume"
    contrarian_signals:
      - "Buy volume exhaustion in uptrend"
      - "Sell volume exhaustion in downtrend"
      - "Volume divergence with price"
      
  open_interest:
    tool: "get_open_interest"
    contrarian_signals:
      - "Open interest decline in trend"
      - "Positioning extreme levels"
      - "Liquidation cascade potential"
```

## Contrarian Scenario Generation
```yml
scenario_types:
  technical_reversal:
    probability: "Calculate based on historical patterns"
    catalysts: "Technical breakdown/breakout levels"
    timeline: "Short to medium term (days to weeks)"
    
  fundamental_shift:
    probability: "Based on macro and sentiment factors"
    catalysts: "News, events, regime changes"
    timeline: "Medium to long term (weeks to months)"
    
  liquidity_driven:
    probability: "Based on positioning and leverage"
    catalysts: "Margin calls, liquidations, forced selling"
    timeline: "Immediate to short term (hours to days)"
    
  black_swan:
    probability: "Low but high impact"
    catalysts: "Unexpected events, system failures"
    timeline: "Immediate impact"
```

## Integration with MCP Tools
```yml
primary_tools:
  - get_top_long_short_account_ratio: "Crowd positioning analysis"
  - get_taker_buy_sell_volume: "Volume flow analysis"
  - get_open_interest: "Positioning extreme detection"
  
secondary_tools:
  - get_funding_rate_history: "Funding rate extreme analysis"
  - get_klines: "Technical contrarian pattern detection"
  - get_market_overview: "Market-wide sentiment assessment"
```

## Contrarian Output Format
```yml
contrarian_report:
  opposing_thesis:
    direction: "Opposite to original signal"
    probability: "Assessed likelihood (max 85%)"
    timeframe: "Expected timeline for contrarian scenario"
    
  supporting_evidence:
    technical: "Technical indicators supporting contrarian view"
    fundamental: "Fundamental factors supporting contrarian view"
    sentiment: "Sentiment factors supporting contrarian view"
    
  risk_assessment:
    original_signal_risks: "Risks to original signal"
    contrarian_signal_risks: "Risks to contrarian signal"
    probability_weighted: "Combined risk assessment"
    
  recommendations:
    position_sizing: "Adjusted position size based on contrarian analysis"
    hedge_suggestions: "Potential hedging strategies"
    monitoring_points: "Key levels to monitor for contrarian confirmation"
```

## Mandatory Integration Points
- Market Analyst: Include contrarian analysis for >75% confidence signals
- CFT Master: Activate contrarian engine for bias-check commands
- Risk Manager: Include contrarian scenarios in risk assessment
- Strategy deployment: Validate strategies against contrarian scenarios
