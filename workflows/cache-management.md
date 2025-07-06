# Cache Management Workflow

## Purpose
Systematic cache updates to maintain data freshness and session continuity

## Trigger Events
- Session start/end
- After any market analysis
- Every 5 minutes (automatic)
- Before major trading decisions
- After trade outcomes

## Workflow Steps

### Step 1: Initialize Session Cache
```
When: Session starts
Who: CFT Master or CFT Orchestrator
Actions:
1. Create new session memory file or load existing
2. Update session metadata with start time
3. Load previous session summary if exists
4. Initialize market context cache

Prompt: |
  "Initialize trading session cache:
  1. Create or update cache/sessions/session-memory.md:
     - session_id: Generate unique ID
     - start_time: Current timestamp
     - session_type: [Ask user: scalping/swing/position]
     - market_session: [Asian/European/American based on time]
  2. Load market context using get_market_overview
  3. Save initial market state to session memory
  4. Set cache status to ACTIVE"
```

### Step 2: Update Market Data Cache
```
When: Every 5 minutes OR when market data requested
Who: Market Analyst or any agent requesting market data
Actions:
1. Call Binance MCP tools for fresh data
2. Update market-data-cache.md with new information
3. Check for significant market changes
4. Update cache timestamp

Prompt: |
  "Update market data cache:
  1. Call mcp_premium-binan_get_market_overview
  2. Call mcp_premium-binan_get_24hr_ticker for major pairs
  3. Update cache/market-data-cache.md:
     - last_updated: Current timestamp
     - cache_status: ACTIVE
     - major_pairs_snapshot: Update BTCUSDT, ETHUSDT, BNBUSDT data
     - top_movers: Update gainers and losers
  4. If major change detected (>2% move), flag for attention"
```

### Step 3: Update Token Analysis Cache
```
When: After analyzing any specific token
Who: Market Analyst
Actions:
1. Load existing token profile or create new
2. Update with latest analysis results
3. Add new technical levels identified
4. Save analysis to both file cache and OpenMemory

Prompt: |
  "Update token analysis cache for {symbol}:
  1. Open cache/tokens/{symbol}-profile.md (create if not exists)
  2. Update sections:
     - current_market_data: Latest price, volume, changes
     - technical_characteristics: New support/resistance levels
     - analysis_history: Add latest analysis with timestamp
     - strategy_performance: Update if strategy applied
  3. Save analysis to OpenMemory: 'TOKEN_ANALYSIS:{symbol}:{date}:{summary}'
  4. Update session memory with this analysis"
```

### Step 4: Update Session Memory
```
When: After any significant analysis or decision
Who: Any agent performing analysis
Actions:
1. Append analysis to session memory
2. Update session statistics
3. Track bias warnings and confidence levels
4. Link related analyses

Prompt: |
  "Update session memory with analysis:
  1. Open cache/sessions/session-memory.md
  2. Add to analysis_sequence:
     - timestamp: Current time
     - analysis_type: [MARKET_OVERVIEW/SIGNAL_ANALYSIS/RISK_CHECK]
     - symbol: {symbol if applicable}
     - result: Brief summary of findings
     - confidence: Percentage confidence
     - bias_flags: Any bias warnings triggered
     - action_taken: What decision was made
  3. Update session statistics (total analyses, signals generated)
  4. Save file"
```

### Step 5: Save Trade Outcomes
```
When: After trade execution or position update
Who: Execution Trader or Performance Tracker
Actions:
1. Record trade outcome in session memory
2. Update token profile with strategy performance
3. Save outcome to OpenMemory for learning
4. Update performance metrics

Prompt: |
  "Record trade outcome:
  1. Update session memory:
     - Add trade outcome to trades_executed section
     - Update session P&L
  2. Update token profile:
     - Add strategy performance data
     - Update success rate for this pattern
  3. Save to OpenMemory: 'SIGNAL_OUTCOME:{id}:{result}:{pnl}:{lesson}'
  4. Update performance metrics cache"
```

### Step 6: End Session Cache
```
When: Session ends or day closes
Who: CFT Master or CFT Orchestrator
Actions:
1. Finalize session memory
2. Create session summary
3. Archive session data
4. Prepare for next session

Prompt: |
  "Finalize session cache:
  1. Update session memory:
     - end_time: Current timestamp
     - session_summary: Key events and outcomes
     - performance_summary: P&L and key metrics
  2. Save session summary to OpenMemory
  3. Archive session file with date
  4. Prepare clean cache for next session"
```

## Cache Update Command Reference

### For CFT Master/Orchestrator:
```
- cache-init: Initialize session cache
- cache-refresh: Update all cache files
- cache-status: Check cache freshness
- session-start: Start new session with cache
- session-end: Finalize and archive session
```

### For Market Analyst:
```
- update-market-cache: Refresh market data cache
- save-analysis {symbol}: Save analysis to token cache
- load-token-history {symbol}: Load previous analysis
```

### For All Agents:
```
- session-update: Add current analysis to session memory
- memory-save: Save important data to OpenMemory
- cache-check: Verify cache is current
```

## Automatic Triggers

### Time-Based Updates:
```
Every 5 minutes: Update market data cache
Every 1 hour: Refresh token profiles for active symbols
Every session start: Initialize session memory
Every session end: Archive session data
```

### Event-Based Updates:
```
After analysis: Update session memory and token cache
After trade: Update trade outcome and performance
After bias warning: Update bias tracking
After significant market move: Update market cache
```

## Cache Validation

### Data Freshness Check:
```
Prompt: |
  "Validate cache freshness:
  1. Check cache/market-data-cache.md last_updated timestamp
  2. If older than 5 minutes, update with fresh data
  3. Check session memory for current session
  4. Verify all active token profiles are current
  5. Report any stale data found"
```

### Cache Integrity Check:
```
Prompt: |
  "Verify cache integrity:
  1. Ensure all cache files exist and are readable
  2. Validate data format in each cache file
  3. Check for missing token profiles
  4. Verify session memory continuity
  5. Report any issues found"
```

This workflow ensures your cache system is actively maintained and provides real value to your trading operations!
