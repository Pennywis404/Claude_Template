# Code Examples

This directory contains code examples and patterns that demonstrate best practices for this project.

## Purpose

Examples serve as references for:
- Code structure and organization
- Implementation patterns
- Testing approaches
- Integration methods
- Common use cases

## Why Examples Matter

AI coding assistants work significantly better when they have concrete examples to follow. By providing well-structured examples, you ensure:
- **Consistency**: AI follows your established patterns
- **Quality**: AI replicates your coding standards
- **Efficiency**: AI requires less iteration to get things right
- **Learning**: New developers understand patterns quickly

## What to Include

### 1. Core Patterns

Place examples of your most common code patterns:

```
examples/
├── basic_module.py          # Basic module structure
├── api_client.py            # API client implementation
├── database_model.py        # Database model pattern
└── service_class.py         # Service layer pattern
```

### 2. Testing Patterns

Show how tests should be structured:

```
examples/
├── tests/
│   ├── test_unit.py         # Unit test example
│   ├── test_integration.py  # Integration test example
│   └── conftest.py          # Pytest configuration
```

### 3. Integration Examples

Demonstrate how to integrate with external services:

```
examples/
├── auth_flow.py             # Authentication implementation
├── external_api.py          # External API integration
└── background_job.py        # Background task example
```

### 4. CLI Patterns

If your project has CLI tools:

```
examples/
├── cli.py                   # CLI implementation
└── argument_parser.py       # Argument parsing pattern
```

## Using Examples in Feature Requests

When creating an INITIAL.md feature request, reference examples:

```markdown
## EXAMPLES:

- `examples/api_client.py` - Follow this pattern for HTTP client setup,
  including error handling and retry logic
- `examples/tests/test_unit.py` - Use this testing structure with the same
  mocking approach and assertion style
```

## Example Structure Template

Each example file should include:

```python
"""
Example: [What this demonstrates]

Purpose:
- [Key pattern 1]
- [Key pattern 2]

Usage:
    [How to use this pattern]

Notes:
- [Important consideration 1]
- [Important consideration 2]
"""

# Your example code here
```

## Best Practices

1. **Keep Examples Simple**: Focus on demonstrating specific patterns, not building complete features
2. **Add Comments**: Explain why things are done a certain way
3. **Show Both Good and Bad**: Include comments showing what NOT to do
4. **Keep Updated**: Update examples when patterns change
5. **Test Examples**: Ensure example code actually works

## Adding New Examples

When adding examples:
1. Create a descriptive filename
2. Add clear documentation at the top
3. Include inline comments for key decisions
4. Update this README with a brief description
5. Reference it in relevant PRPs or INITIAL.md files

## Example Categories

### [Category 1: e.g., Data Processing]
- `example1.py` - [Brief description]
- `example2.py` - [Brief description]

### [Category 2: e.g., API Endpoints]
- `example3.py` - [Brief description]
- `example4.py` - [Brief description]

### [Category 3: e.g., Testing]
- `example5.py` - [Brief description]

---

**Remember**: More examples = better AI-assisted development!
