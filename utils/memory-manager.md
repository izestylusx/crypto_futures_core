# Memory Manager Utility

## Purpose
Integrate OpenMemory MCP tools with file-based caching for comprehensive memory management

## OpenMemory Integration
```yml
memory_functions:
  save_analysis:
    format: "TOKEN_ANALYSIS:{symbol}:{date}:{findings}"
    tool: mcp_openmemory_add-memory
    example: "TOKEN_ANALYSIS:BTCUSDT:2025-07-04:bullish_breakout_confirmed"
    
  recall_analysis:
    query_format: "TOKEN_ANALYSIS:{symbol}"
    tool: mcp_openmemory_search-memories
    example: "Search for BTCUSDT analysis history"
    
  save_market_regime:
    format: "MARKET_REGIME:{date}:{regime}:{confidence}"
    tool: mcp_openmemory_add-memory
    example: "MARKET_REGIME:2025-07-04:trending_bull:85%"
    
  save_bias_detection:
    format: "BIAS_ALERT:{date}:{type}:{level}:{action}"
    tool: mcp_openmemory_add-memory
    example: "BIAS_ALERT:2025-07-04:directional:orange:size_reduction"
    
  save_signal_outcome:
    format: "SIGNAL_OUTCOME:{signal_id}:{result}:{pnl}:{lesson}"
    tool: mcp_openmemory_add-memory
    example: "SIGNAL_OUTCOME:BTC_001:success:+2.5%:volume_confirmation_key"
    
  save_pattern_performance:
    format: "PATTERN_PERF:{pattern}:{symbol}:{outcome}:{conditions}"
    tool: mcp_openmemory_add-memory
    example: "PATTERN_PERF:bull_flag:ETHUSDT:success:high_volume_breakout"
```

## File Cache Management
```yml
file_operations:
  update_market_cache:
    frequency: "Every 5 minutes"
    file: "cache/market-data-cache.md"
    data_sources: ["get_market_overview", "get_24hr_ticker"]
    
  update_session_memory:
    frequency: "Real-time during active trading"
    file: "cache/sessions/session-memory.md"
    triggers: ["signal_generation", "trade_execution", "analysis_completion"]
    
  create_token_profiles:
    frequency: "On-demand and weekly updates"
    location: "cache/tokens/"
    template: "token-template.md"
    auto_creation: "When analyzing new tokens"
    
  update_performance_cache:
    frequency: "End of trading session"
    file: "cache/performance-cache.md"
    data_sources: ["executed_trades", "position_tracking", "pnl_calculation"]
```

## Memory Storage Strategies
```yml
data_categorization:
  immediate_access:
    - "Current session data"
    - "Active position information"
    - "Recent bias detection results"
    - "Today's market regime"
    
  short_term_memory:
    - "Last 7 days of analysis"
    - "Recent signal outcomes"
    - "Weekly performance metrics"
    - "Pattern success rates"
    
  long_term_memory:
    - "Historical market regimes"
    - "Strategy performance over time"
    - "Bias detection improvements"
    - "Learning insights and patterns"
    
  permanent_storage:
    - "Token profile templates"
    - "Strategy configurations"
    - "Risk management rules"
    - "System configuration"
```

## Memory Retrieval Functions
```yml
analysis_context_retrieval:
  get_symbol_history:
    function: "Retrieve all analysis history for specific symbol"
    memory_query: "TOKEN_ANALYSIS:{symbol}"
    file_check: "cache/tokens/{symbol}-profile.md"
    
  get_pattern_success_rate:
    function: "Retrieve historical performance of specific pattern"
    memory_query: "PATTERN_PERF:{pattern}"
    calculation: "Success rate from historical outcomes"
    
  get_bias_history:
    function: "Retrieve bias detection history and effectiveness"
    memory_query: "BIAS_ALERT"
    analysis: "Bias correction effectiveness over time"
    
  get_regime_performance:
    function: "Retrieve strategy performance in specific market regimes"
    memory_query: "MARKET_REGIME:{regime}"
    cross_reference: "SIGNAL_OUTCOME during regime periods"
```

