# 🤖 Awesome GitHub Copilot
[![Powered by Awesome Copilot](https://img.shields.io/badge/Powered_by-Awesome_Copilot-blue?logo=githubcopilot)](https://aka.ms/awesome-github-copilot) [![GitHub contributors from allcontributors.org](https://img.shields.io/github/all-contributors/github/awesome-copilot?color=ee8449)](#contributors-)


A community created collection of custom agents, prompts, and instructions to supercharge your GitHub Copilot experience across different domains, languages, and use cases.

## 🚀 What is Awesome GitHub Copilot?

This repository provides a comprehensive toolkit for enhancing GitHub Copilot with specialized:

- **👉 [Awesome Agents](docs/README.agents.md)** - Specialized GitHub Copilot agents that integrate with MCP servers to provide enhanced capabilities for specific workflows and tools
- **👉 [Awesome Prompts](docs/README.prompts.md)** - Focused, task-specific prompts for generating code, documentation, and solving specific problems
- **👉 [Awesome Instructions](docs/README.instructions.md)** - Comprehensive coding standards and best practices that apply to specific file patterns or entire projects
- **👉 [Awesome Hooks](docs/README.hooks.md)** - Automated workflows triggered by specific events during development, testing, and deployment
- **👉 [Awesome Skills](docs/README.skills.md)** - Self-contained folders with instructions and bundled resources that enhance AI capabilities for specialized tasks
- **👉 [Awesome Plugins](docs/README.plugins.md)** - Curated plugins of related prompts, agents, and skills organized around specific themes and workflows
- **👉 [Awesome Cookbook Recipes](cookbook/README.md)** - Practical, copy-paste-ready code snippets and real-world examples for working with GitHub Copilot tools and features

## 🌟 Featured Plugins

Discover our curated plugins of prompts, agents, and skills organized around specific themes and workflows.

| Name | Description | Items | Tags |
| ---- | ----------- | ----- | ---- |
| [Awesome Copilot](plugins/awesome-copilot/README.md) | Meta prompts that help you discover and generate curated GitHub Copilot agents, collections, instructions, prompts, and skills. | 5 items | github-copilot, discovery, meta, prompt-engineering, agents |
| [Copilot SDK](plugins/copilot-sdk/README.md) | Build applications with the GitHub Copilot SDK across multiple programming languages. Includes comprehensive instructions for C#, Go, Node.js/TypeScript, and Python to help you create AI-powered applications. | 5 items | copilot-sdk, sdk, csharp, go, nodejs, typescript, python, ai, github-copilot |
| [Partners](plugins/partners/README.md) | Custom agents that have been created by GitHub partners | 20 items | devops, security, database, cloud, infrastructure, observability, feature-flags, cicd, migration, performance |


## How to Install Customizations

To make it easy to add these customizations to your editor, we have created an [MCP Server](https://developer.microsoft.com/blog/announcing-awesome-copilot-mcp-server) that provides a prompt for searching and installing prompts, instructions, agents, and skills directly from this repository. You'll need to have Docker installed and running to run the MCP server locally.

[![Install in VS Code](https://img.shields.io/badge/VS_Code-Install-0098FF?logo=visualstudiocode&logoColor=white)](https://aka.ms/awesome-copilot/mcp/vscode) [![Install in VS Code Insiders](https://img.shields.io/badge/VS_Code_Insiders-Install-24bfa5?logo=visualstudiocode&logoColor=white)](https://aka.ms/awesome-copilot/mcp/vscode-insiders) [![Install in Visual Studio](https://img.shields.io/badge/Visual_Studio-Install-C16FDE?logo=visualstudio&logoColor=white)](https://aka.ms/awesome-copilot/mcp/vs)

<details>
<summary>Show MCP Server JSON configuration</summary>

```json
{
  "servers": {
    "awesome-copilot": {
      "type": "stdio",
      "command": "docker",
      "args": [
        "run",
        "-i",
        "--rm",
        "ghcr.io/microsoft/mcp-dotnet-samples/awesome-copilot:latest"
      ]
    }
  }
}
```

</details>

## 📄 llms.txt

An [`llms.txt`](https://github.github.io/awesome-copilot/llms.txt) file following the [llmstxt.org](https://llmstxt.org/) specification is available on the GitHub Pages site. This machine-readable file makes it easy for Large Language Models to discover and understand all available agents, prompts, instructions, and skills, providing a structured overview of the repository's resources with names and descriptions.

## 🔧 How to Use

### 🔌 Plugins

Plugins are installable packages that bundle related agents, commands (prompts), and skills, making it easy to install a curated set of resources.

#### Installing Plugins

First, add the Awesome Copilot marketplace to your Copilot CLI:

```bash
copilot plugin marketplace add github/awesome-copilot
```

Then install any plugin:

```bash
copilot plugin install <plugin-name>@awesome-copilot
```

Alternatively, you can use the `/plugin` command within a Copilot chat session to browse and install plugins interactively.

### 🤖 Custom Agents

Custom agents can be used in Copilot coding agent (CCA), VS Code, and Copilot CLI (coming soon). For CCA, when assigning an issue to Copilot, select the custom agent from the provided list. In VS Code, you can activate the custom agent in the agents session, alongside built-in agents like Plan and Agent.

### 🎯 Prompts

Use the `/` command in GitHub Copilot Chat to access prompts:

```plaintext
/awesome-copilot create-readme
```

### 📋 Instructions

Instructions automatically apply to files based on their patterns and provide contextual guidance for coding standards, frameworks, and best practices.

### 🪝 Hooks

Hooks enable automated workflows triggered by specific events during GitHub Copilot coding agent sessions (like sessionStart, sessionEnd, userPromptSubmitted). They can automate tasks like logging, auto-committing changes, or integrating with external services.

## 🎯 Why Use Awesome GitHub Copilot?

- **Productivity**: Pre-built agents, prompts and instructions save time and provide consistent results.
- **Best Practices**: Benefit from community-curated coding standards and patterns.
- **Specialized Assistance**: Access expert-level guidance through specialized custom agents.
- **Continuous Learning**: Stay updated with the latest patterns and practices across technologies.

## 🤝 Contributing

We welcome contributions! Please see our [Contributing Guidelines](CONTRIBUTING.md) for details on how to:

- Add new prompts, instructions, hooks, agents, or skills
- Improve existing content
- Report issues or suggest enhancements

For AI coding agents working with this project, refer to [AGENTS.md](AGENTS.md) for detailed technical guidance on development workflows, setup commands, and contribution standards.

### Quick Contribution Guide

1. Follow our file naming conventions and frontmatter requirements
2. Test your contributions thoroughly
3. Update the appropriate README tables
4. Submit a pull request with a clear description

## 📖 Repository Structure

```plaintext
├── prompts/          # Task-specific prompts (.prompt.md)
├── instructions/     # Coding standards and best practices (.instructions.md)
├── agents/           # AI personas and specialized modes (.agent.md)
├── plugins/          # Installable plugins bundling related items
├── scripts/          # Utility scripts for maintenance
└── skills/           # AI capabilities for specialized tasks
```

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🛡️ Security & Support

- **Security Issues**: Please see our [Security Policy](SECURITY.md)
- **Support**: Check our [Support Guide](SUPPORT.md) for getting help
- **Code of Conduct**: We follow the [Contributor Covenant](CODE_OF_CONDUCT.md)

## ℹ️ Disclaimer

The customizations in this repository are sourced from and created by third-party developers. GitHub does not verify, endorse, or guarantee the functionality or security of these agents. Please carefully inspect any agent and its documentation before installing to understand permissions it may require and actions it may perform.

---

**Ready to supercharge your coding experience?** Start exploring our [prompts](docs/README.prompts.md), [instructions](docs/README.instructions.md), [hooks](docs/README.hooks.md), and [custom agents](docs/README.agents.md)!

## Contributors ✨

Thanks goes to these wonderful people ([emoji key](./CONTRIBUTING.md#contributors-recognition)):

<!-- ALL-CONTRIBUTORS-LIST:START - Do not remove or modify this section -->
<!-- prettier-ignore-start -->
<!-- markdownlint-disable -->
<table>
  <tbody>
    <tr>
      <td align="center" valign="top" width="14.28%"><a href="https://www.aaron-powell.com/"><img src="https://avatars.githubusercontent.com/u/434140?v=4?s=100" width="100px;" alt="Aaron Powell"/><br /><sub><b>Aaron Powell</b></sub></a><br /><a href="#agents-aaronpowell" title="Specialized agents for GitHub Copilot">🎭</a> <a href="https://github.com/github/awesome-copilot/commits?author=aaronpowell" title="Code">💻</a> <a href="#plugins-aaronpowell" title="Curated plugins of related content">🎁</a> <a href="https://github.com/github/awesome-copilot/commits?author=aaronpowell" title="Documentation">📖</a> <a href="#infra-aaronpowell" title="Infrastructure (Hosting, Build-Tools, etc)">🚇</a> <a href="#instructions-aaronpowell" title="Custom instructions for GitHub Copilot">🧭</a> <a href="#maintenance-aaronpowell" title="Maintenance">🚧</a> <a href="#prompts-aaronpowell" title="Reusable prompts for GitHub Copilot">⌨️</a></td>
      <td align="center" valign="top" width="14.28%"><a href="https://codemilltech.com/"><img src="https://avatars.githubusercontent.com/u/2053639?v=4?s=100" width="100px;" alt="Matt Soucoup"/><br /><sub><b>Matt Soucoup</b></sub></a><br /><a href="#infra-codemillmatt" title="Infrastructure (Hosting, Build-Tools, etc)">🚇</a></td>
      <td align="center" valign="top" width="14.28%"><a href="https://www.buymeacoffee.com/troystaylor"><img src="https://avatars.githubusercontent.com/u/44444967?v=4?s=100" width="100px;" alt="Troy Simeon Taylor"/><br /><sub><b>Troy Simeon Taylor</b></sub></a><br /><a href="#agents-troystaylor" title="Specialized agents for GitHub Copilot">🎭</a> <a href="#plugins-troystaylor" title="Curated plugins of related content">🎁</a> <a href="#instructions-troystaylor" title="Custom instructions for GitHub Copilot">🧭</a> <a href="#prompts-troystaylor" title="Reusable prompts for GitHub Copilot">⌨️</a></td>
      <td align="center" valign="top" width="14.28%"><a href="https://github.com/abbas133"><img src="https://avatars.githubusercontent.com/u/7757139?v=4?s=100" width="100px;" alt="Abbas"/><br /><sub><b>Abbas</b></sub></a><br /><a href="#agents-abbas133" title="Specialized agents for GitHub Copilot">🎭</a> <a href="#instructions-abbas133" title="Custom instructions for GitHub Copilot">🧭</a></td>
      <td align="center" valign="top" width="14.28%"><a href="https://calva.io/"><img src="https://avatars.githubusercontent.com/u/30010?v=4?s=100" width="100px;" alt="Peter Strömberg"/><br /><sub><b>Peter Strömberg</b></sub></a><br /><a href="#agents-PEZ" title="Specialized agents for GitHub Copilot">🎭</a> <a href="#plugins-PEZ" title="Curated plugins of related content">🎁</a> <a href="#instructions-PEZ" title="Custom instructions for GitHub Copilot">🧭</a> <a href="#prompts-PEZ" title="Reusable prompts for GitHub Copilot">⌨️</a></td>
      <td align="center" valign="top" width="14.28%"><a href="https://danielscottraynsford.com/"><img src="https://avatars.githubusercontent.com/u/7589164?v=4?s=100" width="100px;" alt="Daniel Scott-Raynsford"/><br /><sub><b>Daniel Scott-Raynsford</b></sub></a><br /><a href="#agents-PlagueHO" title="Specialized agents for GitHub Copilot">🎭</a> <a href="#plugins-PlagueHO" title="Curated plugins of related content">🎁</a> <a href="#instructions-PlagueHO" title="Custom instructions for GitHub Copilot">🧭</a> <a href="#prompts-PlagueHO" title="Reusable prompts for GitHub Copilot">⌨️</a></td>
      <td align="center" valign="top" width="14.28%"><a href="https://github.com/jhauga"><img src="https://avatars.githubusercontent.com/u/10998676?v=4?s=100" width="100px;" alt="John Haugabook"/><br /><sub><b>John Haugabook</b></sub></a><br /><a href="#instructions-jhauga" title="Custom instructions for GitHub Copilot">🧭</a> <a href="#prompts-jhauga" title="Reusable prompts for GitHub Copilot">⌨️</a></td>
    </tr>
    <tr>
      <td align="center" valign="top" width="14.28%"><a href="https://witter.cz/@pavel"><img src="https://avatars.githubusercontent.com/u/7853836?v=4?s=100" width="100px;" alt="Pavel Simsa"/><br /><sub><b>Pavel Simsa</b></sub></a><br /><a href="https://github.com/github/awesome-copilot/commits?author=psimsa" title="Code">💻</a></td>
      <td align="center" valign="top" width="14.28%"><a href="http://digitarald.de/"><img src="https://avatars.githubusercontent.com/u/8599?v=4?s=100" width="100px;" alt="Harald Kirschner"/><br /><sub><b>Harald Kirschner</b></sub></a><br /><a href="https://github.com/github/awesome-copilot/commits?author=digitarald" title="Code">💻</a> <a href="https://github.com/github/awesome-copilot/commits?author=digitarald" title="Documentation">📖</a> <a href="#maintenance-digitarald" title="Maintenance">🚧</a></td>
      <td align="center" valign="top" width="14.28%"><a href="https://mubaidr.js.org/"><img src="https://avatars.githubusercontent.com/u/2222702?v=4?s=100" width="100px;" alt="Muhammad Ubaid Raza"/><br /><sub><b>Muhammad Ubaid Raza</b></sub></a><br /><a href="#agents-mubaidr" title="Specialized agents for GitHub Copilot">🎭</a> <a href="#instructions-mubaidr" title="Custom instructions for GitHub Copilot">🧭</a></td>
      <td align="center" valign="top" width="14.28%"><a href="https://github.com/tmeschter"><img src="https://avatars.githubusercontent.com/u/10506730?v=4?s=100" width="100px;" alt="Tom Meschter"/><br /><sub><b>Tom Meschter</b></sub></a><br /><a href="https://github.com/github/awesome-copilot/commits?author=tmeschter" title="Code">💻</a></td>
      <td align="center" valign="top" width="14.28%"><a href="https://www.aungmyokyaw.com/"><img src="https://avatars.githubusercontent.com/u/9404824?v=4?s=100" width="100px;" alt="Aung Myo Kyaw"/><br /><sub><b>Aung Myo Kyaw</b></sub></a><br /><a href="#agents-AungMyoKyaw" title="Specialized agents for GitHub Copilot">🎭</a> <a href="#prompts-AungMyoKyaw" title="Reusable prompts for GitHub Copilot">⌨️</a></td>
      <td align="center" valign="top" width="14.28%"><a href="https://github.com/JasonYeMSFT"><img src="https://avatars.githubusercontent.com/u/39359541?v=4?s=100" width="100px;" alt="JasonYeMSFT"/><br /><sub><b>JasonYeMSFT</b></sub></a><br /><a href="https://github.com/github/awesome-copilot/commits?author=JasonYeMSFT" title="Code">💻</a></td>
      <td align="center" valign="top" width="14.28%"><a href="https://www.linkedin.com/in/jrc356/"><img src="https://avatars.githubusercontent.com/u/37387479?v=4?s=100" width="100px;" alt="Jon Corbin"/><br /><sub><b>Jon Corbin</b></sub></a><br /><a href="#agents-Jrc356" title="Specialized agents for GitHub Copilot">🎭</a> <a href="#prompts-Jrc356" title="Reusable prompts for GitHub Copilot">⌨️</a></td>
    </tr>
    <tr>
      <td align="center" valign="top" width="14.28%"><a href="https://github.com/troytaylor-msft"><img src="https://avatars.githubusercontent.com/u/248058374?v=4?s=100" width="100px;" alt="troytaylor-msft"/><br /><sub><b>troytaylor-msft</b></sub></a><br /><a href="https://github.com/github/awesome-copilot/commits?author=troytaylor-msft" title="Code">💻</a></td>
      <td align="center" valign="top" width="14.28%"><a href="https://delatorre.dev/"><img src="https://avatars.githubusercontent.com/u/38289677?v=4?s=100" width="100px;" alt="Emerson Delatorre"/><br /><sub><b>Emerson Delatorre</b></sub></a><br /><a href="#instructions-fazedordecodigo" title="Custom instructions for GitHub Copilot">🧭</a></td>
      <td align="center" valign="top" width="14.28%"><a href="https://github.com/burkeholland"><img src="https://avatars.githubusercontent.com/u/686963?v=4?s=100" width="100px;" alt="Burke Holland"/><br /><sub><b>Burke Holland</b></sub></a><br /><a href="#agents-burkeholland" title="Specialized agents for GitHub Copilot">🎭</a> <a href="#infra-burkeholland" title="Infrastructure (Hosting, Build-Tools, etc)">🚇</a> <a href="#instructions-burkeholland" title="Custom instructions for GitHub Copilot">🧭</a> <a href="#prompts-burkeholland" title="Reusable prompts for GitHub Copilot">⌨️</a></td>
      <td align="center" valign="top" width="14.28%"><a href="https://yaooqinn.github.io/"><img src="https://avatars.githubusercontent.com/u/8326978?v=4?s=100" width="100px;" alt="Kent Yao"/><br /><sub><b>Kent Yao</b></sub></a><br /><a href="#instructions-yaooqinn" title="Custom instructions for GitHub Copilot">🧭</a> <a href="#prompts-yaooqinn" title="Reusable prompts for GitHub Copilot">⌨️</a></td>
      <td align="center" valign="top" width="14.28%"><a href="https://www.devprodlogs.com/"><img src="https://avatars.githubusercontent.com/u/51440732?v=4?s=100" width="100px;" alt="Daniel Meppiel"/><br /><sub><b>Daniel Meppiel</b></sub></a><br /><a href="#prompts-danielmeppiel" title="Reusable prompts for GitHub Copilot">⌨️</a></td>
      <td align="center" valign="top" width="14.28%"><a href="https://github.com/yeelam-gordon"><img src="https://avatars.githubusercontent.com/u/73506701?v=4?s=100" width="100px;" alt="Gordon Lam"/><br /><sub><b>Gordon Lam</b></sub></a><br /><a href="#instructions-yeelam-gordon" title="Custom instructions for GitHub Copilot">🧭</a></td>
      <td align="center" valign="top" width="14.28%"><a href="https://www.madskristensen.net/"><img src="https://avatars.githubusercontent.com/u/1258877?v=4?s=100" width="100px;" alt="Mads Kristensen"/><br /><sub><b>Mads Kristensen</b></sub></a><br /><a href="#instructions-madskristensen" title="Custom instructions for GitHub Copilot">🧭</a></td>
    </tr>
    <tr>
      <td align="center" valign="top" width="14.28%"><a href="https://ks6088ts.github.io/"><img src="https://avatars.githubusercontent.com/u/1254960?v=4?s=100" width="100px;" alt="Shinji Takenaka"/><br /><sub><b>Shinji Takenaka</b></sub></a><br /><a href="https://github.com/github/awesome-copilot/commits?author=ks6088ts" title="Code">💻</a></td>
      <td align="center" valign="top" width="14.28%"><a href="https://github.com/spectatora"><img src="https://avatars.githubusercontent.com/u/1385755?v=4?s=100" width="100px;" alt="spectatora"/><br /><sub><b>spectatora</b></sub></a><br /><a href="#agents-spectatora" title="Specialized agents for GitHub Copilot">🎭</a> <a href="https://github.com/github/awesome-copilot/commits?author=spectatora" title="Code">💻</a> <a href="#maintenance-spectatora" title="Maintenance">🚧</a></td>
      <td align="center" valign="top" width="14.28%"><a href="https://github.com/sinedied"><img src="https://avatars.githubusercontent.com/u/593151?v=4?s=100" width="100px;" alt="Yohan Lasorsa"/><br /><sub><b>Yohan Lasorsa</b></sub></a><br /><a href="#instructions-sinedied" title="Custom instructions for GitHub Copilot">🧭</a> <a href="#prompts-sinedied" title="Reusable prompts for GitHub Copilot">⌨️</a></td>
      <td align="center" valign="top" width="14.28%"><a href="https://github.com/VamshiVerma"><img src="https://avatars.githubusercontent.com/u/21999324?v=4?s=100" width="100px;" alt="Vamshi Verma"/><br /><sub><b>Vamshi Verma</b></sub></a><br /><a href="#instructions-VamshiVerma" title="Custom instructions for GitHub Copilot">🧭</a> <a href="#prompts-VamshiVerma" title="Reusable prompts for GitHub Copilot">⌨️</a></td>
      <td align="center" valign="top" width="14.28%"><a href="https://montemagno.com/"><img src="https://avatars.githubusercontent.com/u/1676321?v=4?s=100" width="100px;" alt="James Montemagno"/><br /><sub><b>James Montemagno</b></sub></a><br /><a href="#instructions-jamesmontemagno" title="Custom instructions for GitHub Copilot">🧭</a> <a href="#prompts-jamesmontemagno" title="Reusable prompts for GitHub Copilot">⌨️</a></td>
    </tr>
  </tbody>
</table>

<!-- markdownlint-restore -->
<!-- prettier-ignore-end -->

<!-- ALL-CONTRIBUTORS-LIST:END -->