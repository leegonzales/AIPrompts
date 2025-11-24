# Contributing to AI Prompts Library

Thank you for your interest in contributing! This library thrives on community contributions of production-tested, high-quality prompts.

## Quick Start

1. Fork the repository
2. Create a feature branch (`git checkout -b add-my-prompt`)
3. Add your prompt to the appropriate category
4. Commit your changes (`git commit -m 'feat: add {prompt-name}'`)
5. Push to your fork (`git push origin add-my-prompt`)
6. Open a Pull Request

## What Makes a Good Contribution

### Quality Criteria

Your prompt should be:

1. **Production-tested** - Actually used in real work, not theoretical
2. **Well-documented** - Clear purpose, use cases, and instructions
3. **Reusable** - Others can adapt it without deep customization
4. **Self-contained** - All necessary context included in the prompt
5. **Clean** - No hardcoded personal info, API keys, or organization-specific details

### Contribution Types

We welcome:

- **New prompts** - Add to existing categories or propose new ones
- **Improvements** - Enhance existing prompts with better structure or clarity
- **Examples** - Real-world usage examples in the `examples/` directory
- **Documentation** - Better explanations, use cases, or guides
- **Bug fixes** - Corrections to existing prompts or docs

## Prompt Format Guidelines

### File Naming

- Use kebab-case: `my-prompt-name.md`
- Be descriptive but concise
- Use `.md` extension for all prompt files

### File Structure

Each prompt file should include:

```markdown
# [Prompt Name]

## Purpose
Brief 1-2 sentence description of what this prompt does.

## Use Cases
- When to use this prompt
- What problems it solves
- Who it's for

## Instructions
1. How to use the prompt
2. Any customization needed
3. Expected output format

## The Prompt

[The actual prompt content starts here]
...
```

### System Prompts

If your prompt includes a system role or persona:

```markdown
<ROLE: SYSTEM>
[System instructions here]
```

or

```markdown
You are a [role description]...
```

## Directory Structure

Place your prompt in the appropriate category:

```
prompts/
├── writing-and-style/          # Writing analysis, style guides
├── coaching-and-training/      # Educational, skill development
├── analysis-and-strategy/      # Business analysis, planning
├── workflow-and-productivity/  # Process optimization, tools
└── [your-new-category]/        # Propose new categories as needed
```

### Creating New Categories

If your prompt doesn't fit existing categories:

1. Create a new directory in `prompts/`
2. Add a `README.md` in that directory explaining the category
3. Update the main `README.md` to reference the new category

## Commit Guidelines

Follow [Conventional Commits](https://www.conventionalcommits.org/):

- `feat:` - New prompt or major enhancement
- `fix:` - Bug fix or correction
- `docs:` - Documentation only
- `refactor:` - Restructuring without changing functionality
- `chore:` - Maintenance tasks

Examples:
```bash
git commit -m "feat: add context-continuity prompt"
git commit -m "fix: correct WritingAnalyzer system role"
git commit -m "docs: improve README usage section"
```

## Pull Request Process

1. **Title**: Clear, descriptive title following conventional commits
2. **Description**: Explain what the prompt does and why it's valuable
3. **Testing**: Confirm you've tested the prompt with real LLMs
4. **Documentation**: Update README.md if adding new categories
5. **Review**: Be responsive to feedback and questions

### PR Template

```markdown
## Type of Change
- [ ] New prompt
- [ ] Enhancement to existing prompt
- [ ] Documentation
- [ ] Bug fix

## Description
[What does this prompt do? What problem does it solve?]

## Testing
- [ ] Tested with GPT-4
- [ ] Tested with Claude
- [ ] Tested with other models: [specify]

## Additional Context
[Any relevant context, screenshots, or examples]
```

## Code of Conduct

### Our Standards

- Be respectful and inclusive
- Provide constructive feedback
- Focus on what's best for the community
- Show empathy towards others

### Unacceptable Behavior

- Harassment or discriminatory language
- Trolling or inflammatory comments
- Publishing others' private information
- Other conduct that's unprofessional

## Questions?

- Open an issue for questions about contributing
- Tag it with `question` or `help wanted`
- We'll respond within a few days

## Recognition

Contributors will be acknowledged in:
- Git commit history
- Future CONTRIBUTORS.md file
- Special thanks in release notes for significant contributions

## License

By contributing, you agree that your contributions will be licensed under the MIT License, the same as the rest of the project.

---

Thank you for helping make this library more valuable for everyone!
