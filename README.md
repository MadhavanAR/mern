<p align="center">
  <h1 align="center">ChenAI Agents</h1>
  <p align="center">
    Open-source AI agent templates for research, automation, and business workflows
    <br />
    <a href="https://www.linkedin.com/company/chenai/"><strong>ChenAI Community »</strong></a>
    <br />
    <br />
    <a href="#quick-start">Quick Start</a>
    ·
    <a href="#agents">Browse Agents</a>
    ·
    <a href="#contributing">Contribute</a>
    ·
    <a href="https://github.com/MadhavanAR/Agents/issues">Report Bug</a>
  </p>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.11+-3776AB?style=flat&logo=python&logoColor=white" alt="Python 3.11+" />
  <img src="https://img.shields.io/badge/n8n-Workflows-EA4B71?style=flat&logo=n8n&logoColor=white" alt="n8n" />
  <img src="https://img.shields.io/badge/Pydantic_AI-Agents-5C6BC0?style=flat" alt="Pydantic AI" />
  <img src="https://img.shields.io/badge/Open%20Source-Community-2ea44f?style=flat" alt="Open Source" />
</p>

---

## About

**ChenAI Agents** is an open-source collection of production-ready AI agent templates built by the [ChenAI Community](https://www.linkedin.com/company/chenai/). Each agent is a self-contained project you can clone, configure, and run — whether you need web research, GitHub analysis, document RAG, n8n automation, or content creation.

Use these agents as:

- **Starting points** for your own AI products and internal tools
- **Reference implementations** for Pydantic AI, n8n, FastAPI, and Supabase patterns
- **Learning resources** for building intelligent automation

Contributions, issues, and stars are welcome. This project grows through community collaboration.

---

## Agents

### Pydantic AI Agents (Python)

| Agent | Description | Docs |
|-------|-------------|------|
| [GitHub Agent](./pydantic-github-agent/) | Analyze GitHub repos — structure, files, and features via the GitHub API | [README](./pydantic-github-agent/README.md) |
| [Advanced Web Researcher](./pydantic-ai-advanced-researcher/) | Web search agent powered by Brave Search API | [README](./pydantic-ai-advanced-researcher/README.md) |
| [Documentation Crawler & RAG](./crawl4AI-agent/) | Crawl docs, embed in Supabase, and answer questions with RAG | [README](./crawl4AI-agent/README.md) |
| [File Agent](./file-agent/) | FastAPI agent with file upload, storage, and AI context integration | [README](./file-agent/README.md) |

### n8n Workflow Agents

| Agent | Description | Docs |
|-------|-------------|------|
| [n8n Expert](./n8n-expert/) | Find and understand n8n automation workflows from natural language | [README](./n8n-expert/README.md) |
| [GitHub Assistant](./n8n-github-assistant/) | GitHub-focused automation assistant | [README](./n8n-github-assistant/README.md) |
| [Advanced Web Researcher](./advanced-web-researcher/) | Deep web research with Brave Search and AI summarization | [README](./advanced-web-researcher/README.md) |
| [YouTube Video Summarizer](./youtube-video-summarizer/) | Summarize YouTube videos and chat about their content | [README](./youtube-video-summarizer/README.md) |
| [Tech Stack Expert](./tech-stack-expert/) | Get recommendations and guidance on technology choices | [README](./tech-stack-expert/README.md) |
| [Local AI Expert](./local-ai-expert/) | Guidance on running AI models locally | [README](./local-ai-expert/README.md) |
| [bolt.diy Expert](./bolt.diy-expert/) | Expert assistant for bolt.diy development | [README](./bolt.diy-expert/README.md) |
| [Content Creator](./linkedin-x-blog-content-creator/) | Generate LinkedIn, X, and blog content | [README](./linkedin-x-blog-content-creator/README.md) |
| [Small Business Researcher](./small-business-researcher/) | Research small business topics from Reddit discussions | [README](./small-business-researcher/README.md) |

### Templates & Integrations

| Project | Description | Docs |
|---------|-------------|------|
| [Sample Python Agent](./~sample-python-agent~/) | Minimal FastAPI + Supabase agent template | [README](./~sample-python-agent~/README.md) |
| [Sample n8n Agent](./~sample-n8n-agent~/) | Base n8n agent workflow template | [README](./~sample-n8n-agent~/README.md) |
| [Base Python Docker](./base_python_docker/) | Docker image for deploying Python agents | [README](./base_python_docker/README.md) |
| [Voiceflow Integration](./~voiceflow-dialog-api-integration~/) | Connect agents to Voiceflow Dialog API | [README](./~voiceflow-dialog-api-integration~/README.md) |

---

## Quick Start

### 1. Clone the repository

```bash
git clone https://github.com/MadhavanAR/Agents.git
cd Agents
```

### 2. Pick an agent

Choose an agent from the table above and `cd` into its directory.

### 3. Configure environment

Most Python agents include a `.env.example` file:

```bash
cp .env.example .env
# Edit .env with your API keys (OpenAI, Supabase, GitHub, etc.)
```

### 4. Install and run

**Python agents:**

```bash
python -m venv venv
source venv/bin/activate   # Windows: venv\Scripts\activate
pip install -r requirements.txt
python cli.py              # or the agent's main entry point
```

**n8n agents:**

Import the `*.json` workflow file into your n8n instance and configure credentials as described in each agent's README.

---

## Project Structure

```
Agents/
├── pydantic-github-agent/       # GitHub repo analysis (Pydantic AI)
├── pydantic-ai-advanced-researcher/
├── crawl4AI-agent/              # Doc crawler + RAG
├── file-agent/
├── n8n-expert/
├── advanced-web-researcher/
├── youtube-video-summarizer/
├── ~sample-python-agent~/       # Starter templates
├── ~sample-n8n-agent~/
├── base_python_docker/
└── README.md
```

Each agent folder is self-contained with its own `README.md`, dependencies, and configuration.

---

## Prerequisites

Requirements vary by agent. Common dependencies include:

| Tool | Used for |
|------|----------|
| Python 3.11+ | Pydantic AI and FastAPI agents |
| [n8n](https://n8n.io/) | Workflow-based agents |
| [Supabase](https://supabase.com/) | Vector storage and conversation history |
| OpenAI / OpenRouter / Brave API | LLM and search capabilities |

Check each agent's README for specific requirements.

---

## Contributing

We welcome contributions from the community. Here's how to get started:

1. **Fork** the repository
2. **Create a branch** for your feature or fix (`git checkout -b feature/my-new-agent`)
3. **Add or improve an agent** — include a clear README with setup steps
4. **Test locally** before opening a PR
5. **Open a Pull Request** with a description of what you changed and why

### Contribution ideas

- New agent templates (Python, n8n, or other frameworks)
- Bug fixes and documentation improvements
- Better error handling and examples
- Translations and tutorials

Please keep each agent self-contained and document all required environment variables.

---

## Community

- **ChenAI Community** — [LinkedIn](https://www.linkedin.com/company/chenai/)
- **Issues** — [GitHub Issues](https://github.com/MadhavanAR/Agents/issues)
- **Discussions** — Use GitHub Discussions for questions and ideas (enable in repo settings)

---

## License

This project is open source. Add a `LICENSE` file to specify terms (MIT is recommended for maximum adoption). Until a license is added, please contact the maintainers before using this code in production.

---

## Acknowledgments

Built and maintained by the **ChenAI Community**, founded by [Madhavan](https://github.com/MadhavanAR).

Several agents were originally contributed by community members including [Cole Medin](https://www.youtube.com/@ColeMedin) and [Mike Russell](https://n8n.io/creators/mikerussell/).

---

<p align="center">
  <sub>© 2025 ChenAI Community · Built with ❤️ for the open-source AI community</sub>
</p>
