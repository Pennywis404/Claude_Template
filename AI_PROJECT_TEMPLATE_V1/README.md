# [PROJECT NAME]

**Replace this with your project description.**

## Overview

[Brief description of what this project does and its purpose]

## Quick Start

```bash
# 1. Clone the repository
git clone [your-repo-url]
cd [project-name]

# 2. Set up environment
cp .env.example .env
# Edit .env with your configuration

# 3. Install dependencies
# [Add your installation commands here]

# 4. Run the project
# [Add your run commands here]
```

## Project Structure

```
[PROJECT]/
├── .claude/              # Claude Code configuration
│   ├── agents/          # Custom AI agents
│   ├── commands/        # Slash commands for workflows
│   ├── hooks/           # Event-triggered automation
│   └── settings.local.json
├── PRPs/                # Product Requirements Prompts
├── examples/            # Code patterns and examples
├── src/                 # Source code
├── tests/              # Test files
├── docs/               # Additional documentation
└── CLAUDE.md           # AI behavior rules
```

## Development Workflow

### Using Context Engineering

This project uses Context Engineering to work effectively with AI coding assistants:

1. **Read PLANNING.md** - Understand the architecture and goals
2. **Check TASK.md** - See what needs to be done
3. **Use INITIAL.md** - Create feature requests
4. **Generate PRPs** - Run `/generate-prp INITIAL.md`
5. **Execute PRPs** - Run `/execute-prp PRPs/feature-name.md`

### Available Commands

- `/generate-prp [file]` - Generate a comprehensive implementation blueprint
- `/execute-prp [file]` - Execute a PRP with validation loops
- `/primer` - Quick project primers
- `/fix-github-issue [number]` - Fix a specific GitHub issue

## Documentation

- [CLAUDE.md](./CLAUDE.md) - AI behavior rules and coding standards
- [PLANNING.md](./PLANNING.md) - Project architecture and design decisions
- [TASK.md](./TASK.md) - Current tasks and progress tracking
- [docs/ARCHITECTURE.md](./docs/ARCHITECTURE.md) - System architecture
- [docs/API.md](./docs/API.md) - API documentation
- [docs/CONTRIBUTING.md](./docs/CONTRIBUTING.md) - Contribution guidelines

## Testing

```bash
# Run tests
[Add your test commands here]
```

## Contributing

See [CONTRIBUTING.md](./docs/CONTRIBUTING.md) for guidelines.

## License

[Add your license here]