## Context Enhancement Functions
```yml
signal_enhancement:
  add_historical_context:
    process: "Enhance signal with similar historical situations"
    memory_sources: ["TOKEN_ANALYSIS", "PATTERN_PERF", "MARKET_REGIME"]
    output: "Signal with historical context and success probability"
    
  bias_context_integration:
    process: "Include bias detection history in current analysis"
    memory_sources: ["BIAS_ALERT", "SIGNAL_OUTCOME"]
    output: "Bias-aware signal with correction recommendations"
    
  regime_context_addition:
    process: "Add market regime context to analysis"
    memory_sources: ["MARKET_REGIME", "strategy performance"]
    output: "Regime-aware analysis with strategy recommendations"
```

## Learning and Improvement Functions
```yml
pattern_learning:
  update_pattern_success_rates:
    trigger: "After each pattern-based trade completion"
    process: "Update success rate based on outcome"
    storage: "PATTERN_PERF memory + token profile update"
    
  bias_detection_improvement:
    trigger: "After each bias detection validation"
    process: "Improve bias detection parameters based on effectiveness"
    storage: "BIAS_IMPROVEMENT memory + system parameter update"
    
  strategy_optimization:
    trigger: "Weekly performance review"
    process: "Optimize strategy parameters based on outcomes"
    storage: "STRATEGY_OPT memory + strategy configuration update"
```

## Memory Synchronization
```yml
sync_operations:
  memory_to_file_sync:
    frequency: "End of each trading session"
    process: "Update file cache with memory insights"
    validation: "Ensure consistency between memory and files"
    
  file_to_memory_sync:
    frequency: "Session startup"
    process: "Load file cache into memory for quick access"
    optimization: "Load only relevant recent data"
    
  cross_system_validation:
    frequency: "Daily"
    process: "Validate consistency across all memory systems"
    error_handling: "Resolve conflicts and inconsistencies"
```

## Memory Performance Optimization
```yml
query_optimization:
  index_creation:
    - "Index by symbol for quick token lookups"
    - "Index by date for temporal queries"
    - "Index by pattern type for pattern analysis"
    - "Index by bias type for bias analysis"
    
  caching_strategy:
    - "Cache frequently accessed patterns"
    - "Cache current session context"
    - "Cache active token profiles"
    - "Cache recent bias detection results"
    
  lazy_loading:
    - "Load detailed history only when needed"
    - "Load pattern details on-demand"
    - "Load full token profiles when analyzing"
    - "Load historical context progressively"
```

## Memory Cleanup and Maintenance
```yml
cleanup_procedures:
  regular_cleanup:
    frequency: "Weekly"
    actions:
      - "Remove outdated session data"
      - "Compress old analysis results"
      - "Archive completed trade data"
      - "Clean up duplicate entries"
      
  performance_maintenance:
    frequency: "Monthly"
    actions:
      - "Optimize memory indexes"
      - "Defragment storage"
      - "Validate data integrity"
      - "Update retrieval algorithms"
      
  capacity_management:
    triggers: ["Memory usage >80%", "File size limits reached"]
    actions:
      - "Archive old data"
      - "Compress historical records"
      - "Remove low-value data"
      - "Optimize storage formats"
```

## Error Handling and Recovery
```yml
error_scenarios:
  memory_tool_failures:
    detection: "MCP tool error responses"
    fallback: "Use file cache for critical operations"
    recovery: "Retry with exponential backoff"
    
  file_corruption:
    detection: "File parsing errors or inconsistencies"
    fallback: "Restore from memory if possible"
    recovery: "Regenerate from memory data"
    
  sync_conflicts:
    detection: "Inconsistencies between memory and files"
    resolution: "Prioritize most recent data"
    validation: "Cross-check with multiple sources"
    
  capacity_limits:
    detection: "Storage or memory limits reached"
    action: "Trigger cleanup procedures"
    prevention: "Proactive capacity monitoring"
```

