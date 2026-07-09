# GitHub Repository Analysis Agent (Studio Variant)

> Production API variant of the GitHub analysis agent — reference implementation for FastAPI deployment.

Part of [ChenAI Agents](https://github.com/MadhavanAR/Agents) — open-source AI agent templates by the [ChenAI Community](https://www.linkedin.com/company/chenai/).

**Author:** [Cole Medin](https://www.youtube.com/@ColeMedin)

This is the studio-integration variant. For the standalone CLI version, see the [parent README](../../README.md).

## Quick Start

```bash
git clone https://github.com/MadhavanAR/Agents.git
cd Agents/github-agent/studio-integration-version/pydantic_ai_github_agent

python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
cp .env.example .env
# Edit .env with your API keys

python cli.py
```

## Files

| File | Description |
|------|-------------|
| `github_agent.py` | Core agent implementation |
| `cli.py` | Command-line interface |
| `requirements.txt` | Python dependencies |
| `.env.example` | Environment variable template |
| `../api/` | FastAPI endpoint variant |

## Contributing

Contributions are welcome! See [CONTRIBUTING.md](../../../CONTRIBUTING.md).

## License

Licensed under the [MIT License](../../../LICENSE).
