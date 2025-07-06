# Automatic Documentation Generation Workflow

## Purpose
Generate comprehensive documentation automatically using GitHub Copilot for all trading activities, analyses, and system operations.

## Documentation System Overview

### 🤖 How GitHub Copilot Auto-Documentation Works:
1. **Trigger Events**: System detects completion of analysis, trades, or sessions
2. **Content Gathering**: Collects relevant data from cache and memory
3. **Template Loading**: Loads appropriate documentation template
4. **AI Generation**: Uses GitHub Copilot to generate structured documentation
5. **File Creation**: Creates markdown files with standardized naming
6. **Index Update**: Updates documentation index automatically

## Documentation Types & Triggers

### 📊 Analysis Documentation
**When Generated:**
- After completing market analysis (*analyze command)
- After generating trading signals (*signal command)
- After running market scans (*scan, *quick-scan)
- After market dashboard reviews (*market-dashboard)

**Content Includes:**
- Market conditions at time of analysis
- Technical indicators used
- Key findings and insights
- Risk assessment
- Recommended actions
- Confidence levels
- Bias detection results

**File Format:** `docs/analysis/YYYY-MM-DD_HH-MM_analysis_{symbol}.md`

### 💰 Trading Documentation
**When Generated:**
- After executing trades (*trade, *bracket-order)
- After closing positions (*close)
- After modifying orders (*modify-order)
- After emergency actions (*emergency-mode)

**Content Includes:**
- Trade setup and rationale
- Entry/exit prices and timing
- Position size and risk calculation
- Risk management measures taken
- Market conditions during trade
- Trade outcome and lessons learned
- Performance metrics

**File Format:** `docs/trades/YYYY-MM-DD_HH-MM_trade_{symbol}_{side}.md`

### 📅 Session Documentation
**When Generated:**
- At end of trading session (*session-archive)
- Daily summary generation (*daily-docs)
- Weekly/monthly summaries (configurable)

**Content Includes:**
- Session overview and objectives
- Markets analyzed and traded
- Performance summary
- Key decisions made
- Lessons learned
- Areas for improvement
- Next session planning

**File Format:** `docs/sessions/YYYY-MM-DD_session_summary.md`

### 🎯 Strategy Documentation
**When Generated:**
- After running specific strategies (*strategy command)
- After strategy performance reviews
- After strategy modifications

**Content Includes:**
- Strategy description and parameters
- Performance metrics
- Market conditions tested
- Success/failure rates
- Optimizations made
- Backtesting results
- Forward testing results

**File Format:** `docs/strategies/YYYY-MM-DD_{strategy_name}_performance.md`

### 📈 Performance Documentation
**When Generated:**
- Weekly performance reviews
- Monthly performance summaries
- After significant drawdowns or gains
- Quarterly performance reports

**Content Includes:**
- Performance metrics and KPIs
- Risk-adjusted returns
- Drawdown analysis
- Win/loss ratios
- Strategy effectiveness
- Market regime analysis
- Improvement recommendations

**File Format:** `docs/performance/YYYY-MM-DD_performance_report.md`

## Auto-Documentation Workflow Steps

### Step 1: Event Detection
```
Trigger: Analysis completion, trade execution, session end, etc.
Action: System detects completion event
Prompt: |
  "Documentation event detected:
  - Event type: {analysis/trade/session/strategy/performance}
  - Timestamp: {current_time}
  - Related data: {symbol/trade_id/session_id}
  - Trigger auto-documentation workflow"
```

### Step 2: Data Collection
```
Trigger: After event detection
Action: Gather all relevant data from cache and memory
Prompt: |
  "Collect documentation data:
  1. Load relevant cache files (market-data, session-memory, token profiles)
  2. Gather analysis results from memory
  3. Collect performance metrics
  4. Extract key insights and decisions
  5. Identify lessons learned and observations
  6. Prepare data for documentation generation"
```

### Step 3: Template Loading
```
Trigger: After data collection
Action: Load appropriate documentation template
Prompt: |
  "Load documentation template:
  1. Identify documentation type: {analysis/trade/session/strategy/performance}
  2. Load template from docs/templates/{type}-template.md
  3. Prepare template variables for population
  4. Ensure template is current and complete"
```

