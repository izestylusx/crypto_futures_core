# Bias Detection Checklist

## Directional Bias Assessment
- [ ] **Recent Signal Count**: Count signals by direction in last 24 hours
- [ ] **Long Signal Percentage**: Calculate percentage of long signals
- [ ] **Short Signal Percentage**: Calculate percentage of short signals
- [ ] **Bias Threshold Check**: Flag if >70% one direction
- [ ] **Bias Trend Analysis**: Check if bias is increasing or stable
- [ ] **Session Bias Check**: Analyze bias by trading session

## Confidence Bias Assessment
- [ ] **Current Signal Confidence**: Assess confidence level of current signal
- [ ] **Recent Average Confidence**: Calculate average confidence of recent signals
- [ ] **Overconfidence Detection**: Flag if current signal >85% confidence
- [ ] **Confidence Pattern**: Check for pattern of increasing confidence
- [ ] **Confidence vs Outcome**: Review if recent high-confidence trades succeeded
- [ ] **Uncertainty Acknowledgment**: Include uncertainty factors in analysis

## Portfolio Bias Assessment
- [ ] **Current Long Exposure**: Calculate percentage of portfolio in long positions
- [ ] **Current Short Exposure**: Calculate percentage of portfolio in short positions
- [ ] **Position Balance Check**: Flag if >70% exposure one direction
- [ ] **Position Correlation**: Check correlation between long positions
- [ ] **Sector Concentration**: Assess concentration in similar assets
- [ ] **Time-Based Exposure**: Check exposure by position duration

## Market Regime Bias Assessment
- [ ] **Current Regime Identification**: Properly identify current market regime
- [ ] **Regime Stability**: Assess how stable the current regime is
- [ ] **Strategy Alignment**: Verify strategy aligns with regime
- [ ] **Regime Change Signals**: Look for signs of regime transition
- [ ] **Historical Regime Performance**: Check strategy performance in similar regimes
- [ ] **Regime Bias Risk**: Assess risk of regime misalignment

## Crowd Sentiment Bias Assessment
- [ ] **Long/Short Ratio Check**: Use get_top_long_short_account_ratio
- [ ] **Positioning Extremes**: Identify if crowd positioning is extreme
- [ ] **Contrarian Opportunity**: Assess if crowd position creates contrarian setup
- [ ] **Volume Flow Analysis**: Use get_taker_buy_sell_volume for sentiment
- [ ] **Funding Rate Extremes**: Check funding rates for sentiment extremes
- [ ] **Open Interest Trends**: Analyze open interest for positioning clues

## Pattern Recognition Bias Assessment
- [ ] **Pattern Validity**: Verify pattern exists and is statistically significant
- [ ] **Cherry-Picking Check**: Ensure not selecting only favorable examples
- [ ] **Confirmation Bias**: Look for contradictory evidence
- [ ] **Pattern Success Rate**: Check historical success rate of pattern
- [ ] **Sample Size Adequacy**: Ensure sufficient historical occurrences
- [ ] **Out-of-Sample Validation**: Test pattern on different time periods

## Temporal Bias Assessment
- [ ] **Recency Bias Check**: Ensure not over-weighting recent events
- [ ] **Seasonality Awareness**: Consider seasonal or cyclical factors
- [ ] **Time-of-Day Bias**: Check for session-specific biases
- [ ] **Weekend Effect**: Consider weekend or holiday effects
- [ ] **News Cycle Bias**: Assess impact of news cycle timing
- [ ] **Economic Calendar**: Consider upcoming economic events

## Cognitive Bias Assessment
- [ ] **Anchoring Bias**: Check for fixation on specific price levels
- [ ] **Availability Bias**: Ensure not over-weighting easily recalled events
- [ ] **Survivorship Bias**: Consider failed trades/strategies in analysis
- [ ] **Hindsight Bias**: Avoid post-hoc reasoning in pattern recognition
- [ ] **Gambler's Fallacy**: Don't assume reversals due to streaks
- [ ] **Loss Aversion**: Check if avoiding losses irrationally

