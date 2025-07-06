# Technical Indicators Configuration

## Core Technical Indicators

### Trend Indicators
```yaml
trend_indicators:
  moving_averages:
    ema_20:
      period: 20
      type: "exponential"
      usage: "Short-term trend"
      signals: ["price_cross", "slope_change"]
      
    ema_50:
      period: 50
      type: "exponential"
      usage: "Medium-term trend"
      signals: ["price_cross", "ma_cross"]
      
    ema_200:
      period: 200
      type: "exponential"
      usage: "Long-term trend"
      signals: ["price_cross", "trend_filter"]
      
  ichimoku:
    tenkan_sen: 9
    kijun_sen: 26
    senkou_span_b: 52
    usage: "Comprehensive trend analysis"
    signals: ["cloud_breakout", "cross_signals"]
```

### Momentum Indicators
```yaml
momentum_indicators:
  rsi:
    period: 14
    overbought: 70
    oversold: 30
    divergence_detection: true
    usage: "Momentum and reversal signals"
    
  macd:
    fast_period: 12
    slow_period: 26
    signal_period: 9
    usage: "Trend confirmation and momentum"
    signals: ["line_cross", "zero_cross", "divergence"]
    
  stochastic:
    k_period: 14
    d_period: 3
    overbought: 80
    oversold: 20
    usage: "Short-term reversal signals"
```

### Volume Indicators
```yaml
volume_indicators:
  volume_profile:
    usage: "Support/resistance identification"
    calculation: "daily_session"
    key_levels: ["poc", "value_area_high", "value_area_low"]
    
  obv:
    usage: "Volume trend confirmation"
    signals: ["divergence", "trend_confirmation"]
    
  vwap:
    usage: "Institutional price reference"
    signals: ["price_deviation", "trend_confirmation"]
```

### Volatility Indicators
```yaml
volatility_indicators:
  bollinger_bands:
    period: 20
    std_dev: 2
    usage: "Volatility and mean reversion"
    signals: ["band_squeeze", "band_breakout"]
    
  atr:
    period: 14
    usage: "Stop loss and position sizing"
    calculation: "true_range_average"
```

## Indicator Combinations

### Signal Confirmation Matrix
```yaml
signal_combinations:
  bullish_confirmation:
    required_indicators: 3
    combinations:
      - ["ema_cross_up", "rsi_oversold_exit", "volume_increase"]
      - ["macd_cross_up", "price_above_vwap", "bollinger_expansion"]
      
  bearish_confirmation:
    required_indicators: 3
    combinations:
      - ["ema_cross_down", "rsi_overbought_exit", "volume_increase"]
      - ["macd_cross_down", "price_below_vwap", "bollinger_expansion"]
```

### Timeframe Analysis
```yaml
timeframe_hierarchy:
  primary: "4h"
  secondary: "1h"
  confirmation: "15m"
  execution: "5m"
  
  analysis_flow:
    1. "Check 4h trend direction"
    2. "Confirm with 1h momentum"
    3. "Time entry with 15m signals"
    4. "Execute on 5m confirmation"
```

## Indicator Settings by Strategy

### Trend Following
```yaml
trend_following_setup:
  primary: ["ema_20", "ema_50", "ema_200"]
  secondary: ["macd", "atr"]
  filters: ["volume_profile", "market_session"]
```

### Mean Reversion
```yaml
mean_reversion_setup:
  primary: ["bollinger_bands", "rsi", "stochastic"]
  secondary: ["vwap", "volume_profile"]
  filters: ["atr", "market_session"]
```

### Momentum
```yaml
momentum_setup:
  primary: ["macd", "rsi", "ema_20"]
  secondary: ["volume_profile", "obv"]
  filters: ["atr", "bollinger_bands"]
```
