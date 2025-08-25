# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a specialized agents repository for Claude Code's SuperClaude framework. The repository contains six specialized agent definitions that extend Claude Code's capabilities through systematic workflows and domain expertise.

## Architecture

### Agent System
The repository contains specialized agent definitions stored as markdown files with YAML frontmatter:

- **codebase-scanner.md**: Systematic codebase analysis and architectural mapping
- **documentation-expert.md**: Current documentation research using Context7 MCP
- **implementation-planner.md**: Step-by-step technical planning with TDD approach
- **requirements-analyst.md**: Transform vague requests into actionable specifications
- **test-designer.md**: Comprehensive TDD test coverage planning
- **tech-researcher-planner.md**: Technology research and architectural planning

### Agent Workflow Integration
Agents follow a structured workflow:
1. **Context Foundation**: Read project documentation and existing analysis
2. **Strategic Analysis**: Use "think hard" approach for complex decision-making
3. **Systematic Execution**: Follow domain-specific methodologies
4. **Documentation**: Save comprehensive analysis to `.claude/docs/` directory
5. **Context Updates**: Add findings to shared context for future agents

### SuperClaude Framework Integration
The repository integrates with the broader SuperClaude framework defined in the parent `.claude` directory, which includes:
- Command system (COMMANDS.md)
- Flag system (FLAGS.md) 
- Personas (PERSONAS.md)
- MCP server integration (MCP.md)
- Orchestration patterns (ORCHESTRATOR.md)

## Agent Usage Patterns

### Proactive Agent Usage
- **codebase-scanner**: Use after requirements analysis, before implementation planning
- **documentation-expert**: Use before implementation to ensure current best practices
- **test-designer**: Use before implementation following TDD principles
- **requirements-analyst**: Use immediately when requests are vague or ambiguous

### Sequential Agent Workflows
Common patterns for complex tasks:
1. **requirements-analyst** → **codebase-scanner** → **implementation-planner** → **test-designer**
2. **documentation-expert** → **tech-researcher-planner** → **implementation-planner**

## Key Principles

### Evidence-Based Development
- All agent analysis must be supported by actual code inspection
- Decisions based on measurable data and empirical evidence
- No assumptions without validation

### Test-Driven Development
- **test-designer** creates comprehensive test coverage before implementation
- Tests define success criteria and iteration targets
- Implementation follows Red-Green-Refactor cycles

### Systematic Analysis
- Agents use structured methodologies for consistent results
- "Think hard" approach for complex architectural decisions
- Course correction when patterns seem unclear

### Context Preservation
- Agents save comprehensive documentation to `.claude/docs/`
- Findings added to shared context for subsequent agents
- ≥90% context retention across agent handoffs

## Development Approach

### Planning Before Implementation
1. Use **requirements-analyst** to clarify vague requests
2. Use **codebase-scanner** to understand existing architecture 
3. Use **documentation-expert** for current best practices research
4. Use **implementation-planner** for detailed technical approach
5. Use **test-designer** for TDD test coverage strategy

### Quality Standards
- Every recommendation must be traceable to specific evidence
- All architectural patterns must be supported with file examples
- Risk assessments must cite specific code locations
- Integration recommendations based on existing successful patterns

This agents repository extends Claude Code with specialized domain expertise, systematic workflows, and evidence-based decision-making capabilities for complex software development tasks.