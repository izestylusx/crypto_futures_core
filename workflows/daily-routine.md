# Daily Routine Workflow

## Time-Based Daily Trading Routine

### Morning Market Preparation (08:00-09:00 UTC)
1. Market overview and overnight analysis
2. Review open positions and pending orders
3. Check global market sentiment and news
4. Update watchlist and scan for opportunities
5. Plan trading strategy for the session

### Mid-Session Analysis (12:00-13:00 UTC)
1. Review morning trading performance
2. Reassess market conditions and regime
3. Update bias detection analysis
4. Adjust positions if needed
5. Scan for emerging opportunities

### Evening Review (20:00-21:00 UTC)
1. Daily performance summary
2. Close or adjust positions as needed
3. Plan for next trading session
4. Update memory system with analysis
5. Review bias detection effectiveness

## Detailed Daily Routine Steps

### Morning Preparation Phase
```yml
step_1_market_overview:
  actions:
    - Call get_market_overview for overall market state
    - Check get_top_gainers_losers for overnight movers
    - Review get_24hr_ticker for volume patterns
    - Assess market regime using regime-classifier
  
  bias_monitoring:
    - Review previous day's signal distribution
    - Check portfolio balance (long vs short)
    - Assess any overnight bias accumulation
    - Reset daily bias counters

step_2_position_review:
  actions:
    - Check all open positions via get_position_info
    - Review unrealized PnL and performance
    - Assess stop-loss and take-profit levels
    - Check margin utilization via get_balance
  
  risk_assessment:
    - Validate positions against risk limits
    - Check correlation between positions
    - Assess total portfolio exposure
    - Plan any needed position adjustments

step_3_news_and_sentiment:
  actions:
    - Review major crypto news and events
    - Check funding rates via get_funding_rate_history
    - Assess crowd positioning via get_top_long_short_account_ratio
    - Evaluate global market sentiment
  
  bias_implications:
    - Identify potential news-driven bias
    - Assess sentiment extreme implications
    - Plan contrarian analysis if needed
    - Update regime assessment

step_4_opportunity_scanning:
  actions:
    - Run tier-1 major pair analysis
    - Scan for breakout setups
    - Identify mean reversion opportunities
    - Check grid trading range conditions
  
  filtering_process:
    - Apply volume and movement filters
    - Run technical screening
    - Include bias detection in all signals
    - Prioritize highest probability setups

step_5_session_planning:
  actions:
    - Set trading priorities for the session
    - Plan position sizing allocations
    - Define key levels to monitor
    - Set bias monitoring parameters
```

### Mid-Session Review Phase
```yml
step_1_performance_check:
  actions:
    - Review session PnL and performance
    - Check executed trades vs plan
    - Assess any slippage or execution issues
    - Validate stop-loss and take-profit hits
  
  bias_assessment:
    - Check session signal distribution
    - Assess any emerging directional bias
    - Review confidence levels in executed trades
    - Plan bias correction if needed

step_2_market_condition_update:
  actions:
    - Reassess current market regime
    - Check for any regime change signals
    - Update volatility and volume analysis
    - Assess crowd positioning changes
  
  strategy_adjustment:
    - Validate current strategies vs regime
    - Adjust strategy allocation if needed
    - Update risk parameters for conditions
    - Plan strategy switches if required

step_3_position_management:
  actions:
    - Review all position performance
    - Assess any needed stop-loss adjustments
    - Consider profit-taking opportunities
    - Plan position scaling or hedging
  
  risk_management:
    - Check overall portfolio risk
    - Validate margin levels and utilization
    - Assess any correlation changes
    - Plan risk reduction if needed

step_4_opportunity_update:
  actions:
    - Scan for new trading opportunities
    - Update existing signal analysis
    - Check for changed market conditions
    - Assess any time-sensitive setups
  
  bias_validation:
    - Apply bias detection to new signals
    - Include contrarian analysis for high-confidence setups
    - Validate against current regime
    - Check portfolio balance impact
```

