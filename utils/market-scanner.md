# Market Scanner Utility

## Purpose
Implement multi-stage filtering for 400+ tokens to prevent context overflow

## Multi-Stage Filtering System
```yml
stage_1_quick_filter:
  purpose: "Reduce 400+ tokens to manageable 20-50 candidates"
  method: "Statistical filters before detailed analysis"
  tools: [get_market_overview, get_top_gainers_losers, get_24hr_ticker]
  
  filtering_criteria:
    volume_filter:
      minimum_24h_volume: "$1M"
      volume_spike_threshold: "150%"
      exclude_low_liquidity: true
      
    price_movement_filter:
      significant_move: ">3%"
      exclude_extreme: "exclude >20% moves"
      focus_range: "3-20% price moves"
      
    market_cap_tiers:
      tier_1_major: ["BTC", "ETH", "BNB", "ADA", "SOL", "XRP", "DOGE", "MATIC", "DOT", "AVAX"]
      tier_2_mid: "Top 11-50 by market cap"
      tier_3_small: "Selected small caps with high volume"

stage_2_technical_filter:
  purpose: "Reduce 20-50 candidates to 5-15 strong signals"
  method: "Technical indicator screening"
  tools: [get_klines]
  
  technical_criteria:
    trend_strength:
      - "ADX > 25 for trending setups"
      - "EMA alignment for trend following"
      - "Momentum confirmation with RSI"
      
    reversal_signals:
      - "RSI divergence patterns"
      - "Support/resistance bounces"
      - "Volume confirmation"
      
    breakout_setups:
      - "Consolidation pattern completion"
      - "Volume accumulation"
      - "Key level approaches"

stage_3_context_analysis:
  purpose: "Deep analysis of final 5-15 candidates"
  method: "Full technical and bias analysis"
  tools: "All MCP tools as needed"
  
  analysis_depth:
    - "Multi-timeframe analysis"
    - "Bias detection and contrarian analysis"
    - "Risk assessment and position sizing"
    - "Entry/exit level identification"
```

## Token Prioritization System
```yml
priority_scoring:
  volume_score: "30% weight"
    calculation: "(current_volume / avg_volume) * 30"
    max_points: 30
    
  price_action_score: "25% weight"
    calculation: "abs(price_change) * significance_factor * 25"
    max_points: 25
    
  technical_score: "25% weight"
    factors: ["trend_strength", "momentum", "pattern_quality"]
    max_points: 25
    
  opportunity_score: "20% weight"
    factors: ["risk_reward_ratio", "probability", "timing"]
    max_points: 20
    
total_score: "Sum of all scores (max 100)"
threshold: "Minimum 60 points for detailed analysis"
```

## Tier-Based Analysis Approach
```yml
tier_1_major_analysis:
  symbols: ["BTCUSDT", "ETHUSDT", "BNBUSDT"]
  frequency: "Continuous monitoring"
  depth: "Full analysis with all indicators"
  bias_detection: "Enhanced bias monitoring"
  
tier_2_mid_cap_analysis:
  symbols: "Top 11-50 by market cap"
  frequency: "Hourly scans"
  depth: "Standard technical analysis"
  bias_detection: "Standard bias checking"
  
tier_3_small_cap_analysis:
  symbols: "High volume small caps only"
  frequency: "4-hour scans"
  depth: "Basic pattern recognition"
  bias_detection: "Basic bias validation"
```

## Context Management Strategies
```yml
memory_optimization:
  token_caching:
    - "Cache 24hr ticker data for all tokens"
    - "Update cache every 5 minutes"
    - "Use bulk_ticker for efficiency"
    
  session_continuity:
    - "Maintain watchlist between sessions"
    - "Save analysis progress"
    - "Resume interrupted scans"
    
  result_prioritization:
    - "Focus on highest scoring opportunities"
    - "Limit detailed analysis to top 10 tokens"
    - "Provide summary for remaining candidates"

context_preservation:
  analysis_chunking:
    - "Process tokens in batches of 5"
    - "Maintain context between batches"
    - "Summarize batch results"
    
  progressive_filtering:
    - "Apply filters progressively"
    - "Maintain filter state"
    - "Allow filter adjustment"
```

## Scanning Workflows for Different Timeframes
```yml
1_minute_scan:
  purpose: "Scalping opportunities"
  filters: ["volume_spike", "momentum_breakout"]
  tokens: "Tier 1 major pairs only"
  analysis_depth: "Basic momentum indicators"
  
5_minute_scan:
  purpose: "Short-term momentum"
  filters: ["significant_moves", "volume_confirmation"]
  tokens: "Tier 1 + high volume Tier 2"
  analysis_depth: "Standard technical analysis"
  
1_hour_scan:
  purpose: "Swing trading setups"
  filters: ["pattern_completion", "trend_alignment"]
  tokens: "All tiers with volume threshold"
  analysis_depth: "Full multi-timeframe analysis"
  
4_hour_scan:
  purpose: "Position trading opportunities"
  filters: ["major_pattern_breaks", "regime_changes"]
  tokens: "All tradeable pairs"
  analysis_depth: "Comprehensive fundamental + technical"
```

## MCP Tools Integration
```yml
bulk_data_tools:
  - get_market_overview: "Initial market state assessment"
  - get_top_gainers_losers: "Quick mover identification"
  - get_24hr_ticker: "Bulk data for all symbols"
  
detailed_analysis_tools:
  - get_klines: "Technical analysis for filtered tokens"
  - get_open_interest: "Positioning analysis for top candidates"
  - get_funding_rate_history: "Sentiment analysis for final selection"
  
memory_integration:
  - mcp_openmemory_add-memory: "Save scan results"
  - mcp_openmemory_search-memories: "Retrieve previous analysis"
```

## Practical Prompt Templates
```yml
quick_opportunity_scan:
  prompt: "Scan for immediate trading opportunities"
  filter_chain: "Volume spike → Price movement → Basic technical"
  output: "Top 5 opportunities with entry levels"
  
swing_setup_scan:
  prompt: "Find swing trading setups for next 1-5 days"
  filter_chain: "Pattern completion → Trend alignment → Full analysis"
  output: "Detailed analysis of top 3 setups"
  
breakout_monitoring:
  prompt: "Monitor for breakout opportunities"
  filter_chain: "Consolidation patterns → Volume buildup → Breakout signals"
  output: "Breakout alerts with execution plans"
  
regime_change_scan:
  prompt: "Identify potential regime changes"
  filter_chain: "Trend exhaustion → Divergences → Regime indicators"
  output: "Regime change analysis with implications"
```

## Integration with Memory System
```yml
session_memory:
  save_format: "SCAN_RESULTS:{timestamp}:{scan_type}:{results_summary}"
  recall_format: "Previous scan results for context continuity"
  
token_memory:
  save_format: "TOKEN_ANALYSIS:{symbol}:{timestamp}:{analysis_summary}"
  recall_format: "Historical analysis for pattern tracking"
  
watchlist_memory:
  save_format: "WATCHLIST:{timestamp}:{tokens}:{reasoning}"
  recall_format: "Active monitoring list with analysis notes"
```

## Efficiency Metrics
- Scan completion time: <2 minutes for full market scan
- Token reduction rate: 400+ → 5-15 (95%+ reduction)
- Analysis accuracy: >80% of flagged opportunities valid
- Context preservation: Maintain analysis continuity across sessions
- Memory efficiency: Optimal use of available context window