### Step 4: AI-Generated Documentation
```
Trigger: After template loading
Action: Use GitHub Copilot to generate comprehensive documentation
Prompt: |
  "Generate comprehensive documentation:
  
  Using the following data:
  - Event type: {type}
  - Timestamp: {timestamp}
  - Data: {collected_data}
  - Template: {template_content}
  
  Create detailed documentation that includes:
  1. Executive Summary
  2. Detailed Analysis/Trade Description
  3. Key Metrics and Data
  4. Risk Assessment
  5. Lessons Learned
  6. Recommendations
  7. Next Steps
  
  Format as markdown with proper headers, tables, and code blocks.
  Include all relevant technical and fundamental analysis.
  Ensure documentation is clear, comprehensive, and actionable."
```

### Step 5: File Creation & Organization
```
Trigger: After AI documentation generation
Action: Create and organize documentation files
Prompt: |
  "Create documentation file:
  1. Generate filename: {docs_folder}/{type}/YYYY-MM-DD_HH-MM_{identifier}.md
  2. Create file with generated content
  3. Add metadata headers (date, type, version, etc.)
  4. Save file to appropriate directory
  5. Update file permissions if needed"
```

### Step 6: Index Update
```
Trigger: After file creation
Action: Update documentation index and cross-references
Prompt: |
  "Update documentation index:
  1. Add new document to docs/index.md
  2. Update relevant category indices
  3. Create cross-references to related documents
  4. Update search tags and keywords
  5. Generate document summary for index"
```

## Documentation Commands for CFT Master

### 📝 Manual Documentation Generation:
```
*generate-docs analysis     → Generate analysis documentation
*generate-docs trade        → Generate trade documentation
*generate-docs session      → Generate session documentation
*generate-docs strategy     → Generate strategy documentation
*generate-docs performance  → Generate performance documentation
*docs-summary              → Generate summary of all documentation
*session-docs              → Generate documentation for current session
*daily-docs                → Generate daily summary documentation
```

### ⚙️ Documentation Management:
```
*auto-docs on              → Enable automatic documentation
*auto-docs off             → Disable automatic documentation
*docs-index                → Generate/update documentation index
*docs-cleanup              → Clean up old documentation files
*docs-archive              → Archive old documentation
*docs-template {type}      → Edit documentation template
```

### 🔍 Documentation Review:
```
*docs-review {type}        → Review recent documentation
*docs-search {keyword}     → Search documentation
*docs-stats                → Show documentation statistics
*docs-validate             → Validate documentation completeness
```

## Documentation Templates

### Analysis Documentation Template:
```markdown
# Market Analysis Documentation

## 📊 Analysis Summary
- **Date**: {analysis_date}
- **Time**: {analysis_time}
- **Symbol**: {symbol}
- **Analysis Type**: {analysis_type}
- **Analyst**: {agent_name}

## 🎯 Key Findings
{key_findings}

## 📈 Technical Analysis
{technical_analysis}

## 🛡️ Risk Assessment
{risk_assessment}

## 💡 Recommendations
{recommendations}

## 🔍 Bias Detection
{bias_detection_results}

## 📝 Lessons Learned
{lessons_learned}

## 🔗 Related Documents
{related_documents}
```

### Trade Documentation Template:
```markdown
# Trade Documentation

## 💰 Trade Summary
- **Date**: {trade_date}
- **Time**: {trade_time}
- **Symbol**: {symbol}
- **Side**: {side}
- **Size**: {size}
- **Entry Price**: {entry_price}
- **Exit Price**: {exit_price}
- **P&L**: {pnl}

## 🎯 Trade Setup
{trade_setup}

## 🛡️ Risk Management
{risk_management}

## 📊 Market Conditions
{market_conditions}

## 📈 Performance Analysis
{performance_analysis}

## 📝 Lessons Learned
{lessons_learned}

## 🔄 Next Steps
{next_steps}
```

## Configuration Integration

### Auto-Documentation Settings in core-config.yml:
```yaml
documentation:
  auto_documentation: true
  documentation_trigger: "analysis_complete"
  generate_analysis_docs: true
  generate_trade_docs: true
  generate_session_docs: true
  
  triggers:
    after_analysis: true
    after_trade: true
    after_session: true
    daily_summary: true
```

## Integration with Cache Management

### Cache-Documentation Sync:
```
- Cache updates trigger documentation checks
- Session memory includes documentation status
- Documentation references are cached
- Performance metrics include documentation coverage
```

This system ensures that all your trading activities are comprehensively documented automatically, providing valuable insights for continuous improvement and regulatory compliance!
