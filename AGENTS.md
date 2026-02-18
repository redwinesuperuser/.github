# Agent Development Guide

This guide provides comprehensive technical information for AI coding agents working with the Awesome GitHub Copilot repository. It covers development workflows, setup commands, contribution standards, and best practices.

## 🏗️ Repository Structure

```plaintext
.
├── agents/              # Custom GitHub Copilot agents (.agent.md)
├── cookbook/            # Code snippets and examples
├── docs/                # Documentation for different resource types
├── instructions/        # Coding standards and best practices (.instructions.md)
├── plugins/             # Installable plugin bundles
├── prompts/             # Task-specific prompts (.prompt.md)
├── scripts/             # Maintenance and utility scripts
└── skills/              # Self-contained AI capabilities with bundled resources
```

## 🛠️ Development Setup

### Prerequisites

- Git installed and configured
- Text editor or IDE
- GitHub account with access to the repository

### Initial Setup

```bash
# Clone the repository
git clone https://github.com/github/awesome-copilot.git
cd awesome-copilot

# Create a new branch for your work
git checkout -b feature/your-feature-name
```

## 📝 File Naming Conventions

### Agents
- **Format**: `{name}.agent.md`
- **Example**: `code-reviewer.agent.md`
- **Location**: `/agents/`

### Prompts
- **Format**: `{name}.prompt.md`
- **Example**: `create-readme.prompt.md`
- **Location**: `/prompts/`

### Instructions
- **Format**: `{name}.instructions.md`
- **Example**: `python-testing.instructions.md`
- **Location**: `/instructions/`

### Skills
- **Format**: `{name}/` (directory)
- **Example**: `api-testing/`
- **Location**: `/skills/`

### Plugins
- **Format**: `{plugin-name}/README.md`
- **Example**: `awesome-copilot/README.md`
- **Location**: `/plugins/`

## 📋 Frontmatter Standards

All content files (agents, prompts, instructions) must include YAML frontmatter:

```yaml
---
title: "Descriptive Title"
description: "Clear, concise description of what this does"
tags: ["tag1", "tag2", "tag3"]
author: "Your Name or GitHub Handle"
version: "1.0.0"
---
```

### Required Fields
- `title`: Human-readable name
- `description`: Brief explanation of purpose
- `tags`: Array of relevant tags for discoverability

### Optional Fields
- `author`: Creator attribution
- `version`: Semantic version number
- `requires`: Dependencies or prerequisites
- `filePattern`: For instructions, the glob pattern to match files

## 🎯 Creating Different Content Types

### Creating a Custom Agent

1. Create a new file in `/agents/` with `.agent.md` extension
2. Add frontmatter with metadata
3. Write the agent instructions and capabilities
4. Include example usage
5. Test with GitHub Copilot

**Example Structure**:
```markdown
---
title: "Python Test Generator"
description: "Generates comprehensive unit tests for Python code"
tags: ["python", "testing", "pytest"]
author: "Your Name"
---

# Python Test Generator Agent

## Capabilities
- Generate pytest test cases
- Create test fixtures
- Mock external dependencies

## Instructions
[Detailed instructions for the agent]

## Examples
[Usage examples]
```

### Creating a Prompt

1. Create a new file in `/prompts/` with `.prompt.md` extension
2. Add frontmatter
3. Write the prompt template
4. Include parameters and examples

### Creating Instructions

1. Create a new file in `/instructions/` with `.instructions.md` extension
2. Add frontmatter with `filePattern` if applicable
3. Document coding standards and best practices
4. Provide examples

### Creating a Skill

1. Create a new directory in `/skills/`
2. Add an `instructions.md` file
3. Include any supporting files (templates, examples, etc.)
4. Create a README.md explaining the skill

### Creating a Plugin

1. Create a new directory in `/plugins/`
2. Create a `README.md` with plugin metadata and instructions
3. Reference the agents, prompts, and skills included
4. Document installation and usage

## 🔍 Testing Guidelines

### Manual Testing
1. Load the content in GitHub Copilot
2. Test with real-world scenarios
3. Verify all examples work as documented
4. Check that tags are appropriate

### Validation
- Ensure frontmatter is valid YAML
- Verify all links work
- Check for typos and formatting issues
- Confirm file naming follows conventions

## 📦 Pull Request Workflow

### Before Submitting

1. **Test your changes** thoroughly
2. **Update documentation** if needed
3. **Add yourself** to contributors (or request to be added)
4. **Verify formatting** matches repository standards

### PR Description Template

```markdown
## What does this PR do?
Brief description of the changes

## Type of contribution
- [ ] New agent
- [ ] New prompt
- [ ] New instruction
- [ ] New skill
- [ ] New plugin
- [ ] Bug fix
- [ ] Documentation
- [ ] Infrastructure

## Testing performed
- [ ] Tested with GitHub Copilot
- [ ] Verified examples work
- [ ] Checked links and references
- [ ] Validated frontmatter

## Related issues
Closes #(issue-number)
```

### After Submitting

1. Respond to review comments promptly
2. Make requested changes
3. Update the PR if needed
4. Be patient and professional

## 🏷️ Tagging Best Practices

Use clear, specific tags that help users discover your content:

### Language Tags
`python`, `javascript`, `typescript`, `go`, `rust`, `java`, `csharp`, `ruby`, `php`, `swift`, `kotlin`

### Framework Tags
`react`, `vue`, `angular`, `django`, `flask`, `express`, `spring`, `dotnet`, `rails`

### Domain Tags
`web`, `mobile`, `backend`, `frontend`, `devops`, `security`, `testing`, `documentation`, `api`, `database`

### Tool Tags
`docker`, `kubernetes`, `git`, `github-actions`, `terraform`, `ansible`, `jenkins`

## 🚨 Common Pitfalls

1. **Missing frontmatter**: All content files must have valid frontmatter
2. **Wrong file extension**: Use `.agent.md`, `.prompt.md`, or `.instructions.md`
3. **Unclear descriptions**: Make sure your description clearly explains what it does
4. **No testing**: Always test your contribution before submitting
5. **Too broad**: Focus on specific use cases rather than trying to do everything

## 🔐 Security Considerations

1. **Never include secrets** or credentials in any files
2. **Avoid hardcoded** sensitive information
3. **Review security implications** of generated code
4. **Follow security best practices** for your domain

## 📚 Resources

- [GitHub Copilot Documentation](https://docs.github.com/en/copilot)
- [Markdown Guide](https://www.markdownguide.org/)
- [YAML Specification](https://yaml.org/spec/)
- [Contributing Guidelines](CONTRIBUTING.md)

## 💬 Getting Help

- **Questions**: Open a discussion in the repository
- **Issues**: Report bugs or request features via GitHub Issues
- **Support**: See [SUPPORT.md](SUPPORT.md) for additional help

## 🎉 Recognition

Contributors are recognized using [All Contributors](https://allcontributors.org/). Your contributions will be celebrated with appropriate emojis:

- 🎭 Agents
- ⌨️ Prompts
- 🧭 Instructions
- 💻 Code
- 📖 Documentation
- 🎁 Plugins

Thank you for contributing to Awesome GitHub Copilot!
