# Contributing to Awesome GitHub Copilot

Thank you for your interest in contributing to Awesome GitHub Copilot! This guide will help you get started with contributing prompts, instructions, agents, skills, and plugins to the repository.

## 🚀 Quick Start

1. Fork this repository
2. Create a new branch for your contribution
3. Add your content following our guidelines below
4. Test your contribution
5. Submit a pull request

## 📝 What Can You Contribute?

### Custom Agents
Specialized AI agents that integrate with MCP servers to provide enhanced capabilities for specific workflows.

**Location**: `/agents/`  
**Extension**: `.agent.md`

### Prompts
Focused, task-specific prompts for generating code, documentation, and solving specific problems.

**Location**: `/prompts/`  
**Extension**: `.prompt.md`

### Instructions
Comprehensive coding standards and best practices that apply to specific file patterns or entire projects.

**Location**: `/instructions/`  
**Extension**: `.instructions.md`

### Skills
Self-contained folders with instructions and bundled resources that enhance AI capabilities for specialized tasks.

**Location**: `/skills/`  
**Structure**: Each skill is a folder containing its files and instructions

### Plugins
Curated collections of related prompts, agents, and skills organized around specific themes and workflows.

**Location**: `/plugins/`  
**Structure**: Each plugin is a folder with a README.md

## 📋 Contribution Guidelines

### File Naming Conventions

- **Agents**: `{name}.agent.md`
- **Prompts**: `{name}.prompt.md`
- **Instructions**: `{name}.instructions.md`
- **Skills**: `{name}/` (folder)
- **Plugins**: `{plugin-name}/README.md`

Use kebab-case for file and folder names (e.g., `create-readme.prompt.md`, `python-best-practices.instructions.md`).

### Frontmatter Requirements

All agents, prompts, and instructions must include frontmatter with metadata:

```yaml
---
title: "Your Title"
description: "A brief description"
tags: ["tag1", "tag2", "tag3"]
author: "Your Name"
---
```

### Quality Standards

1. **Clear and Concise**: Make your content easy to understand
2. **Well-Documented**: Include examples and usage instructions
3. **Tested**: Ensure your contribution works as expected
4. **Specific**: Focus on solving a particular problem or use case
5. **Secure**: Don't include sensitive information or credentials

### Testing Your Contribution

Before submitting a pull request:

1. Test your agent, prompt, or instruction with GitHub Copilot
2. Verify all links and references work correctly
3. Ensure frontmatter is properly formatted
4. Check for typos and grammatical errors

## 🔍 Pull Request Process

1. **Create a Descriptive Title**: Use a clear, concise title for your PR
2. **Provide Context**: Explain what you're adding and why it's useful
3. **Link Related Issues**: Reference any related issues or discussions
4. **Be Responsive**: Respond to feedback and requested changes promptly

### PR Template

```markdown
## Description
Brief description of what this PR adds

## Type of Contribution
- [ ] Agent
- [ ] Prompt
- [ ] Instruction
- [ ] Skill
- [ ] Plugin
- [ ] Documentation
- [ ] Bug fix

## Testing
How have you tested this contribution?

## Related Issues
Closes #(issue number)
```

## 🏷️ Tags and Categories

Use appropriate tags to help users discover your content:

- **Languages**: `python`, `javascript`, `typescript`, `go`, `rust`, `java`, `csharp`, etc.
- **Frameworks**: `react`, `vue`, `angular`, `django`, `flask`, `express`, etc.
- **Tools**: `docker`, `kubernetes`, `git`, `github-actions`, etc.
- **Domains**: `web`, `mobile`, `devops`, `security`, `testing`, `documentation`, etc.

## 🤝 Code of Conduct

This project follows the [Contributor Covenant Code of Conduct](CODE_OF_CONDUCT.md). By participating, you are expected to uphold this code.

## 📖 Additional Resources

- [GitHub Copilot Documentation](https://docs.github.com/en/copilot)
- [Awesome GitHub Copilot README](README.md)
- [Agent Development Guide](AGENTS.md)

## 💡 Need Help?

- Check our [Support Guide](SUPPORT.md)
- Open an issue for questions or suggestions
- Join community discussions

## Contributors Recognition

We use [All Contributors](https://allcontributors.org/) to recognize all contributors. When you make a contribution, you'll be added to our contributors list with the appropriate emoji based on your contribution type:

- 🎭 Agents
- ⌨️ Prompts
- 🧭 Instructions
- 🎁 Plugins
- 💻 Code
- 📖 Documentation
- 🚇 Infrastructure
- 🚧 Maintenance

Thank you for contributing to Awesome GitHub Copilot! 🎉
