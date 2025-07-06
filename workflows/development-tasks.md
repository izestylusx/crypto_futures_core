# Development Task Workflow

## Purpose
Execute structured development tasks for system enhancement and expansion while maintaining system integrity.

## Available Development Tasks

### 1. Create Trading Strategy (*dev-task create-trading-strategy)
- **Purpose**: Develop new trading strategies following CFTAS standards
- **Process**: Strategy conceptualization → Technical implementation → Backtesting → Integration
- **Dependencies**: strategy-template.md, bias-detector.md, signal-to-execution.md
- **Output**: Complete strategy document, backtesting results, system integration

### 2. Enhance Trading Agent (*dev-task enhance-trading-agent)
- **Purpose**: Modify or enhance existing crypto trading agents
- **Process**: Agent analysis → Design enhancement → Implementation → Integration & testing
- **Dependencies**: agent-template.md, cft-orchestrator.md, team configurations
- **Output**: Enhanced agent specification, updated configurations, test results

### 3. System Integration (*dev-task system-integration)
- **Purpose**: Integrate new tools, APIs, or capabilities into CFTAS
- **Process**: Integration planning → Technical implementation → Validation → Documentation
- **Dependencies**: utils/ directory, affected agents and workflows, core-config.yml
- **Output**: Integration implementation, updated capabilities, documentation

## Workflow Steps

### Phase 1: Task Selection and Preparation
1. **Task Identification**: Use `*dev-task` command to list available tasks
2. **Requirements Analysis**: Review prerequisites and dependencies
3. **Resource Allocation**: Ensure necessary MCP tools and configurations are available
4. **Risk Assessment**: Evaluate potential impact on existing system

### Phase 2: Task Execution
1. **Load Task Template**: Access specific task file from tasks/ directory
2. **Follow Task Instructions**: Execute step-by-step process outlined in task
3. **Document Progress**: Maintain development log throughout process
4. **Validation Checkpoints**: Run bias detection and reality checks at each phase

### Phase 3: Integration and Testing
1. **System Integration**: Incorporate new elements into existing architecture
2. **Compatibility Testing**: Verify new additions work with existing components
3. **Risk Validation**: Ensure changes don't compromise trading safety
4. **Documentation Update**: Update system documentation and help files

### Phase 4: Deployment and Monitoring
1. **Staged Deployment**: Implement changes incrementally
2. **Performance Monitoring**: Track system performance after changes
3. **Rollback Preparation**: Maintain ability to revert if issues arise
4. **Knowledge Base Update**: Update orchestrator and agent knowledge

## Safety Protocols

### Before Starting Any Development Task
- [ ] Backup current system state
- [ ] Review impact on active trading operations
- [ ] Ensure development environment separation
- [ ] Validate all dependencies are available

### During Development
- [ ] Follow bias detection protocols
- [ ] Test incrementally
- [ ] Document all changes
- [ ] Maintain system coherence

### After Completion
- [ ] Comprehensive testing
- [ ] Update all affected documentation
- [ ] Train relevant agents on new capabilities
- [ ] Monitor system stability

## Integration with CFT System

### Orchestrator Commands
- `*dev-task` - List available development tasks
- `*dev-task [name]` - Execute specific development task
- `*dev-task status` - Show current development task progress

### Dependencies
- **Tasks**: create-trading-strategy.md, enhance-trading-agent.md, system-integration.md
- **Utils**: bias-detector.md, reality-validator.md, memory-manager.md
- **Templates**: agent-template.md, strategy-template.md, analysis-template.md
- **Checklists**: bias-detection-checklist.md, reality-check-checklist.md

### Success Criteria
- All new elements follow CFTAS architectural principles
- System integrity maintained throughout development
- Proper documentation and integration completed
- Testing validates safety and functionality
- Bias detection protocols satisfied

## Usage Examples

### Creating a New Trading Strategy
```
*dev-task create-trading-strategy
> Loads strategy creation workflow
> Guides through conceptualization, implementation, testing
> Ensures proper integration with existing system
```

### Enhancing an Existing Agent
```
*dev-task enhance-trading-agent
> Analyzes current agent capabilities
> Designs improvements while maintaining compatibility
> Tests enhanced functionality
> Updates team configurations
```

### Integrating New MCP Tools
```
*dev-task system-integration
> Plans integration of new capabilities
> Implements utilities and agent updates
> Validates against risk management
> Documents new functionality
```

This workflow ensures that all system development follows structured, safe, and validated processes while maintaining the high standards required for crypto trading operations.
