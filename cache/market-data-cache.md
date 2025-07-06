# Market Data Cache

## Purpose
Daily market snapshot and data caching for efficient analysis

## Cache Structure
```yml
cache_metadata:
  last_updated: {TIMESTAMP}
  cache_duration: 300  # 5 minutes
  data_sources: ["binance_futures"]
  cache_status: {ACTIVE/EXPIRED/UPDATING}
  
market_overview:
  total_market_cap: {VALUE}
  total_volume_24h: {VALUE}
  active_symbols: {COUNT}
  trending_direction: {BULLISH/BEARISH/NEUTRAL}
  volatility_index: {VALUE}
  fear_greed_index: {VALUE}
```

## Cached Market Data
```yml
major_pairs_snapshot:
  BTCUSDT:
    price: {CURRENT_PRICE}
    change_24h: {PERCENTAGE}
    volume_24h: {VOLUME}
    funding_rate: {RATE}
    open_interest: {VALUE}
    long_short_ratio: {RATIO}
    
  ETHUSDT:
    price: {CURRENT_PRICE}
    change_24h: {PERCENTAGE}
    volume_24h: {VOLUME}
    funding_rate: {RATE}
    open_interest: {VALUE}
    long_short_ratio: {RATIO}
    
  # ... additional major pairs

top_movers:
  gainers:
    - symbol: {SYMBOL}
      change: {PERCENTAGE}
      volume: {VOLUME}
    # ... top 10 gainers
    
  losers:
    - symbol: {SYMBOL}
      change: {PERCENTAGE}
      volume: {VOLUME}
    # ... top 10 losers

volume_leaders:
  - symbol: {SYMBOL}
    volume_24h: {VOLUME}
    volume_change: {PERCENTAGE}
  # ... top 20 by volume
```

## Market Regime Cache
```yml
current_regime:
  regime_type: {TRENDING_BULL/TRENDING_BEAR/RANGING_HIGH_VOL/RANGING_LOW_VOL/CHOPPY}
  confidence: {PERCENTAGE}
  duration: {DAYS}
  strength: {STRONG/MODERATE/WEAK}
  
regime_indicators:
  trend_strength:
    btc_adx: {VALUE}
    eth_adx: {VALUE}
    market_adx: {VALUE}
    
  volatility_measures:
    btc_atr: {VALUE}
    eth_atr: {VALUE}
    vix_equivalent: {VALUE}
    
  momentum_indicators:
    market_rsi: {VALUE}
    fear_greed: {VALUE}
    funding_rates_avg: {VALUE}

regime_change_signals:
  trend_exhaustion: {TRUE/FALSE}
  volatility_spike: {TRUE/FALSE}
  momentum_divergence: {TRUE/FALSE}
  volume_decline: {TRUE/FALSE}
```

## Bias Tracking Cache
```yml
daily_bias_metrics:
  date: {DATE}
  total_signals: {COUNT}
  long_signals: {COUNT}
  short_signals: {COUNT}
  long_percentage: {PERCENTAGE}
  bias_level: {GREEN/YELLOW/ORANGE/RED}
  
signal_confidence_tracking:
  average_confidence: {PERCENTAGE}
  high_confidence_count: {COUNT}  # >85%
  overconfidence_flags: {COUNT}
  confidence_adjustments: {COUNT}
  
portfolio_balance_tracking:
  long_exposure: {PERCENTAGE}
  short_exposure: {PERCENTAGE}
  balance_flags: {COUNT}
  correlation_warnings: {COUNT}
```

## Performance Cache
```yml
daily_performance:
  date: {DATE}
  total_return: {PERCENTAGE}
  realized_pnl: {VALUE}
  unrealized_pnl: {VALUE}
  win_rate: {PERCENTAGE}
  profit_factor: {VALUE}
  max_drawdown: {PERCENTAGE}
  sharpe_ratio: {VALUE}
  
weekly_performance:
  week_ending: {DATE}
  weekly_return: {PERCENTAGE}
  best_trade: {VALUE}
  worst_trade: {VALUE}
  total_trades: {COUNT}
  strategy_performance:
    trend_following: {PERCENTAGE}
    mean_reversion: {PERCENTAGE}
    momentum: {PERCENTAGE}
    grid_trading: {PERCENTAGE}
```

## Cache Update Procedures
```yml
automatic_updates:
  market_data: "Every 5 minutes during active sessions"
  regime_detection: "Every 15 minutes"
  bias_tracking: "After each signal generation"
  performance_metrics: "Every hour"
  
manual_updates:
  full_refresh: "User-initiated cache refresh"
  selective_refresh: "Update specific data categories"
  emergency_refresh: "During market volatility spikes"
  
cache_invalidation:
  time_based: "Expire after specified duration"
  event_based: "Major market events or news"
  error_based: "Data quality issues detected"
  user_initiated: "Manual cache clearing"
```

## Memory Integration
```yml
memory_storage:
  market_snapshots: "MARKET_CACHE:{date}:{summary}"
  regime_changes: "REGIME_CHANGE:{date}:{from}:{to}:{trigger}"
  bias_alerts: "BIAS_ALERT:{date}:{type}:{level}:{action}"
  performance_summaries: "PERFORMANCE:{period}:{metrics_summary}"
  
memory_retrieval:
  recent_patterns: "Retrieve similar market conditions"
  regime_history: "Historical regime performance"
  bias_patterns: "Historical bias detection results"
  performance_context: "Comparative performance analysis"
```

## Cache Optimization
```yml
storage_efficiency:
  data_compression: "Compress historical data"
  selective_retention: "Keep only relevant data"
  rolling_windows: "Maintain limited historical depth"
  memory_limits: "Respect system memory constraints"
  
access_optimization:
  frequent_access: "Cache most-used data in memory"
  lazy_loading: "Load data only when needed"
  background_updates: "Update cache during idle periods"
  priority_queuing: "Prioritize critical data updates"
```

## Cache Monitoring
```yml
health_metrics:
  cache_hit_rate: "Percentage of successful cache retrievals"
  update_frequency: "Rate of cache updates"
  data_freshness: "Age of cached data"
  error_rate: "Cache errors and failures"
  
performance_metrics:
  response_time: "Cache response times"
  memory_usage: "Cache memory consumption"
  update_duration: "Time to update cache"
  throughput: "Cache operations per second"
```

## Error Handling
```yml
cache_failures:
  network_errors: "Handle MCP tool failures gracefully"
  data_corruption: "Detect and handle corrupt data"
  timeout_errors: "Handle slow response times"
  memory_errors: "Handle insufficient memory"
  
fallback_procedures:
  stale_data_usage: "Use expired data with warnings"
  direct_api_calls: "Bypass cache for critical data"
  reduced_functionality: "Limit features during cache issues"
  error_notifications: "Alert user to cache problems"
```