### Evening Review Phase
```yml
step_1_daily_summary:
  actions:
    - Generate comprehensive performance report
    - Calculate daily PnL and metrics
    - Assess trading plan execution
    - Review any major market movements
  
  performance_metrics:
    - Daily return percentage
    - Win rate and profit factor
    - Maximum intraday drawdown
    - Sharpe ratio calculation
    - Risk-adjusted returns

step_2_position_closure_decisions:
  actions:
    - Review overnight holding suitability
    - Close any day-trading positions
    - Adjust stop-losses for overnight risk
    - Plan any hedge requirements
  
  risk_considerations:
    - Overnight gap risk assessment
    - Funding rate implications
    - Weekend holding decisions
    - Margin requirement validation

step_3_next_session_planning:
  actions:
    - Plan for next trading session
    - Update watchlist based on analysis
    - Set alerts for key levels
    - Prepare strategy adjustments
  
  bias_preparation:
    - Review daily bias accumulation
    - Plan contrarian analysis needs
    - Set bias monitoring parameters
    - Update bias detection thresholds

step_4_memory_system_update:
  actions:
    - Save daily analysis to memory system
    - Update token analysis documentation
    - Store session trading notes
    - Record bias detection results
  
  learning_improvement:
    - Review signal accuracy and outcomes
    - Update pattern success rates
    - Improve bias detection parameters
    - Enhance contrarian analysis effectiveness
```

## Session-Specific Routines

### Asian Session Focus (00:00-08:00 UTC)
```yml
characteristics:
  - Lower volume, range-bound movement
  - Asian crypto pairs more active
  - Overnight gap analysis important
  
trading_approach:
  - Focus on range trading strategies
  - Monitor for breakout setups
  - Assess overnight sentiment changes
  - Plan for European session open
  
bias_considerations:
  - Lower signal frequency expected
  - Range bias possible in low volume
  - Monitor for weekend sentiment effects
```

### European Session Focus (08:00-16:00 UTC)
```yml
characteristics:
  - Moderate volume and volatility
  - European market open influence
  - Mid-session trend development
  
trading_approach:
  - Trend following opportunities
  - Break of Asian range levels
  - Volume confirmation important
  - Prepare for US session
  
bias_considerations:
  - Moderate signal generation expected
  - Trend bias possible with breakouts
  - Monitor European market sentiment
```

### American Session Focus (16:00-24:00 UTC)
```yml
characteristics:
  - Highest volume and volatility
  - Major price movements likely
  - News and event impact
  
trading_approach:
  - High-probability momentum trades
  - Breakout and trend following
  - News-driven opportunities
  - Daily closing considerations
  
bias_considerations:
  - Highest signal frequency expected
  - Momentum bias risk elevated
  - News-driven bias possible
  - End-of-day position review
```

## Memory System Integration
```yml
daily_routine_memory:
  morning_analysis: "MORNING_ROUTINE:{date}:{market_overview}:{plan}"
  session_review: "SESSION_REVIEW:{date}:{performance}:{adjustments}"
  evening_summary: "EVENING_REVIEW:{date}:{summary}:{next_plan}"
  
bias_tracking_memory:
  daily_bias: "DAILY_BIAS:{date}:{long_pct}:{short_pct}:{actions}"
  signal_distribution: "SIGNAL_DIST:{date}:{count_by_direction}:{avg_confidence}"
  bias_corrections: "BIAS_CORRECT:{date}:{corrections_applied}:{effectiveness}"
  
performance_memory:
  daily_metrics: "DAILY_PERF:{date}:{return}:{sharpe}:{drawdown}:{trades}"
  weekly_summary: "WEEKLY_PERF:{week}:{total_return}:{win_rate}:{best_strategy}"
  monthly_review: "MONTHLY_PERF:{month}:{performance_summary}:{improvements}"
```

## Automation and Alerts
```yml
automated_checks:
  position_monitoring: "Every 15 minutes during active sessions"
  bias_detection: "After each signal generation"
  risk_validation: "Hourly during active trading"
  performance_tracking: "Real-time PnL updates"
  
alert_conditions:
  risk_limit_approach: "Portfolio risk >8% of maximum"
  bias_threshold_breach: "Directional bias >60%"
  drawdown_warning: "Daily drawdown >5%"
  margin_utilization: "Margin usage >80%"
  performance_deviation: "Significant underperformance vs plan"
```

## Success Metrics
- Routine completion rate: >95%
- Daily plan execution: >80% adherence
- Bias detection effectiveness: Catch >85% of bias situations
- Risk management compliance: 100% within limits
- Performance consistency: Reduce daily variance by >30%
