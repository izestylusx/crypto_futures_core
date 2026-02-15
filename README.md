# 🎯 Complete Guide to the Crypto Futures Core System

## 📋 Introduction

Welcome to the **Crypto Futures Core System**! This is an advanced AI agent system for crypto futures trading that works directly in VS Code using GitHub Copilot. The system is specifically designed to help traders — from beginners to professionals — analyze markets, manage risk, and trade more effectively.

### 🌟 Key Features
- **AI Trading Agents** — Specialized agents for market analysis, risk management, and trade execution
- **Real-time Market Data** — Direct connection to the Binance Futures API
- **Risk Management** — Automated, customizable risk management system
- **Technical Analysis** — Comprehensive technical indicators with flexible configuration
- **Workflow Automation** — Automate the trading process from analysis to execution

---

## 📖 Table of Contents

### 🚀 Quick Start
- [1. Requirements & Preparation](#-requirements--preparation)
- [2. Installing Prerequisites](#-installing-prerequisites-windows)
- [3. Installing the Premium Binance MCP Server](#-installing-the-premium-binance-mcp-server)
- [4. How to Use the System](#-how-to-use-the-system)
- [5. Start Your First Trade](#-start-your-first-trade)

### 📚 Full Guide
- **[1. 🛠️ Requirements & Preparation](#-requirements--preparation)**
  - [What You Need](#what-you-need)
  - [Download & Setup Folder](#-download--setup-folder)

- **[2. 🔧 Installing Prerequisites (Windows)](#-installing-prerequisites-windows)**
  - [Install Python](#1-install-python-for-premium-binance-mcp)
  - [Install Node.js](#2-install-nodejs-for-sequential-thinking)
  - [Verify Installation](#3-verify-installation)
  - [Troubleshooting Prerequisites](#-troubleshooting-prerequisites)

- **[3. 🚀 Installing the Premium Binance MCP Server](#-installing-the-premium-binance-mcp-server)**
  - [Step 1: Install Python Packages](#step-1-install-python-packages)
  - [Step 2: Configure Settings.json](#step-2-configure-settingsjson-in-vs-code)
  - [Step 3: Replace API Keys](#step-3-replace-api-keys)
  - [Step 4: Restart MCP Server](#step-4-restart-mcp-server)

- **[4. 🎮 How to Use the System](#-how-to-use-the-system)**
  - [Getting Started with CFT Master](#1-getting-started-with-cft-master)
  - [Basic System Commands](#2-basic-system-commands)
  - [Practical Usage Examples](#3-practical-usage-examples)

- **[5. ⚙️ System Customization](#-system-customization)**
  - [Main Configuration - core-config.yml](#1-main-configuration---core-configyml)
  - [Customization Examples for Various Trader Profiles](#2-customization-examples-for-various-trader-profiles)
  - [Performance & Resource Optimization](#3-performance--resource-optimization)
  - [Flexible Memory System](#4-flexible-memory-system)
  - [How to Apply Customizations](#5-how-to-apply-customizations)
  - [Newly Added Parameters](#6-newly-added-parameters)
  - [Automatic Documentation System](#7-automatic-documentation-system-new)
  - [Creating a Custom Strategy](#8-creating-a-custom-strategy)

- **[6. 🔥 Tips & Tricks](#-tips--tricks)**
  - [Best Practices](#-best-practices)
  - [Recommended Workflows](#-recommended-workflows)
  - [Trading Security](#-trading-security)

- **[7. 🆘 Troubleshooting](#-troubleshooting)**
  - [Common Problems](#-common-problems)

- **[8. 🎓 Start Your First Trade](#-start-your-first-trade)**
  - [Quick Start Guide](#quick-start-guide)
  - [Happy Trading](#-happy-trading)
  - [New CFT Master Features](#-new-cft-master-features)

- **[9. 📞 Support & Community](#-support--community)**

### 🎯 Command Reference
- **Core Commands:** `*help`, `*status`, `*config`, `*mode`, `*exit`
- **Agent Commands:** `*agent market-analyst`, `*agent risk-manager`, `*agent execution-trader`, `*agent performance-tracker`
- **Team Commands:** `*team full-trading`, `*team scalping`, `*team swing-trading`
- **Trading Commands:** `*market-overview`, `*portfolio`, `*risk-check`, `*scan`, `*trade`, `*bracket-order`
- **Analysis Commands:** `*analyze`, `*signal`, `*market-dashboard`, `*market-opportunities`, `*quick-scan`
- **Workflow Commands:** `*workflow-guidance`, `*strategy [name]`, `*signal-to-execution`, `*daily-routine`
- **Risk Commands:** `*bias-check`, `*contrarian-view`, `*reality-check`, `*emergency-mode`
- **Memory Commands:** `*memory`, `*cache-refresh`, `*session-archive`
- **Documentation Commands:** `*generate-docs`, `*auto-docs`, `*session-docs`, `*daily-docs`, `*docs-index`

---

## 🛠️ Requirements & Preparation

### What You Need:
1. **VS Code** (latest version)
2. **GitHub Copilot** (active subscription)
3. **Python** (version 3.8+) — **Will be installed in the next section**
4. **Node.js** (version 18+) — **Will be installed in the next section**
5. **Binance Account** with API Key
6. **Premium Member Key** (for SmartAITrading premium features)

### 📁 Download & Setup Folder
1. Download or clone the `crypto-futures-core` folder
2. Open this folder in VS Code
3. Make sure all `.md` and `.yml` files are readable

---

## 🔧 Installing Prerequisites (Windows)

### ⚠️ Important: Install These Before Proceeding!

Before installing the trading system, make sure your Windows laptop has the following:

#### 1. Install Python (For Premium Binance MCP)

**Easiest Method - Microsoft Store:**
1. Open the **Microsoft Store** on Windows
2. Search for "**Python**"
3. Select "**Python 3.12**" (or the latest version)
4. Click "**Install**"
5. Wait until it finishes

**Manual Method - Python.org:**
1. Go to https://python.org/downloads/
2. Download "**Python 3.12**" for Windows
3. Run the installer
4. ✅ **IMPORTANT: Check "Add Python to PATH"**
5. Click "Install Now"

#### 2. Install Node.js (For Sequential Thinking)

**Easiest Method - Winget:**
1. Open **Command Prompt** or **PowerShell** as Administrator
2. Run: `winget install OpenJS.NodeJS`
3. Wait for the installation to complete

**Manual Method - Node.js Website:**
1. Go to https://nodejs.org/
2. Download the "**LTS version**" (recommended)
3. Run the installer
4. Click "Next" until it finishes (use default settings)

#### 3. Verify Installation

Open **Command Prompt** or **PowerShell** and check:

```bash
# Check Python
python --version
# Expected output: Python 3.12.x

# Check Node.js
node --version
# Expected output: v20.x.x

# Check npm (automatically installed with Node.js)
npm --version
# Expected output: 10.x.x
```

#### 🚨 Troubleshooting Prerequisites

**Problem: "python is not recognized"**
```
• Restart Command Prompt/PowerShell
• Check PATH environment variable
• If the error persists, reinstall Python with "Add to PATH" checked
```

**Problem: "node is not recognized"**
```
• Restart Command Prompt/PowerShell
• Check PATH environment variable
• If the error persists, reinstall Node.js
```

**Problem: "npm is not recognized"**
```
• Node.js was not installed correctly
• Reinstall Node.js from nodejs.org
```

---

## 🚀 Installing the Premium Binance MCP Server

### Step 1: Install Python Packages
Open the terminal in VS Code (`Ctrl + `` ` or View > Terminal`), then run:

```bash
pip install premium_futures_mcp
```

> 💡 **Note:** If you get the error "pip is not recognized", make sure Python is installed correctly (see the Prerequisites section above)

### Step 2: Configure Settings.json in VS Code

1. **Open Settings.json:**
   - Press `Ctrl + Shift + P`
   - Type "Preferences: Open User Settings (JSON)"
   - Select and click it

2. **Add MCP Configuration:**
   Find the `"mcp"` section and add the following configuration inside `"servers"`:

```json
"premium-binance-futures": {
  "command": "python",
  "args": [
    "-m", 
    "premium_futures_mcp.server", 
    "--binance-api-key", "your_binance_api_key",
    "--binance-secret-key", "your_binance_secret_key",
    "--binance-member-key", "your_member_key"
  ]
}
```

3. **Add Sequential Thinking (Recommended):**
   For more structured AI reasoning capabilities:

```json
"sequential-thinking": {
  "command": "npx",
  "args": [
    "-y",
    "@modelcontextprotocol/server-sequential-thinking"
  ],
  "env": {}
}
```

> 💡 **Note:** Sequential thinking requires Node.js. If you get the error "npx is not recognized", make sure Node.js is installed (see the Prerequisites section above)

### Step 3: Replace API Keys
- **your_binance_api_key** → Your Binance API Key
- **your_binance_secret_key** → Your Binance Secret Key  
- **your_member_key** → SmartAITrading Premium Member Key

> 💡 **How to Get a Binance API Key:**
> 1. Log in to your Binance account
> 2. Go to API Management
> 3. Create a new API Key
> 4. Enable "Enable Futures"
> 5. Copy the API Key and Secret Key

### Step 4: Restart MCP Server
1. **Quick Method:** Restart MCP from the sidebar (click the restart button next to the server name)
2. **Or:** Close and reopen VS Code
3. **Or:** Press `Ctrl + Shift + P`, type "Developer: Reload Window"

---

## 🎮 How to Use the System

### 1. Getting Started with CFT Master

1. **Open the file `cft-master.md`** in the `agents/` folder
2. **Open GitHub Copilot Chat** (`Ctrl + Shift + I`)
3. **Make sure the file `cft-master.md` is open** — this will let Copilot understand the system
4. **Start with the command:** `*help`

> 💡 **System Update:** CFT Master is now a unified agent that combines direct trading functions and orchestration. You no longer need a separate orchestrator file!

### 2. Basic System Commands

All commands must start with an **asterisk (*)** in GitHub Copilot Chat:

#### 🔧 Main Commands:
```
*help              → Show all commands and agents
*status            → Check current market status and positions
*config            → Show configuration and risk parameters
*agent [name]      → Switch to a specific specialist agent
*team [name]       → Activate a trading team (full-trading, scalping, swing-trading)
*workflow          → Start a trading workflow
*portfolio         → View positions and balance
*market-overview   → Overview of the current crypto market
*status            → System status and performance
```

#### 🤖 Specialist Agents:
```
*agent market-analyst     → In-depth market analysis
*agent risk-manager       → Risk management
*agent execution-trader   → Trade execution
*agent performance-tracker → Performance tracking
```

#### 👥 Trading Teams:
```
*team full-trading       → Full team for comprehensive trading
*team scalping          → Team for scalping and high-frequency trading
*team swing-trading     → Team for conservative swing trading
```

#### 📊 Workflow & Market Analysis:
```
*workflow-guidance        → Workflow selection guide
*signal-to-execution     → From signal to execution
*daily-routine          → Daily trading routine
*strategy [name]        → Load a trading strategy
*scan                   → Scan the market for 400+ tokens
*market-dashboard       → Comprehensive market dashboard
*market-opportunities   → Trading opportunities with scoring
*quick-scan            → Quick scan for immediate opportunities
```

#### 🛡️ Risk & Bias Management:
```
*bias-check {symbol}     → Detect directional bias
*contrarian-view {symbol} → Contrarian analysis
*reality-check {signal}  → Validate signal vs. historical data
*emergency-mode         → Activate emergency protocol
*safe-mode             → Ultra-conservative mode
```

### 3. Practical Usage Examples

#### 📈 Bitcoin Market Analysis:
```
*agent market-analyst
Analyze current Bitcoin market conditions, provide trading recommendations
```

#### 🎯 Trading Opportunity Analysis:
```
*market-opportunities
Show the best trading opportunities with comprehensive scoring
```

#### 📊 Full Market Dashboard:
```
*market-dashboard
Display market dashboard with all important metrics
```

#### ⚠️ Portfolio Risk Check:
```
*risk-check
Evaluate the risk of my current portfolio
```

#### 🎯 Trade Execution:
```
*agent execution-trader
Create a BTC long bracket order with a 1:2 TP/SL ratio
```

#### 🔍 Quick Market Scan:
```
*quick-scan
Provide a quick analysis for immediate trading opportunities
```

#### 👥 Activate a Trading Team:
```
*team full-trading
Activate the full team for comprehensive trading
```

---

## ⚙️ System Customization

### 1. Main Configuration - core-config.yml

The `core-config.yml` file is the central system configuration that is read by CFT Master and all agents. Edit this file to customize the system to your needs:

```yaml
# Trading Configuration - CAN BE CHANGED TO FIT YOUR NEEDS
trading:
  exchange: "binance_futures"
  default_leverage: 5           # Default leverage (1-20)
  max_leverage: 20             # Maximum allowed leverage
  risk_percentage: 2.0         # Risk percentage per trade (1.0-5.0)
  base_currency: "USDT"        # Base currency
  
  # Trading Modes - NEW!
  paper_trading: false         # Paper trading mode (simulation)
  auto_trading: false          # Automated trading
  max_daily_trades: 20         # Maximum trades per day
  max_open_positions: 10       # Maximum open positions
  
  # Order Management - NEW!
  order_timeout: 300           # Order timeout in seconds
  slippage_tolerance: 0.5      # Slippage tolerance (%)
  partial_fill_threshold: 0.8  # Minimum fill ratio

# Risk Management - ADJUST TO YOUR RISK PROFILE
risk_management:
  max_portfolio_risk: 10.0     # Maximum portfolio risk (5.0-20.0)
  max_position_risk: 5.0       # Maximum risk per position (2.0-10.0)
  stop_loss_percentage: 2.0    # Stop loss percentage (1.0-5.0)
  take_profit_ratio: 2.0       # Take profit ratio (1.5-3.0)
  max_drawdown_threshold: 20.0 # Maximum drawdown threshold (10.0-30.0)
  
  # Advanced Risk Controls - NEW!
  correlation_limit: 0.7       # Maximum correlation between positions
  sector_exposure_limit: 30.0  # Maximum exposure per sector
  volatility_adjustment: true  # Adjust position size based on volatility
  
  # Emergency Controls - NEW!
  emergency_stop_loss: 15.0    # Emergency stop loss (%)
  margin_call_threshold: 80.0  # Margin call threshold
  force_close_threshold: 90.0  # Force close threshold

# Memory System - FLEXIBLE FOR ALL USERS
memory_system:
  # OpenMemory MCP (Optional - requires separate installation)
  use_openmemory: false        # Enable OpenMemory if available
  
  # File-based Memory (Always available)
  use_file_memory: true        # File-based memory
  cache_duration: 300          # Cache duration in seconds (60-600)
  file_documentation: true     # Automatic file documentation
  session_tracking: true       # Session tracking
  
  # Memory Management - NEW!
  max_memory_entries: 1000     # Maximum memory entries
  memory_cleanup_interval: 3600 # Cleanup interval (seconds)
  compress_old_data: true      # Compress old data

# Performance Optimization - NEW!
performance:
  # Market Data
  market_data_interval: 1000   # Market data refresh interval (ms)
  max_symbols_scan: 400        # Maximum symbols for scanning
  concurrent_requests: 10      # Maximum concurrent requests
  
  # Analysis Optimization
  enable_caching: true         # Enable analysis caching
  cache_analysis_duration: 180 # Cache analysis for 3 minutes
  parallel_analysis: true      # Parallel analysis
  
  # Resource Management
  max_cpu_usage: 80           # Maximum CPU usage (%)
  max_memory_usage: 70        # Maximum memory usage (%)

# Market Scanning Configuration - NEW!
market_scanning:
  # Filtering
  min_volume_24h: 1000000     # Minimum 24h volume
  min_price: 0.0001           # Minimum price
  max_price: 100000           # Maximum price
  
  # Scanning Intervals
  quick_scan_interval: 30     # Quick scan interval (seconds)
  deep_scan_interval: 300     # Deep scan interval (seconds)
  
  # Opportunity Detection
  min_opportunity_score: 20   # Minimum opportunity score
  max_opportunities: 50       # Maximum opportunities to track

# Notification System - NEW!
notifications:
  # Alert Settings
  enable_alerts: true         # Enable system alerts
  alert_sound: true           # Alert sound
  desktop_notifications: true # Desktop notifications
  
  # Alert Thresholds
  profit_alert_threshold: 5.0 # Profit alert threshold
  loss_alert_threshold: 3.0   # Loss alert threshold
  volume_spike_threshold: 3.0 # Volume spike threshold
```

### 2. Customization Examples for Various Trader Profiles

#### 🔰 Conservative Profile (Beginner):
```yaml
trading:
  default_leverage: 3
  risk_percentage: 1.0
  paper_trading: true          # Start with simulation
  max_daily_trades: 5          # Limit the number of trades

risk_management:
  max_portfolio_risk: 5.0
  max_position_risk: 2.0
  stop_loss_percentage: 1.5
  max_drawdown_threshold: 10.0
  emergency_stop_loss: 10.0    # Tighter emergency stop loss

performance:
  max_symbols_scan: 50         # Scan limited tokens
  concurrent_requests: 3       # Fewer requests
```

#### ⚡ Aggressive Profile (Experienced):
```yaml
trading:
  default_leverage: 10
  risk_percentage: 3.0
  auto_trading: true           # Automated trading
  max_daily_trades: 50         # More trades
  max_open_positions: 20       # More positions

risk_management:
  max_portfolio_risk: 15.0
  max_position_risk: 8.0
  stop_loss_percentage: 3.0
  max_drawdown_threshold: 25.0
  correlation_limit: 0.8       # Higher correlation tolerance

performance:
  max_symbols_scan: 400        # Scan all tokens
  concurrent_requests: 15      # More requests
  parallel_analysis: true      # Parallel analysis
```

#### 🏃 Scalping Profile (High-Frequency):
```yaml
trading:
  default_leverage: 20
  risk_percentage: 1.5
  max_daily_trades: 100        # Many daily trades
  order_timeout: 60            # Faster order timeout
  slippage_tolerance: 0.1      # Tight slippage tolerance

risk_management:
  max_portfolio_risk: 8.0
  max_position_risk: 3.0
  stop_loss_percentage: 1.0
  take_profit_ratio: 1.5       # Smaller TP/SL ratio

performance:
  market_data_interval: 500    # Faster data refresh
  concurrent_requests: 20      # More requests
  
market_scanning:
  quick_scan_interval: 10      # More frequent scanning
  min_opportunity_score: 15    # Lower opportunity threshold
```

### 3. Performance & Resource Optimization

#### 🚀 High Performance Mode:
```yaml
performance:
  enable_caching: true
  cache_analysis_duration: 300
  parallel_analysis: true
  max_cpu_usage: 90
  max_memory_usage: 80
  
market_scanning:
  max_symbols_scan: 500
  concurrent_requests: 20
  quick_scan_interval: 15
```

#### 💾 Low Resource Mode (Slow Laptop):
```yaml
performance:
  enable_caching: true
  cache_analysis_duration: 600  # Longer cache
  parallel_analysis: false      # Disable parallel processing
  max_cpu_usage: 50
  max_memory_usage: 40
  
market_scanning:
  max_symbols_scan: 100         # Scan fewer tokens
  concurrent_requests: 3        # Fewer requests
  quick_scan_interval: 60       # Less frequent scanning
```

### 4. Flexible Memory System

#### 📚 With OpenMemory MCP (If Available):
```yaml
memory_system:
  use_openmemory: true         # Enable if installed
  use_file_memory: true        # Backup with file memory
  cache_duration: 300
  max_memory_entries: 2000
```

#### 📁 Without OpenMemory MCP (Default):
```yaml
memory_system:
  use_openmemory: false        # Disable
  use_file_memory: true        # Rely on file memory
  cache_duration: 600          # Longer cache
  max_memory_entries: 1000
  compress_old_data: true      # Compress for efficiency
```

### 5. How to Apply Customizations

1. **Edit the `core-config.yml` file** in the root folder
2. **Save the file** (`Ctrl + S`) — changes will be automatically read by the system
3. **Run `*config`** in CFT Master to verify the loaded parameters
4. **Test with `*status`** to ensure the system is running with the new configuration
5. **Monitor performance** with `*market-overview` or `*portfolio`

### 6. Newly Added Parameters

#### 🎯 Trading Enhancements:
- **Paper Trading Mode**: Risk-free simulated trading
- **Auto Trading**: Automated trading based on signals
- **Order Management**: Timeout and slippage control
- **Position Limits**: Control daily trade and position counts

#### 🛡️ Advanced Risk Management:
- **Correlation Limits**: Avoid highly correlated positions
- **Sector Exposure**: Limit exposure per sector
- **Emergency Controls**: Automatic emergency protocols
- **Volatility Adjustment**: Adjust position size based on volatility

#### ⚡ Performance Optimization:
- **Caching System**: Cache analysis for efficiency
- **Parallel Processing**: Parallel analysis for speed
- **Resource Management**: Control CPU and memory usage
- **Concurrent Requests**: Optimize API requests

#### 📡 Market Scanning Enhancements:
- **Advanced Filtering**: Filter by volume, price, and other criteria
- **Flexible Intervals**: Customize scanning intervals
- **Opportunity Detection**: Scoring and opportunity tracking
- **Tier-based Analysis**: Analysis based on token tiers

#### 🔔 Notification System:
- **Multi-channel Alerts**: Desktop, sound, and webhook
- **Customizable Thresholds**: Set thresholds to your needs
- **Real-time Alerts**: Real-time notifications for important events

### 7. Automatic Documentation System (NEW!)

The system uses GitHub Copilot to automatically generate documentation from all your trading activities:

```yaml
# Documentation System - AUTOMATIC DOCUMENTATION GENERATION
documentation:
  # Auto Documentation Settings
  auto_documentation: true     # Enable automatic documentation
  documentation_trigger: "analysis_complete"  # When to create documentation
  documentation_format: "markdown"  # Documentation format (markdown/json/yaml)
  
  # Documentation Types
  generate_analysis_docs: true    # Analysis documentation
  generate_trade_docs: true       # Trade documentation
  generate_session_docs: true     # Session documentation
  generate_strategy_docs: true    # Strategy documentation
  generate_performance_docs: true # Performance documentation
  
  # Documentation Triggers - WHEN IS DOCUMENTATION CREATED
  triggers:
    after_analysis: true          # After market analysis
    after_trade: true             # After trade execution
    after_session: true           # After session ends
    daily_summary: true           # Daily summary
    
  # Documentation Locations - WHERE IS DOCUMENTATION SAVED
  locations:
    analysis_docs: "docs/analysis/"     # Analysis documentation folder
    trade_docs: "docs/trades/"          # Trade documentation folder
    session_docs: "docs/sessions/"      # Session documentation folder
    strategy_docs: "docs/strategies/"   # Strategy documentation folder
    performance_docs: "docs/performance/" # Performance documentation folder
```

#### 📋 Types of Documentation Generated:

1. **📊 Analysis Documentation** — Created after market analysis
   - Market conditions at the time of analysis
   - Technical indicators used
   - Key findings and insights
   - Trading recommendations
   - Bias detection
   - File: `docs/analysis/YYYY-MM-DD_HH-MM_analysis_{symbol}.md`

2. **💰 Trade Documentation** — Created after trade execution
   - Trade setup and reasoning
   - Entry/exit prices and timing
   - Position sizing and risk calculations
   - Market conditions during the trade
   - Trade results and lessons learned
   - File: `docs/trades/YYYY-MM-DD_HH-MM_trade_{symbol}_{side}.md`

3. **📅 Session Documentation** — Created at the end of a session
   - Session overview and objectives
   - Markets analyzed and traded
   - Performance summary
   - Key decisions made
   - Lessons learned
   - File: `docs/sessions/YYYY-MM-DD_session_summary.md`

4. **🎯 Strategy Documentation** — Created after running a strategy
   - Strategy description and parameters
   - Performance metrics
   - Market conditions tested
   - Success/failure rates
   - Optimizations made
   - File: `docs/strategies/YYYY-MM-DD_{strategy_name}_performance.md`

#### 🤖 How Automatic Documentation Works:

1. **Event Detection** — The system detects completion events (analysis finished, trade executed, etc.)
2. **Data Collection** — Gathers data from cache and memory
3. **Template Loading** — Loads the appropriate documentation template
4. **AI Generation** — GitHub Copilot generates the complete documentation
5. **File Creation** — Creates a markdown file with a standardized naming convention
6. **Index Update** — Automatically updates the documentation index

#### 📝 Documentation Commands:

```
# Manual Documentation Generation
*generate-docs analysis     → Generate analysis documentation
*generate-docs trade        → Generate trade documentation
*generate-docs session      → Generate session documentation
*session-docs              → Generate documentation for the current session
*daily-docs                → Generate a daily summary

# Documentation Management
*auto-docs on              → Enable automatic documentation
*auto-docs off             → Disable automatic documentation
*docs-index                → Generate/update the documentation index
*docs-cleanup              → Clean up old documentation
*docs-archive              → Archive old documentation
```

#### 💡 Benefits of the Automatic Documentation System:

- **📈 Continuous Learning** — Comprehensive documentation for review and improvement
- **🔍 Performance Analysis** — Detailed trading performance tracking
- **🛡️ Compliance** — Documentation for regulatory needs
- **🧠 Knowledge Base** — Build a knowledge base from trading experience
- **🔄 Strategy Iteration** — Documentation to optimize strategies
- **📊 Portfolio Review** — Comprehensive portfolio review

> 💡 **Premium Feature**: The system uses GitHub Copilot to generate highly detailed and structured documentation, helping you understand and continuously improve your trading performance!

### 8. Creating a Custom Strategy

1. Open the `strategies/` folder
2. Copy the `strategy-template.md` file
3. Edit it to fit your needs
4. Use it with the command `*strategy [file-name]`

> 💡 **Important Note:** The system is now more flexible and does not depend on OpenMemory MCP. All users can use file-based memory as the default, and those who have OpenMemory MCP can enable it as an enhancement.

---

## 🔥 Tips & Tricks

### 💪 Best Practices:
1. **Always start with `*help`** to see the latest commands
2. **Use `*config`** to view current risk parameters
3. **Use `*risk-check`** before making large trades
4. **Activate `*agent risk-manager`** for automatic monitoring
5. **Use `*scan`** to find trading opportunities across many tokens
6. **Leverage `*market-dashboard`** for a complete market overview
7. **Use `*team [name]`** to activate a trading team matching your strategy
8. **Activate `*bias-check`** to detect bias before trading
9. **Save important analysis** with `*memory`
10. **Use `*quick-scan`** for immediate opportunities

### 🎯 Recommended Workflows:
1. **Morning Routine:**
   ```
   *market-overview
   *portfolio
   *risk-check
   *market-dashboard
   ```

2. **Trading Analysis:**
   ```
   *agent market-analyst
   *market-opportunities
   *scan
   *workflow-guidance
   ```

3. **Trade Preparation:**
   ```
   *bias-check [symbol]
   *contrarian-view [symbol]
   *reality-check [signal]
   ```

4. **Trade Execution:**
   ```
   *agent execution-trader
   *checklist pre-trade-checklist
   *bracket-order [symbol] [side] [size] [tp] [sl]
   ```

5. **Trading Teams (Advanced):**
   ```
   *team full-trading      → For comprehensive trading
   *team scalping         → For high-frequency trading
   *team swing-trading    → For position trading
   ```

### 🚨 Trading Security:
- **Never share your API Keys** with anyone
- **Use IP whitelisting** in Binance API settings
- **Set daily limits** for automated trading
- **Always back up** important configurations

---

## 🆘 Troubleshooting

### ❌ Common Problems:

**1. MCP Server won't connect:**
```
• Check if API keys are correct
• Restart MCP server from the sidebar
• Check internet connection
• Make sure the Python package is installed
```

**2. Commands not working:**
```
• Make sure the cft-master.md file is open
• Use * before the command
• Check command spelling
• Restart GitHub Copilot
• Make sure the MCP server is connected
```

**3. Error during trading:**
```
• Check Binance balance
• Make sure the API key has Futures access
• Check market status (maintenance?)
• Use *status to check system conditions
```

---

## 🎓 Start Your First Trade

### Quick Start Guide:
1. **Open `cft-master.md`**
2. **Start a chat with:** `*help`
3. **Check conditions:** `*market-overview`
4. **View dashboard:** `*market-dashboard`
5. **Select agent:** `*agent market-analyst`
6. **Request analysis:** "Analyze today's trading opportunities"
7. **Check opportunities:** `*market-opportunities`
8. **Validate bias:** `*bias-check [symbol]`
9. **Execute:** `*agent execution-trader`
10. **Activate team:** `*team full-trading` (for comprehensive trading)

### 🎯 Happy Trading!
With the upgraded CFT Master, you have a more powerful and unified AI trading assistant. The system combines direct trading capabilities with intelligent agent orchestration. From market analysis to trade execution, everything can be done easily through a single master agent.

### 🆕 New CFT Master Features:
- **Unified Agent**: One agent for all trading needs
- **Team Management**: Automatic trading team coordination
- **Advanced Market Analysis**: Dashboard and opportunities with scoring
- **Enhanced Risk Management**: Bias detection and reality check
- **Workflow Orchestration**: Smarter workflow guidance
- **Memory & Cache Management**: Improved memory system

> **⚠️ Disclaimer:** Trading crypto futures carries high risk. Always use proper risk management and never trade with money you cannot afford to lose.

---

## 📞 Support & Community

For further questions or to join the premium community, contact **SmartAITrading** to get a premium member key.

**Happy Trading! 🚀**
