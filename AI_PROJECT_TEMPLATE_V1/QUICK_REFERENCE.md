# Quick Reference - AI Project Template

**Essential commands and workflows for AI-assisted development**

## 🚀 Getting Started

```bash
# 1. Copy template
cp -r AI_PROJECT_TEMPLATE my-project
cd my-project

# 2. Customize
# - Edit README.md, PLANNING.md, TASK.md
# - Update CLAUDE.md with your standards
# - Create .env from .env.example

# 3. Initialize git
git init

# 4. Start coding with Claude Code
claude-code .
```

## 📋 Essential Files

| File | Purpose | Action |
|------|---------|--------|
| **INSTRUCTIONS.md** | Complete template guide | READ FIRST! |
| **CLAUDE.md** | AI behavior rules | Customize for your project |
| **PLANNING.md** | Architecture & decisions | Document your design |
| **TASK.md** | Task tracking | Keep updated |
| **INITIAL.md** | Feature request template | Use for each feature |

## 🛠️ Slash Commands

### Core Workflow Commands

```bash
# Generate implementation blueprint
/generate-prp INITIAL.md

# Execute a PRP
/execute-prp PRPs/feature-name.md

# Get quick project primer
/primer

# Fix a GitHub issue
/fix-github-issue 123
```

### Parallel Execution

```bash
# Prepare parallel tasks
/prep-parallel

# Execute tasks in parallel
/execute-parallel
```

## 🔄 Development Workflow

### Building a New Feature

```markdown
1. Update TASK.md
   - Add feature to task list

2. Create Feature Request (INITIAL.md)
   ## FEATURE:
   [What to build]

   ## EXAMPLES:
   [Reference examples/ files]

   ## DOCUMENTATION:
   [List relevant docs]

   ## OTHER CONSIDERATIONS:
   [Gotchas and requirements]

3. Generate PRP
   /generate-prp INITIAL.md

4. Review Generated PRP
   - Check PRPs/feature-name.md
   - Ensure context is complete
   - Verify validation commands

5. Execute PRP
   /execute-prp PRPs/feature-name.md

6. Mark Complete
   - Update TASK.md
   - Commit changes
```

### Starting New Conversation

```markdown
# Claude automatically reads CLAUDE.md

# Optionally remind Claude:
"Read PLANNING.md to understand the architecture"
"Check TASK.md for current work"
```

## 📁 Directory Structure

```
my-project/
├── .claude/          # AI configuration
├── PRPs/             # Implementation blueprints
├── examples/         # Code patterns (ADD THESE!)
├── src/              # Your source code
├── tests/            # Your tests
├── docs/             # Documentation
├── CLAUDE.md         # AI rules (customize)
├── PLANNING.md       # Architecture (fill in)
├── TASK.md           # Tasks (keep updated)
└── README.md         # Overview (customize)
```

## ✅ Validation Loops

### Python
```bash
# Syntax & Style
ruff check --fix && mypy .

# Unit Tests
pytest tests/ -v

# Integration Tests
pytest tests/integration/ -v
```

### JavaScript/TypeScript
```bash
# Syntax & Style
npm run lint && npm run type-check

# Unit Tests
npm test

# Integration Tests
npm run test:integration
```

## 🎯 Best Practices

### 1. Always Provide Examples
```bash
# Add to examples/
examples/
├── basic_module.py
├── api_client.py
├── tests/
│   └── test_example.py
```

### 2. Keep TASK.md Current
```markdown
## Active Tasks
- [ ] Feature X - Started: 2025-01-15
  - [ ] Subtask 1
  - [x] Subtask 2

## Completed Tasks
- [x] Feature Y - Completed: 2025-01-14
```

### 3. Document in PLANNING.md
```markdown
## Technology Stack
- Language: Python 3.11
- Framework: FastAPI
- Database: PostgreSQL

## Design Decisions
### Use FastAPI over Flask
Context: Need async support
Decision: FastAPI
Rationale: Better async, auto-docs
```

### 4. Reference Real Files
```markdown
# In INITIAL.md
## EXAMPLES:
- examples/auth_flow.py - Follow the JWT pattern
  and error handling approach
```

## 🤖 AI Agents

### documentation-manager
**Auto-updates docs when code changes**

```markdown
# Called automatically or:
"Use the documentation-manager agent to update README"
```

### validation-gates
**Validates implementations**

```markdown
"Run the validation-gates agent to check the implementation"
```

## 🔧 Customization Quick Tips

### Add Language Support

**Python**:
```json
// .claude/settings.local.json
"Bash(pytest:*)",
"Bash(ruff:*)",
"Bash(mypy:*)"
```

**JavaScript**:
```json
// .claude/settings.local.json
"Bash(npm:*)",
"Bash(jest:*)",
"Bash(eslint:*)"
```

### Custom Slash Command

Create `.claude/commands/my-command.md`:
```markdown
# My Custom Command

Do something specific to my project

## Steps
1. Step one
2. Step two
```

Use: `/my-command`

## 📊 PRP Structure

```markdown
## Goal
[What to build]

## All Needed Context
- Documentation URLs
- Code examples
- Known gotchas

## Implementation Blueprint
- Tasks in order
- Pseudocode
- Integration points

## Validation Loop
- Level 1: Syntax/style
- Level 2: Unit tests
- Level 3: Integration tests
```

## 🆘 Troubleshooting

| Problem | Solution |
|---------|----------|
| AI doesn't follow patterns | Add examples to `examples/` |
| Generated PRP incomplete | Make INITIAL.md more specific |
| Validation fails | Check commands in PRP match your setup |
| AI ignores CLAUDE.md | Reference rules in INITIAL.md |
| Tests don't pass | Add test examples to `examples/tests/` |

## 🎓 Learning Resources

- **INSTRUCTIONS.md** - Complete template guide
- **TEMPLATE_OVERVIEW.md** - Template summary
- **PRPs/README.md** - How to use PRPs
- **examples/README.md** - Adding examples
- [Claude Code Docs](https://docs.anthropic.com/en/docs/claude-code)

## 💡 Pro Tips

1. **Start Small**: Use simple features to learn the workflow
2. **Build Examples**: Add examples as you build features
3. **Iterate on PRPs**: Refine PRP template based on experience
4. **Keep Context Rich**: More context = better results
5. **Use Validation**: Let AI self-correct through testing
6. **Document Gotchas**: Add to CLAUDE.md or PLANNING.md
7. **Update Regularly**: Keep TASK.md and docs current

## ⚡ Common Commands

```bash
# Read important context
cat PLANNING.md
cat TASK.md

# Check template structure
ls -la .claude/

# View available commands
ls .claude/commands/

# View available agents
ls .claude/agents/

# Check examples
ls examples/

# View PRPs
ls PRPs/
```

## 📝 File Checklist

Before starting development:
- [ ] README.md customized
- [ ] PLANNING.md filled in
- [ ] TASK.md has initial tasks
- [ ] CLAUDE.md reviewed/customized
- [ ] .env.example created
- [ ] .gitignore updated
- [ ] examples/ has code patterns
- [ ] Git initialized

---

**Quick Start**: Read INSTRUCTIONS.md → Customize files → Add examples → Build with PRPs

**Key Workflow**: INITIAL.md → /generate-prp → Review → /execute-prp → Validate

**Remember**: Context is king - more examples and documentation = better AI results!
