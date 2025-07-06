# Create Trading Strategy Task

## Purpose
Develop a new trading strategy following CFTAS standards with proper risk management, backtesting, and documentation.

## Prerequisites
- Load crypto-futures-core/core-config.yml
- Access to market data via Binance MCP tools
- Risk management parameters configured

## Task Execution Instructions

### 1. Strategy Conceptualization
- Identify market condition (trend/range/volatile)
- Define strategy type (momentum/mean-reversion/arbitrage)
- Set theoretical foundation

### 2. Technical Implementation
- Define entry/exit criteria using technical indicators
- Set risk management rules (stop-loss, take-profit)
- Configure position sizing methodology

### 3. Backtesting & Validation
- Use historical data for initial testing
- Validate against bias detection framework
- Test across different market conditions

### 4. Documentation & Integration
- Create strategy file in strategies/ directory
- Add to strategy selection workflows
- Update team configurations if needed

## Dependencies
- strategies/strategy-template.md
- utils/bias-detector.md
- checklists/strategy-validation.md
- workflows/signal-to-execution.md

## Output
- Complete strategy document
- Backtesting results
- Integration into CFT system