## Integration APIs
```yml
agent_integration:
  cft_master_integration:
    - "Provide context for all analysis commands"
    - "Store all command results for future reference"
    - "Enable session continuity and learning"
    
  market_analyst_integration:
    - "Enhance analysis with historical context"
    - "Provide pattern success rate data"
    - "Store analysis results for learning"
    
  bias_detector_integration:
    - "Store bias detection results"
    - "Provide bias history for improvement"
    - "Track bias correction effectiveness"
    
  risk_manager_integration:
    - "Store risk assessment results"
    - "Provide risk history context"
    - "Track risk management effectiveness"
```

## Memory System Metrics
```yml
performance_metrics:
  response_time: "Average memory retrieval time"
  hit_rate: "Percentage of successful memory retrievals"
  storage_efficiency: "Storage space utilization"
  sync_success_rate: "Memory-file synchronization success"
  
quality_metrics:
  data_accuracy: "Accuracy of stored vs actual data"
  context_relevance: "Relevance of retrieved context"
  learning_effectiveness: "Improvement in decision quality over time"
  bias_detection_improvement: "Improvement in bias detection accuracy"
```

## ⚠️ CRITICAL SAFETY WARNING

**🚨 NEVER USE CACHED DATA FOR TRADING DECISIONS**
- Cache is for LEARNING and SESSION CONTINUITY only
- ALL trading decisions must use FRESH real-time MCP data
- Crypto markets move every second - cached prices are DANGEROUS
- Always call fresh MCP tools before any trade execution

## Cache Update Commands

### Session Learning Cache (SAFE)
```yaml
update_session_learning_cache:
  purpose: "Record analysis process and outcomes for learning"
  trigger: "After analysis completion (NOT during live trading)"
  safety_rule: "Contains NO real-time price data"
  process:
    1. "Save analysis reasoning and methodology"
    2. "Record strategy used and confidence level"
    3. "Note market conditions at time of analysis"
    4. "Track decision process for future learning"
    
  example_prompt: |
    "Save analysis learning to session cache:
    1. Record: 'BTCUSDT analysis at 14:30 - identified bull flag pattern'
    2. Method: 'Used RSI + volume analysis'
    3. Confidence: '78% based on historical similar setups'
    4. Outcome: 'Recommended long entry - monitoring for results'
    ⚠️ NO PRICE DATA cached - analysis process only"
```

### Strategy Performance Cache (SAFE)
```yaml
update_strategy_performance_cache:
  purpose: "Track strategy success rates over time"
  trigger: "After trade outcomes are known"
  safety_rule: "Historical performance only, no current prices"
  process:
    1. "Update strategy win/loss statistics"
    2. "Record which market conditions worked best"
    3. "Note timing and session patterns"
    4. "Calculate performance metrics"
    
  example_prompt: |
    "Update strategy performance cache:
    1. Strategy: 'Trend following' Result: 'Success (+2.3%)'
    2. Conditions: 'High volume breakout during US session'
    3. Update stats: 'Now 78% win rate over 25 trades'
    ⚠️ NO current prices - performance tracking only"
```

### Token Profile Updates
```yaml
update_token_profile_command:
  trigger: "After analyzing any specific token"
  process:
    1. "Load existing token profile or create from template"
    2. "Update technical characteristics based on new analysis"
    3. "Add new support/resistance levels if identified"
    4. "Update strategy performance data"
    
  example_prompt: |
    "Update BTCUSDT token profile:
    1. Open cache/tokens/BTCUSDT-profile.md (or create from token-template.md)
    2. Update current_market_data section with latest price data
    3. Add any new support/resistance levels identified
    4. Update technical_characteristics based on today's analysis
    5. Add this analysis to analysis_history section
    6. Save updated profile"
```
