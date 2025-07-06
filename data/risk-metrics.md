# Risk Metrics Configuration

## Portfolio Risk Metrics

### Core Risk Measurements
```yaml
portfolio_metrics:
  value_at_risk:
    confidence_level: 95
    time_horizon: "1_day"
    calculation_method: "historical_simulation"
    lookback_period: 252
    
  maximum_drawdown:
    threshold: 20.0
    calculation: "peak_to_trough"
    recovery_tracking: true
    
  sharpe_ratio:
    risk_free_rate: 0.02
    calculation_period: "annual"
    minimum_acceptable: 1.5
    
  sortino_ratio:
    target_return: 0.0
    calculation_period: "annual"
    minimum_acceptable: 2.0
```

### Position Risk Metrics
```yaml
position_metrics:
  position_size:
    max_portfolio_percentage: 10.0
    max_correlation_exposure: 25.0
    sector_concentration_limit: 30.0
    
  leverage_metrics:
    max_account_leverage: 20.0
    max_position_leverage: 5.0
    leverage_utilization_target: 60.0
    
  stop_loss_metrics:
    default_stop_percentage: 2.0
    max_stop_percentage: 5.0
    trailing_stop_activation: 1.5
```

### Real-time Risk Monitoring
```yaml
real_time_monitoring:
  position_limits:
    total_exposure_limit: "100% of account"
    single_position_limit: "10% of account"
    correlation_cluster_limit: "25% of account"
    
  margin_requirements:
    maintenance_margin_buffer: 150.0
    liquidation_distance_minimum: 25.0
    funding_rate_threshold: 0.5
    
  volatility_adjustments:
    high_volatility_threshold: 50.0
    position_size_reduction: 50.0
    leverage_reduction: 30.0
```

## Risk-Adjusted Performance

### Return Metrics
```yaml
return_metrics:
  calmar_ratio:
    calculation: "annual_return / max_drawdown"
    minimum_acceptable: 3.0
    
  information_ratio:
    benchmark: "BTC_index"
    tracking_error_target: 5.0
    
  win_rate:
    target_percentage: 55.0
    minimum_acceptable: 45.0
    
  profit_factor:
    calculation: "gross_profit / gross_loss"
    minimum_acceptable: 1.3
```

### Risk-Adjusted Sizing
```yaml
position_sizing:
  kelly_criterion:
    use_fractional_kelly: true
    kelly_fraction: 0.25
    max_kelly_position: 5.0
    
  volatility_targeting:
    target_volatility: 15.0
    lookback_period: 30
    rebalance_frequency: "daily"
    
  correlation_adjustment:
    max_correlation_threshold: 0.7
    position_reduction_factor: 0.5
```

## Stress Testing

### Scenario Analysis
```yaml
stress_scenarios:
  market_crash:
    btc_decline: -50.0
    alt_decline: -70.0
    correlation_increase: 0.9
    
  liquidity_crisis:
    spread_widening: 300.0
    volume_reduction: 80.0
    slippage_increase: 500.0
    
  black_swan:
    extreme_volatility: 200.0
    correlation_breakdown: true
    margin_requirement_increase: 100.0
```

### Backtesting Metrics
```yaml
backtesting:
  minimum_data_period: "2_years"
  out_of_sample_period: "6_months"
  walk_forward_analysis: true
  
  required_metrics:
    - "total_return"
    - "volatility"
    - "max_drawdown"
    - "sharpe_ratio"
    - "win_rate"
    - "profit_factor"
    - "calmar_ratio"
```

## Risk Management Rules

### Dynamic Risk Scaling
```yaml
risk_scaling:
  low_volatility_regime:
    position_size_multiplier: 1.2
    leverage_multiplier: 1.1
    
  normal_volatility_regime:
    position_size_multiplier: 1.0
    leverage_multiplier: 1.0
    
  high_volatility_regime:
    position_size_multiplier: 0.7
    leverage_multiplier: 0.8
```

### Emergency Procedures
```yaml
emergency_protocols:
  margin_call_threshold: 120.0
  forced_liquidation_threshold: 110.0
  
  risk_reduction_triggers:
    daily_loss_limit: 5.0
    weekly_loss_limit: 10.0
    monthly_loss_limit: 15.0
    
  circuit_breakers:
    single_position_loss: 3.0
    portfolio_loss_1h: 2.0
    portfolio_loss_1d: 5.0
```
