# Contributing Guidelines

Thank you for considering contributing to this project! This document provides guidelines for contributing.

## Table of Contents

- [Code of Conduct](#code-of-conduct)
- [Getting Started](#getting-started)
- [Development Workflow](#development-workflow)
- [Coding Standards](#coding-standards)
- [Testing Guidelines](#testing-guidelines)
- [Commit Guidelines](#commit-guidelines)
- [Pull Request Process](#pull-request-process)

## Code of Conduct

- Be respectful and inclusive
- Focus on constructive feedback
- Help others learn and grow
- Maintain a professional environment

## Getting Started

### Prerequisites

[List prerequisites]

### Setup Development Environment

```bash
# 1. Fork and clone the repository
git clone [your-fork-url]
cd [project-name]

# 2. Set up environment
cp .env.example .env
# Edit .env with your configuration

# 3. Install dependencies
[installation commands]

# 4. Run tests to verify setup
[test commands]
```

## Development Workflow

### Using Context Engineering

This project uses Context Engineering for AI-assisted development:

1. **Read PLANNING.md** first to understand architecture
2. **Check TASK.md** before starting work
3. **Follow CLAUDE.md** rules for code consistency
4. **Use INITIAL.md** to create feature requests
5. **Generate PRPs** with `/generate-prp INITIAL.md`
6. **Execute PRPs** with `/execute-prp PRPs/feature-name.md`

### Branch Strategy

- `main` - Production-ready code
- `develop` - Development branch
- `feature/[name]` - Feature branches
- `fix/[name]` - Bug fix branches
- `docs/[name]` - Documentation branches

### Workflow Steps

1. **Create a branch**:
   ```bash
   git checkout -b feature/your-feature-name
   ```

2. **Make changes** following the coding standards

3. **Write tests** for your changes

4. **Run tests and linting**:
   ```bash
   [test command]
   [lint command]
   ```

5. **Commit changes** following commit guidelines

6. **Push to your fork**:
   ```bash
   git push origin feature/your-feature-name
   ```

7. **Create a Pull Request**

## Coding Standards

### General Principles

- **KISS**: Keep It Simple, Stupid - favor simple solutions
- **YAGNI**: You Aren't Gonna Need It - don't build speculative features
- **DRY**: Don't Repeat Yourself - avoid code duplication
- **Single Responsibility**: Each function/class should have one clear purpose

### Code Style

[Language-specific style guidelines]

**Python Example**:
- Follow PEP8
- Use type hints
- Max line length: 100 characters
- Max file length: 500 lines
- Max function length: 50 lines
- Use docstrings (Google style)

**JavaScript/TypeScript Example**:
- Follow StandardJS or ESLint rules
- Use TypeScript for type safety
- Prefer functional programming patterns
- Use async/await over promises

### File Organization

```
[Describe file organization structure]
```

### Naming Conventions

- **Variables**: `snake_case` or `camelCase`
- **Functions**: `snake_case` or `camelCase`
- **Classes**: `PascalCase`
- **Constants**: `UPPER_SNAKE_CASE`
- **Files**: `kebab-case` or `snake_case`

## Testing Guidelines

### Test Structure

- Tests should live in a `/tests` folder or next to the code they test
- Test files should mirror the source structure
- Each feature should have at least 3 tests:
  1. Happy path (expected use)
  2. Edge case
  3. Failure case

### Writing Tests

**Example**:
```python
def test_feature_happy_path():
    """Test expected behavior"""
    result = feature("valid_input")
    assert result.status == "success"

def test_feature_edge_case():
    """Test edge case handling"""
    result = feature("")
    assert result.status == "error"

def test_feature_failure():
    """Test error handling"""
    with pytest.raises(ValueError):
        feature(None)
```

### Running Tests

```bash
# Run all tests
[test command]

# Run specific test file
[specific test command]

# Run with coverage
[coverage command]
```

## Commit Guidelines

### Commit Message Format

```
<type>(<scope>): <subject>

<body>

<footer>
```

### Types

- `feat`: New feature
- `fix`: Bug fix
- `docs`: Documentation changes
- `style`: Code style changes (formatting, etc.)
- `refactor`: Code refactoring
- `test`: Adding or updating tests
- `chore`: Maintenance tasks

### Examples

```
feat(api): add user authentication endpoint

Implemented JWT-based authentication with refresh tokens.
Includes rate limiting and session management.

Closes #123
```

```
fix(database): resolve connection pool exhaustion

Modified pool size and timeout settings to prevent
connection exhaustion under high load.

Fixes #456
```

## Pull Request Process

### Before Submitting

- [ ] All tests pass
- [ ] Code follows style guidelines
- [ ] Documentation is updated
- [ ] Commit messages follow guidelines
- [ ] No merge conflicts with target branch

### PR Description Template

```markdown
## Description
[Describe your changes]

## Type of Change
- [ ] Bug fix
- [ ] New feature
- [ ] Breaking change
- [ ] Documentation update

## Testing
[Describe testing done]

## Checklist
- [ ] Tests pass
- [ ] Code follows style guide
- [ ] Documentation updated
- [ ] No breaking changes (or documented)

## Related Issues
Closes #[issue number]
```

### Review Process

1. At least one maintainer must review and approve
2. All comments must be addressed
3. All checks must pass (tests, linting, etc.)
4. No merge conflicts

### After Merge

- Delete your feature branch
- Update your local repository
- Close related issues

## Questions?

If you have questions, please:
- Check existing documentation
- Search closed issues
- Open a new issue with the "question" label
- Contact: [contact information]

Thank you for contributing! 🎉
