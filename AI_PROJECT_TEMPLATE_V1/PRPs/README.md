# Product Requirements Prompts (PRPs)

This directory contains PRPs - comprehensive implementation blueprints for features.

## What are PRPs?

PRPs (Product Requirements Prompts) are like PRDs (Product Requirements Documents), but specifically designed to guide AI coding assistants through complex implementations. They include:

- **Complete Context**: All documentation, patterns, and gotchas
- **Implementation Blueprint**: Step-by-step tasks and pseudocode
- **Validation Loops**: Executable tests and checks
- **Success Criteria**: Clear definition of done

## Directory Structure

```
PRPs/
├── templates/
│   └── prp_base.md              # Base template for creating PRPs
├── ai_docs/                      # Documentation for AI reference
│   └── [documentation files]    # API docs, library docs, etc.
├── EXAMPLE_multi_agent_prp.md   # Example of a complete PRP
└── [feature-name].md            # Your feature PRPs
```

## Workflow

### 1. Create Feature Request

Start by creating an `INITIAL.md` file describing what you want to build:

```markdown
## FEATURE:
Build a user authentication system with JWT tokens

## EXAMPLES:
- examples/auth_flow.py - Follow this pattern for token handling

## DOCUMENTATION:
- https://jwt.io/introduction/ - JWT documentation
- https://fastapi.tiangolo.com/tutorial/security/ - FastAPI security

## OTHER CONSIDERATIONS:
- Use bcrypt for password hashing
- Implement refresh token rotation
- Add rate limiting to prevent brute force attacks
```

### 2. Generate PRP

Run the generate command in Claude Code:

```bash
/generate-prp INITIAL.md
```

This will:
1. Analyze your codebase for patterns
2. Research relevant documentation
3. Create a comprehensive PRP in `PRPs/user-authentication.md`

### 3. Review PRP

Review the generated PRP to ensure:
- All context is included
- Implementation steps are clear
- Validation commands are correct
- Success criteria are complete

### 4. Execute PRP

Run the execute command:

```bash
/execute-prp PRPs/user-authentication.md
```

The AI will:
1. Load all context from the PRP
2. Create a detailed task list
3. Implement each component
4. Run validation loops
5. Fix any issues found
6. Ensure all success criteria are met

## PRP Template Structure

A PRP includes these sections:

### Goal, Why, What
- **Goal**: What needs to be built
- **Why**: Business value and purpose
- **What**: User-visible behavior and technical requirements

### All Needed Context
- Documentation URLs with specific sections
- Code examples from the codebase
- Known gotchas and library quirks
- Current and desired codebase structure

### Implementation Blueprint
- Data models and structure
- Ordered list of tasks
- Pseudocode with critical details
- Integration points

### Validation Loops
- **Level 1**: Syntax & style checks
- **Level 2**: Unit tests
- **Level 3**: Integration tests
- **Final Checklist**: All requirements met

### Anti-Patterns
- Common mistakes to avoid
- What NOT to do

## ai_docs/ Directory

The `ai_docs/` directory stores documentation for AI reference:

- API documentation (copied from web)
- Library guides and examples
- Architecture decision records
- Domain-specific knowledge
- Common patterns and gotchas

**When to add docs**:
- External APIs you frequently use
- Complex library configurations
- Domain knowledge that's hard to find online
- Internal architecture documents

## Best Practices

### Writing Effective PRPs

1. **Include All Context**: Don't assume the AI knows your preferences
2. **Be Specific**: Reference actual files and line numbers where relevant
3. **Provide Examples**: Show patterns to follow from your codebase
4. **List Gotchas**: Include common pitfalls and how to avoid them
5. **Make Tests Executable**: Validation commands must actually run
6. **Score Confidence**: Rate the PRP's completeness (1-10)

### PRP Maintenance

- **Update After Implementation**: Note what worked and what didn't
- **Refine for Reuse**: If building similar features, improve the PRP
- **Archive Completed**: Move implemented PRPs to a `completed/` folder
- **Document Learnings**: Add notes about unexpected challenges

## Example PRPs

See `EXAMPLE_multi_agent_prp.md` for a complete example showing:
- How to structure context
- How to write implementation steps
- How to define validation loops
- How to set success criteria

## Tips for Success

### For Simple Features
- Quick feature requests might not need a full PRP
- Use INITIAL.md and execute directly with Claude Code
- Generate PRPs for features that need multiple steps

### For Complex Features
- Always generate a PRP first
- Spend time on the research phase
- Include more examples and documentation
- Break into smaller PRPs if needed

### For Iterative Development
- Create PRP for initial version
- Execute and validate
- Create follow-up PRPs for enhancements
- Reference previous PRPs in new ones

## Validation Loop Examples

### Python Projects
```bash
# Syntax/Style
ruff check --fix && mypy .

# Unit Tests
pytest tests/ -v

# Integration Tests
pytest tests/integration/ -v
```

### JavaScript/TypeScript Projects
```bash
# Syntax/Style
npm run lint && npm run type-check

# Unit Tests
npm test

# Integration Tests
npm run test:integration
```

## Common Issues

### PRP Generation Fails
- Ensure INITIAL.md is complete and specific
- Check that referenced examples exist
- Verify documentation URLs are accessible

### PRP Execution Fails
- Review validation commands - ensure they're correct
- Check that all dependencies are installed
- Verify file paths in the PRP are accurate

### AI Doesn't Follow PRP
- Add more specific examples
- Include more context about patterns
- Make success criteria more explicit
- Reference exact files and patterns to follow

---

**Remember**: A well-crafted PRP is the key to successful one-pass implementation with AI!
