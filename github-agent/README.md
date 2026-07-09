# GitHub Repository Analysis Agent

> Analyze GitHub repositories — structure, files, and features — using Pydantic AI and the GitHub API.

Part of [ChenAI Agents](https://github.com/MadhavanAR/Agents) — open-source AI agent templates by the [ChenAI Community](https://www.linkedin.com/company/chenai/).

**Author:** [Cole Medin](https://www.youtube.com/@ColeMedin)

## Features

- Repository information retrieval (size, description, etc.)
- Directory structure analysis
- File content examination
- Support for OpenAI and OpenRouter models
- Available as both API endpoint and command-line interface

## Prerequisites

- Python 3.11+
- GitHub Personal Access Token (for private repositories)
- OpenRouter API key

## Quick Start

### 1. Clone the repository

```bash
git clone https://github.com/MadhavanAR/Agents.git
cd Agents/github-agent
```

### 2. Install dependencies

```bash
python -m venv venv
source venv/bin/activate   # Windows: venv\Scripts\activate
pip install -r requirements.txt
```

### 3. Configure environment

```bash
cp .env.example .env
```

Edit `.env` with your API keys:

```env
GITHUB_TOKEN=your_github_token          # Required for private repos
OPEN_ROUTER_API_KEY=your_openrouter_api_key
LLM_MODEL=deepseek/deepseek-chat        # Or your chosen model
SUPABASE_URL=your_supabase_url          # Only needed for API endpoint
SUPABASE_SERVICE_KEY=your_supabase_key  # Only needed for API endpoint
```

### 4. Run

**Command-line interface:**

```bash
python cli.py
```

**FastAPI endpoint:**

```bash
python github_agent_endpoint.py
```

The endpoint will be available at `http://localhost:8001`.

## Example Queries

- "What's the structure of repository https://github.com/username/repo?"
- "Show me the contents of the main Python file in https://github.com/username/repo"
- "What are the key features of repository https://github.com/username/repo?"

## Configuration

### LLM Models

Configure via the `LLM_MODEL` environment variable. The agent uses OpenRouter:

```env
LLM_MODEL=deepseek/deepseek-chat
```

### API Keys

- **GitHub Token** — [GitHub Settings](https://github.com/settings/tokens)
- **OpenRouter API Key** — [OpenRouter](https://openrouter.ai/)

## Files

| File | Description |
|------|-------------|
| `github_agent.py` | Core agent with GitHub API integration |
| `github_agent_endpoint.py` | FastAPI endpoint |
| `cli.py` | Command-line interface |
| `requirements.txt` | Python dependencies |
| `.env.example` | Environment variable template |
| `studio-integration-version/` | Production API variant reference |

## Error Handling

Built-in retries and error handling for invalid GitHub URLs, rate limiting, authentication issues, and file-not-found errors.

## Contributing

Contributions are welcome! See [CONTRIBUTING.md](../CONTRIBUTING.md).

## License

Licensed under the [MIT License](../LICENSE).
