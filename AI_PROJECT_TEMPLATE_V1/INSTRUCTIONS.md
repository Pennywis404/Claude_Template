# AI Project Template - Instructions

**This file explains how to use this template for your projects. Read this document with Claude Code when starting a new project.**

## Table of Contents

1. [Overview](#overview)
2. [Template Structure](#template-structure)
3. [Quick Start](#quick-start)
4. [What to Modify](#what-to-modify)
5. [What to Keep](#what-to-keep)
6. [Project-Specific Customization](#project-specific-customization)
7. [Working with Claude Code](#working-with-claude-code)
8. [Best Practices](#best-practices)
9. [Troubleshooting](#troubleshooting)

---

## Overview

This template implements **Context Engineering** - a comprehensive system for providing AI coding assistants with all the context they need to build features end-to-end.

### What is Context Engineering?

Context Engineering is 10x better than prompt engineering and 100x better than "vibe coding". It provides:
- **Complete Documentation**: AI has access to all relevant information
- **Code Examples**: AI follows your established patterns
- **Validation Loops**: AI self-corrects through automated testing
- **Implementation Blueprints**: Clear step-by-step guidance via PRPs

### Template Philosophy

- **KISS**: Keep It Simple, Stupid
- **YAGNI**: You Aren't Gonna Need It
- **Fail Fast**: Catch errors early
- **Single Responsibility**: Each component has one clear purpose

---

## Template Structure

```
AI_PROJECT_TEMPLATE/
├── .claude/                    # Claude Code configuration
│   ├── agents/                # Custom AI agents
│   │   ├── documentation-manager.md    # Auto-updates docs
│   │   └── validation-gates.md         # Validates implementations
│   ├── commands/              # Slash commands
│   │   ├── generate-prp.md            # Generate implementation blueprints
│   │   ├── execute-prp.md             # Execute PRPs with validation
│   │   ├── primer.md                  # Quick primers
│   │   ├── fix-github-issue.md        # Fix GitHub issues
│   │   ├── prep-parallel.md           # Prepare parallel tasks
│   │   └── execute-parallel.md        # Execute tasks in parallel
│   ├── hooks/                 # Event-triggered automation
│   │   ├── README.md                  # Hooks documentation
│   │   ├── example-hook-config.json   # Example configuration
│   │   └── log-tool-usage.sh          # Example logging hook
│   └── settings.local.json    # Permission preauthorization
├── PRPs/                      # Product Requirements Prompts
│   ├── templates/
│   │   └── prp_base.md       # PRP template
│   ├── ai_docs/              # Documentation for AI reference
│   ├── EXAMPLE_multi_agent_prp.md     # Example PRP
│   └── README.md             # PRP documentation
├── examples/                  # Code examples and patterns
│   └── README.md             # Examples documentation
├── tests/                     # Test files
├── src/                       # Source code
├── docs/                      # Project documentation
│   ├── ARCHITECTURE.md       # System architecture
│   ├── API.md                # API documentation
│   └── CONTRIBUTING.md       # Contribution guidelines
├── .env.example              # Environment variables template
├── .gitignore                # Git ignore patterns
├── CLAUDE.md                 # AI behavior rules (CRITICAL)
├── PLANNING.md               # Project architecture and goals
├── TASK.md                   # Task tracking
├── INITIAL.md                # Feature request template
├── INITIAL_EXAMPLE.md        # Example feature request
├── README.md                 # Project overview
└── INSTRUCTIONS.md           # This file (delete after setup)
```

---

## Quick Start

### 1. Copy the Template

```bash
# Copy template to new project directory
cp -r AI_PROJECT_TEMPLATE my-new-project
cd my-new-project

# Initialize git
git init

# Optional: Remove INSTRUCTIONS.md after reading
# rm INSTRUCTIONS.md
```

### 2. Customize Core Files

**MUST MODIFY** (these define your project):
- `README.md` - Project description and setup
- `PLANNING.md` - Architecture and technical decisions
- `CLAUDE.md` - Coding standards (or keep defaults)
- `TASK.md` - Initial tasks and goals
- `.env.example` - Environment variables for your project

### 3. Add Your Code

- Place source code in `src/`
- Add tests in `tests/`
- Include examples in `examples/`

### 4. Start Using Context Engineering

```bash
# Open with Claude Code
claude-code .

# Create a feature request
# Edit INITIAL.md with your feature description

# Generate implementation blueprint
/generate-prp INITIAL.md

# Execute the PRP
/execute-prp PRPs/your-feature-name.md
```

---

## What to Modify

### 🔴 MUST MODIFY for Every Project

#### 1. README.md
**Purpose**: Project overview and quick start guide

**What to change**:
- Replace `[PROJECT NAME]` with your project name
- Add project description
- Update installation commands
- Add run commands
- Update project structure diagram if needed
- Update available commands if you add custom slash commands

#### 2. PLANNING.md
**Purpose**: Technical architecture and design decisions

**What to change**:
- Define project purpose and goals
- Document architecture (add diagrams)
- List technology stack
- Describe directory structure
- Document design decisions
- List dependencies
- Note constraints and requirements

#### 3. TASK.md
**Purpose**: Track current and future tasks

**What to change**:
- Add initial project tasks
- Set sprint/iteration dates
- List priorities

**Keep updating** as work progresses!

#### 4. .env.example
**Purpose**: Template for environment variables

**What to change**:
- Add all environment variables your project needs
- Provide example values (not real secrets!)
- Group related variables
- Add comments explaining each variable

#### 5. docs/ Directory

**ARCHITECTURE.md**:
- Document your system architecture
- Add component descriptions
- Include data flow diagrams
- Document security and scalability

**API.md**:
- Document all API endpoints
- Include request/response examples
- List error codes
- Add authentication details

**CONTRIBUTING.md**:
- Customize for your project's workflow
- Update coding standards
- Modify commit guidelines
- Set PR requirements

### 🟡 SHOULD CUSTOMIZE for Most Projects

#### 6. CLAUDE.md
**Purpose**: AI behavior rules and coding standards

**Default settings are good**, but customize if you:
- Use different languages (default is Python-focused)
- Have specific coding conventions
- Need different file size limits
- Have unique testing requirements
- Want specific documentation formats

**What to modify**:
- Language and framework preferences
- File/function size limits
- Testing requirements
- Style conventions
- Documentation standards

#### 7. .gitignore
**Purpose**: Files git should ignore

**What to change**:
- Add language-specific ignores
- Add framework-specific ignores
- Add build output directories
- Add IDE-specific files

#### 8. .claude/settings.local.json
**Purpose**: Preauthorize commands for Claude Code

**What to change**:
- Add commands you use frequently
- Add language-specific test commands (pytest, jest, etc.)
- Add build commands
- Add linting commands

**Example additions**:
```json
{
  "permissions": {
    "allow": [
      "Bash(npm:*)",
      "Bash(jest:*)",
      "Bash(docker:*)",
      "WebFetch(domain:your-api.com)"
    ]
  }
}
```

### 🟢 OPTIONAL to Modify

#### 9. examples/ Directory
**Add code examples** showing:
- Your coding patterns
- Testing approaches
- Integration methods
- Common use cases

#### 10. .claude/commands/
**Add custom slash commands** for:
- Project-specific workflows
- Deployment procedures
- Database migrations
- Custom test suites

#### 11. .claude/agents/
**Add custom agents** for:
- Domain-specific validation
- Custom documentation generation
- Specialized code review
- Project-specific automation

#### 12. PRPs/templates/prp_base.md
**Customize PRP template** if you:
- Have unique validation requirements
- Use different testing frameworks
- Need additional sections
- Have specific implementation patterns

---

## What to Keep

### ✅ Keep As-Is (Already Optimal)

These files are designed to work out of the box:

1. **INITIAL.md** - Feature request template (works universally)
2. **INITIAL_EXAMPLE.md** - Example showing how to use INITIAL.md
3. **PRPs/templates/prp_base.md** - PRP template (unless you have specific needs)
4. **PRPs/EXAMPLE_multi_agent_prp.md** - Example PRP
5. **.claude/commands/** - Slash commands (unless you need project-specific ones)
6. **.claude/agents/** - AI agents (unless you need custom ones)
7. **.claude/hooks/** - Hooks examples (unless you want to use them)

---

## Project-Specific Customization

### Language-Specific Setup

#### Python Projects
```bash
# Add to your project:
- pyproject.toml or requirements.txt
- pytest.ini or pyproject.toml [tool.pytest]
- .python-version (if using pyenv)

# Update CLAUDE.md:
- Confirm Python version
- List required packages
- Document virtual environment setup

# Update .claude/settings.local.json:
"Bash(pytest:*)",
"Bash(ruff:*)",
"Bash(mypy:*)",
"Bash(uv:*)"
```

#### JavaScript/TypeScript Projects
```bash
# Add to your project:
- package.json
- tsconfig.json (for TypeScript)
- .eslintrc or eslint.config.js
- jest.config.js (if using Jest)

# Update CLAUDE.md:
- Specify Node version
- Document npm/yarn/pnpm preference
- List key dependencies

# Update .claude/settings.local.json:
"Bash(npm:*)",
"Bash(yarn:*)",
"Bash(jest:*)",
"Bash(tsc:*)"
```

#### Go Projects
```bash
# Add to your project:
- go.mod
- go.sum

# Update CLAUDE.md:
- Go version
- Project structure conventions
- Testing approach (go test)

# Update .claude/settings.local.json:
"Bash(go:*)"
```

### Framework-Specific Setup

#### FastAPI (Python)
```markdown
# Update CLAUDE.md with:
- FastAPI-specific patterns
- Pydantic model conventions
- Router organization
- Dependency injection patterns

# Add to examples/:
- API endpoint example
- Pydantic model example
- Dependency injection example
```

#### Next.js (React)
```markdown
# Update CLAUDE.md with:
- Component structure
- App Router vs Pages Router
- Server/Client component patterns
- State management approach

# Add to examples/:
- Page component example
- API route example
- Server component example
```

### Database Setup

#### PostgreSQL
```markdown
# Update PLANNING.md:
- Database schema
- Migration strategy
- Connection pooling

# Add to .env.example:
DATABASE_URL="postgresql://user:password@localhost:5432/dbname"
DATABASE_POOL_SIZE="10"

# Add to examples/:
- Database connection example
- Query pattern example
- Migration example
```

### Testing Setup

#### Unit Testing
```markdown
# Update CLAUDE.md:
- Testing framework (pytest, jest, etc.)
- Test organization strategy
- Coverage requirements
- Mocking approach

# Add to examples/tests/:
- Unit test example
- Integration test example
- Fixture/mock example
```

---

## Working with Claude Code

### Development Workflow

#### 1. Starting a New Feature

```markdown
1. Update TASK.md with the new feature
2. Create INITIAL.md describing the feature:
   - What needs to be built
   - Examples to follow (in examples/)
   - Documentation to reference
   - Gotchas and considerations
3. Generate PRP: /generate-prp INITIAL.md
4. Review the generated PRP
5. Execute: /execute-prp PRPs/feature-name.md
6. Mark task complete in TASK.md
```

#### 2. Starting a New Conversation

When opening Claude Code in a new conversation:

```markdown
Claude will automatically read CLAUDE.md

Additionally, you can say:
"Read PLANNING.md to understand the architecture"
"Check TASK.md for current work"

Or just start working - Claude has context!
```

#### 3. Using Slash Commands

Available commands:
- `/generate-prp [file]` - Generate implementation blueprint
- `/execute-prp [file]` - Execute PRP with validation
- `/primer` - Get quick project primer
- `/fix-github-issue [number]` - Fix specific issue
- `/prep-parallel` - Prepare parallel task execution
- `/execute-parallel` - Execute multiple tasks in parallel

#### 4. Using AI Agents

Agents are called automatically or manually:

**documentation-manager**:
- Automatically updates docs when code changes
- Ensures README accuracy
- Maintains API documentation

**validation-gates**:
- Validates implementations meet requirements
- Runs comprehensive checks
- Ensures quality standards

Call manually: Reference the agent by name in your request

### Validation Loops

Every PRP includes validation loops:

**Level 1: Syntax & Style**
```bash
# Python
ruff check --fix && mypy .

# JavaScript
npm run lint && npm run type-check
```

**Level 2: Unit Tests**
```bash
# Python
pytest tests/ -v

# JavaScript
npm test
```

**Level 3: Integration Tests**
```bash
# Python
pytest tests/integration/ -v

# JavaScript
npm run test:integration
```

**Final Checklist**:
- All tests pass
- No linting errors
- No type errors
- Manual testing successful
- Documentation updated

---

## Best Practices

### 1. Always Read PLANNING.md First

At the start of each Claude Code session, have Claude read PLANNING.md:
```
"Read PLANNING.md to understand the project architecture"
```

### 2. Keep TASK.md Updated

- Add tasks as you discover them
- Mark completed tasks immediately
- Update priorities regularly

### 3. Provide Rich Examples

The more examples in `examples/`, the better Claude Code performs:
- Add examples of your coding patterns
- Include both good and bad examples
- Document why patterns are used

### 4. Use PRPs for Complex Features

Simple changes: Direct implementation
Complex features: Create INITIAL.md → Generate PRP → Execute PRP

### 5. Customize CLAUDE.md Early

Set your coding standards early:
- File size limits
- Testing requirements
- Documentation standards
- Style preferences

### 6. Leverage Validation Loops

Always include executable validation commands in PRPs:
- Makes Claude Code self-correcting
- Ensures working code on first try
- Catches issues early

### 7. Document Gotchas

In CLAUDE.md or PLANNING.md, document:
- Common mistakes
- Library quirks
- Performance considerations
- Security requirements

### 8. Use Hooks for Automation

Set up hooks for:
- Pre-commit checks
- Tool usage logging
- Custom validations
- Notifications

### 9. Keep PRPs Updated

After implementation:
- Note what worked well
- Document unexpected issues
- Update template for future features

### 10. Reference Real Files

In PRPs and INITIAL.md, always reference:
- Actual file paths
- Real code examples
- Specific documentation URLs
- Concrete patterns to follow

---

## Troubleshooting

### Issue: Claude Code Doesn't Follow Patterns

**Solution**:
1. Add more examples to `examples/`
2. Reference specific examples in INITIAL.md
3. Add pattern documentation to CLAUDE.md
4. Include pseudocode in PRPs showing exact patterns

### Issue: Generated PRP is Incomplete

**Solution**:
1. Make INITIAL.md more specific
2. Add more examples
3. Include more documentation URLs
4. List all gotchas and considerations
5. Manually edit the PRP before executing

### Issue: Validation Fails

**Solution**:
1. Check validation commands are correct for your setup
2. Ensure dependencies are installed
3. Verify test patterns match your framework
4. Update PRP template with correct commands

### Issue: Claude Code Ignores CLAUDE.md Rules

**Solution**:
1. Make rules more specific with examples
2. Reference rules in INITIAL.md
3. Include rules in PRP context
4. Remind Claude in conversation

### Issue: Tests Don't Pass

**Solution**:
1. Ensure test examples are in `examples/tests/`
2. Document testing patterns in CLAUDE.md
3. Include test requirements in PRPs
4. Make validation loops more explicit

### Issue: Documentation Gets Stale

**Solution**:
1. Use documentation-manager agent
2. Add "Update docs" to validation checklist
3. Include documentation in PR requirements
4. Review docs in TASK.md regularly

---

## Advanced Features

### Custom Slash Commands

Create project-specific commands in `.claude/commands/`:

```markdown
# deploy-staging.md
Deploy the application to staging environment

## Process
1. Run tests
2. Build artifacts
3. Deploy to staging
4. Run smoke tests
5. Report status
```

### Custom Agents

Create specialized agents in `.claude/agents/`:

```markdown
---
name: security-auditor
description: "Reviews code for security vulnerabilities"
tools: Read, Grep, Glob
---

Review code for:
- SQL injection risks
- XSS vulnerabilities
- Authentication issues
- Insecure dependencies
```

### Hooks

Set up event-driven automation in `.claude/hooks/`:

See `.claude/hooks/README.md` for details.

### Parallel Execution

For independent tasks:
```bash
/prep-parallel
# List tasks
/execute-parallel
```

---

## Migration to New Projects

### Copying Template

```bash
# Full template
cp -r AI_PROJECT_TEMPLATE new-project

# Minimal template (just essentials)
cp -r AI_PROJECT_TEMPLATE/\{.claude,PRPs,examples,.env.example,.gitignore,CLAUDE.md,PLANNING.md,TASK.md,INITIAL.md,README.md\} new-project/
```

### Template Maintenance

Keep your template updated:
1. **After each project**, note what worked
2. **Update examples** with new patterns
3. **Refine CLAUDE.md** rules
4. **Improve PRP templates** based on experience
5. **Share learnings** with your team

---

## Final Checklist

Before starting development with this template:

- [ ] Copied template to new project directory
- [ ] Updated README.md with project details
- [ ] Filled in PLANNING.md with architecture
- [ ] Added initial tasks to TASK.md
- [ ] Created .env.example with needed variables
- [ ] Customized CLAUDE.md for your language/framework
- [ ] Updated .gitignore for your stack
- [ ] Added examples to examples/ directory
- [ ] Customized .claude/settings.local.json permissions
- [ ] Initialized git repository
- [ ] Created .env from .env.example
- [ ] Read this INSTRUCTIONS.md file with Claude Code
- [ ] **Optional**: Deleted INSTRUCTIONS.md (keep for reference if needed)

---

## Questions?

This template is based on the Context Engineering principles from the [context-engineering-intro](https://github.com/coleam00/context-engineering-intro) repository.

For more information:
- [Claude Code Documentation](https://docs.anthropic.com/en/docs/claude-code)
- [Context Engineering Best Practices](https://www.philschmid.de/context-engineering)

---

**Remember**: Context Engineering is about giving AI all the context it needs to succeed. The more context you provide, the better the results!

Happy coding! 🚀