## Contrarian Analysis Requirements
### Mandatory for High Bias Situations:
- [ ] **Opposing Direction Analysis**: Generate opposite direction thesis
- [ ] **Contrarian Evidence**: Find supporting evidence for opposing view
- [ ] **Devil's Advocate**: Challenge all assumptions in original analysis
- [ ] **Failure Scenarios**: Identify potential failure modes
- [ ] **Contrarian Probability**: Estimate probability of contrarian scenario
- [ ] **Contrarian Timeline**: Assess timeframe for potential reversal

## Bias Correction Actions
### Low Bias (Green: <50%):
- [ ] **No Action Required**: Proceed with standard analysis
- [ ] **Continue Monitoring**: Maintain awareness of bias levels
- [ ] **Standard Documentation**: Record bias levels for tracking

### Moderate Bias (Yellow: 50-70%):
- [ ] **Confidence Reduction**: Reduce signal confidence by 10-20%
- [ ] **Enhanced Scrutiny**: Apply additional validation to same-direction signals
- [ ] **Contrarian Consideration**: Include brief contrarian analysis
- [ ] **Size Adjustment**: Consider reducing position size by 25%

### High Bias (Orange: 70-80%):
- [ ] **Mandatory Contrarian Analysis**: Full opposing viewpoint required
- [ ] **Confidence Cap**: Limit confidence to maximum 70%
- [ ] **Size Reduction**: Reduce position size by 50%
- [ ] **Additional Confirmation**: Require 3+ confirming indicators
- [ ] **Enhanced Monitoring**: Increase position monitoring frequency

### Critical Bias (Red: >80%):
- [ ] **Trade Suspension**: Consider suspending same-direction trades
- [ ] **Emergency Review**: Conduct immediate portfolio bias review
- [ ] **Forced Contrarian**: Actively look for opposite direction opportunities
- [ ] **Maximum Reduction**: Reduce position sizes by 75% or skip
- [ ] **Bias Reset Protocol**: Implement systematic bias reduction measures

## Memory System Integration
- [ ] **Bias Record Saving**: Save bias analysis to memory system
- [ ] **Historical Bias Tracking**: Retrieve previous bias patterns
- [ ] **Bias Effectiveness Tracking**: Monitor bias detection effectiveness
- [ ] **Pattern Learning**: Update bias detection based on outcomes
- [ ] **Contrarian Success Rate**: Track success of contrarian analyses

## Red Flags - High Bias Risk
- [ ] **Emotional Language**: Avoiding emotional or certain language
- [ ] **Confirmation Seeking**: Not seeking only confirming evidence
- [ ] **Pattern Forcing**: Not forcing patterns where none exist
- [ ] **Dismissing Contrary Evidence**: Not ignoring opposing indicators
- [ ] **Overconfidence Signals**: Not expressing extreme confidence
- [ ] **Urgency Pressure**: Not feeling pressure to trade immediately

## Bias Detection Tools Integration
- [ ] **MCP Tool Usage**: Properly using get_top_long_short_account_ratio
- [ ] **Memory Tool Usage**: Using mcp_openmemory tools for bias tracking
- [ ] **Data Validation**: Ensuring data quality for bias analysis
- [ ] **Tool Reliability**: Verifying MCP tool responses are reasonable

## Post-Analysis Validation
- [ ] **Bias Summary Complete**: Clear summary of all bias assessments
- [ ] **Action Plan Defined**: Specific actions based on bias level
- [ ] **Documentation Ready**: Bias analysis ready for memory storage
- [ ] **Monitoring Plan**: Plan for ongoing bias monitoring
- [ ] **Correction Effectiveness**: Method to measure bias correction success

## Quality Assurance
- [ ] **Checklist Completion**: All relevant sections completed
- [ ] **Bias Level Classification**: Clear classification of bias level
- [ ] **Appropriate Actions**: Actions match detected bias level
- [ ] **Documentation Quality**: Clear and complete bias documentation
- [ ] **Learning Integration**: Results will improve future bias detection

Remember: **Bias detection is critical for trading success. Never skip or rush through bias analysis, especially for high-confidence signals.**
