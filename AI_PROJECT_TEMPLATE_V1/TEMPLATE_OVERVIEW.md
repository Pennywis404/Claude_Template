# AI Project Template - Overview

**A comprehensive template for AI-assisted software development using Context Engineering**

## What You Have

This template contains everything you need to build projects effectively with AI coding assistants like Claude Code.

## Template Contents

### 🤖 AI Configuration (.claude/)

**Purpose**: Configure Claude Code's behavior and capabilities

- **agents/** - Specialized AI agents
  - `documentation-manager.md` - Auto-updates documentation
  - `validation-gates.md` - Validates implementations

- **commands/** - Custom slash commands
  - `/generate-prp` - Create implementation blueprints
  - `/execute-prp` - Execute PRPs with validation
  - `/primer` - Quick project primers
  - `/fix-github-issue` - Fix GitHub issues
  - `/prep-parallel` & `/execute-parallel` - Parallel task execution

- **hooks/** - Event-triggered automation
  - Examples for logging and validation

- **settings.local.json** - Preauthorized commands

### 📋 Implementation Blueprints (PRPs/)

**Purpose**: Comprehensive feature implementation guides

- **templates/prp_base.md** - Template for creating PRPs
- **ai_docs/** - Documentation for AI reference
- **EXAMPLE_multi_agent_prp.md** - Example PRP
- **README.md** - How to use PRPs

### 💡 Code Examples (examples/)

**Purpose**: Code patterns and best practices

- Place your code examples here
- AI will follow these patterns
- See README.md for guidance

### 🧪 Tests & Source

- **tests/** - Test files
- **src/** - Source code

### 📚 Documentation (docs/)

- **ARCHITECTURE.md** - System architecture
- **API.md** - API documentation
- **CONTRIBUTING.md** - Contribution guidelines

### 📝 Core Files

**Project Management**:
- **PLANNING.md** - Architecture and technical decisions
- **TASK.md** - Task tracking
- **README.md** - Project overview

**AI Guidance**:
- **CLAUDE.md** - AI behavior rules and coding standards
- **INITIAL.md** - Feature request template
- **INITIAL_EXAMPLE.md** - Example feature request

**Configuration**:
- **.env.example** - Environment variables template
- **.gitignore** - Git ignore patterns

**Documentation**:
- **INSTRUCTIONS.md** - How to use this template (READ THIS!)

## Quick Start

1. **Read INSTRUCTIONS.md** - Complete guide to using this template
2. **Customize core files** - Update README, PLANNING, TASK, CLAUDE.md
3. **Add your code** - Place in src/ with tests in tests/
4. **Add examples** - Put code patterns in examples/
5. **Start building** - Use /generate-prp and /execute-prp

## Key Concepts

### Context Engineering

Providing AI with comprehensive context through:
- **Documentation** - All relevant information
- **Examples** - Code patterns to follow
- **Rules** - Coding standards (CLAUDE.md)
- **Validation** - Automated testing loops

### PRPs (Product Requirements Prompts)

Implementation blueprints that include:
- Complete context and documentation
- Step-by-step tasks
- Validation loops
- Success criteria

### Workflow

```
Feature Request → Generate PRP → Review → Execute PRP → Validate
    (INITIAL.md)    (/generate-prp)           (/execute-prp)
```

## What Makes This Template Powerful

1. **Complete Context** - AI has everything it needs
2. **Validation Loops** - AI self-corrects through testing
3. **Examples** - AI follows your patterns
4. **Automation** - Agents and hooks streamline work
5. **Consistency** - Rules ensure quality
6. **Scalability** - Works for projects of any size

## File Priority

**MUST MODIFY**:
- README.md
- PLANNING.md
- TASK.md
- .env.example

**SHOULD CUSTOMIZE**:
- CLAUDE.md
- .gitignore
- .claude/settings.local.json
- docs/*

**OPTIONAL**:
- examples/* (but highly recommended)
- .claude/commands/* (add custom)
- .claude/agents/* (add custom)

**KEEP AS-IS**:
- INITIAL.md
- PRPs/templates/prp_base.md
- Most .claude/ files

## Next Steps

1. **READ**: Open INSTRUCTIONS.md with Claude Code
2. **CUSTOMIZE**: Update the "MUST MODIFY" files
3. **BUILD**: Start creating features with PRPs
4. **ITERATE**: Improve the template as you learn

## Benefits

- **Faster Development**: AI builds features end-to-end
- **Higher Quality**: Validation loops ensure working code
- **Consistency**: Examples and rules maintain standards
- **Less Iteration**: Comprehensive context gets it right first time
- **Better Documentation**: Auto-updated and always accurate

## Template Philosophy

> "Context Engineering is 10x better than prompt engineering and 100x better than vibe coding"

This template embodies best practices for:
- **KISS** - Keep It Simple
- **YAGNI** - You Aren't Gonna Need It
- **Fail Fast** - Catch errors early
- **Single Responsibility** - Clear, focused components

---

**Ready to start?** Read INSTRUCTIONS.md for complete guidance!
