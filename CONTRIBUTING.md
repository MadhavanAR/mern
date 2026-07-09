# Contributing to ChenAI Agents

Thank you for your interest in contributing to [ChenAI Agents](https://github.com/MadhavanAR/Agents)! This project is maintained by the [ChenAI Community](https://www.linkedin.com/company/chenai/).

## How to Contribute

### Reporting Issues

- Search [existing issues](https://github.com/MadhavanAR/Agents/issues) before opening a new one
- Include steps to reproduce, expected behavior, and actual behavior
- Mention which agent folder you are working with

### Pull Requests

1. Fork the repository
2. Create a feature branch: `git checkout -b feature/my-improvement`
3. Make your changes
4. Test locally before submitting
5. Open a pull request with a clear description of what changed and why

### Adding a New Agent

Each agent should be self-contained in its own folder with:

- `README.md` — setup, usage, prerequisites, and credentials
- `.env.example` — for Python agents (list all required environment variables)
- `requirements.txt` — for Python agents
- Workflow JSON file — for n8n agents

Follow the structure of existing agents in this repository.

### Documentation Standards

- Use ChenAI Agents branding and link back to the root README
- Include clone instructions pointing to `https://github.com/MadhavanAR/Agents`
- Document all required API keys and credentials
- Credit original authors when adapting existing work

### Code Style

- Python 3.11+ for Python agents
- Match the style of surrounding code in the agent you are editing
- Keep changes focused — one agent or fix per PR when possible

## Community

- [ChenAI Community on LinkedIn](https://www.linkedin.com/company/chenai/)
- [GitHub Issues](https://github.com/MadhavanAR/Agents/issues)

## License

By contributing, you agree that your contributions will be licensed under the [MIT License](LICENSE).
