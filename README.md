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

**ChenAI Agents** is an open-source collection of production-ready AI agent templates built by the [ChenAI Community](https://www.linkedin.com/company/chenai/). Each agent is a self-contained project you can clone, configure, and run.

Contributions, issues, and stars are welcome.

---

## Agents

### Python Agents

| Folder | Description | Docs |
|--------|-------------|------|
| [github-agent](./github-agent/) | Analyze GitHub repos — structure, files, and features | [README](./github-agent/README.md) |
| [web-researcher](./web-researcher/) | Web search with Brave API (Pydantic AI) | [README](./web-researcher/README.md) |
| [doc-rag-agent](./doc-rag-agent/) | Crawl docs, embed in Supabase, answer with RAG | [README](./doc-rag-agent/README.md) |
| [file-agent](./file-agent/) | FastAPI agent with file upload and AI context | [README](./file-agent/README.md) |

### n8n Workflow Agents

| Folder | Description | Docs |
|--------|-------------|------|
| [n8n-workflow-finder](./n8n-workflow-finder/) | Find n8n automation workflows from natural language | [README](./n8n-workflow-finder/README.md) |
| [github-assistant](./github-assistant/) | GitHub repository exploration assistant | [README](./github-assistant/README.md) |
| [n8n-web-researcher](./n8n-web-researcher/) | Deep web research with Brave Search | [README](./n8n-web-researcher/README.md) |
| [youtube-summarizer](./youtube-summarizer/) | Summarize YouTube videos and chat about content | [README](./youtube-summarizer/README.md) |
| [tech-stack-advisor](./tech-stack-advisor/) | Recommend tech stacks for full-stack apps | [README](./tech-stack-advisor/README.md) |
| [local-llm-advisor](./local-llm-advisor/) | Guidance on running LLMs locally | [README](./local-llm-advisor/README.md) |
| [bolt-diy-advisor](./bolt-diy-advisor/) | Expert assistant for bolt.diy | [README](./bolt-diy-advisor/README.md) |
| [social-content-creator](./social-content-creator/) | Generate LinkedIn, X, and blog content | [README](./social-content-creator/README.md) |
| [small-business-researcher](./small-business-researcher/) | Research business ideas from Reddit | [README](./small-business-researcher/README.md) |

### Templates & Infrastructure

| Folder | Description | Docs |
|--------|-------------|------|
| [templates/python-agent](./templates/python-agent/) | Starter FastAPI + Supabase agent template | [README](./templates/python-agent/README.md) |
| [templates/n8n-agent](./templates/n8n-agent/) | Starter n8n agent workflow template | [README](./templates/n8n-agent/README.md) |
| [docker/python-base](./docker/python-base/) | Shared Docker base image for Python agents | [README](./docker/python-base/README.md) |
| [integrations/voiceflow](./integrations/voiceflow/) | Voiceflow Dialog API integration | [README](./integrations/voiceflow/README.md) |

---

## Quick Start

### 1. Clone the repository

```bash
git clone https://github.com/MadhavanAR/Agents.git
cd Agents
```

### 2. Pick an agent

Choose a folder from the tables above and `cd` into it.

### 3. Configure environment

Python agents include a `.env.example` file:

```bash
cp .env.example .env
# Edit .env with your API keys
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
├── github-agent/              # GitHub repo analysis (Python)
├── web-researcher/            # Web search with Brave API (Python)
├── doc-rag-agent/             # Documentation crawler + RAG (Python)
├── file-agent/                # File upload agent (Python)
├── n8n-workflow-finder/       # n8n workflow discovery
├── github-assistant/          # GitHub assistant (n8n)
├── n8n-web-researcher/        # Web research (n8n)
├── youtube-summarizer/        # YouTube summarizer (n8n)
├── tech-stack-advisor/        # Tech stack advisor (n8n)
├── local-llm-advisor/         # Local LLM advisor (n8n)
├── bolt-diy-advisor/          # bolt.diy advisor (n8n)
├── social-content-creator/    # Social content creator (n8n)
├── small-business-researcher/ # Business research (n8n)
├── templates/
│   ├── python-agent/          # Python agent starter template
│   └── n8n-agent/             # n8n agent starter template
├── docker/
│   └── python-base/           # Shared Docker base image
├── integrations/
│   └── voiceflow/             # Voiceflow integration
├── LICENSE
├── CONTRIBUTING.md
└── README.md
```

---

## Prerequisites

| Tool | Used for |
|------|----------|
| Python 3.11+ | Python-based agents |
| [n8n](https://n8n.io/) | Workflow-based agents |
| [Supabase](https://supabase.com/) | Vector storage and conversation history |
| OpenAI / OpenRouter / Brave API | LLM and search capabilities |

Check each agent's README for specific requirements.

---

## Contributing

We welcome contributions from the community. See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

1. **Fork** the repository
2. **Create a branch** (`git checkout -b feature/my-new-agent`)
3. **Add or improve an agent** with a clear README
4. **Test locally** before opening a PR
5. **Open a Pull Request**

---

## Community

- **ChenAI Community** — [LinkedIn](https://www.linkedin.com/company/chenai/)
- **Issues** — [GitHub Issues](https://github.com/MadhavanAR/Agents/issues)

---

## License

Licensed under the [MIT License](LICENSE).

---

## Acknowledgments

Built and maintained by the **ChenAI Community**, founded by [Madhavan](https://github.com/MadhavanAR).

Several agents were originally contributed by community members including [Cole Medin](https://www.youtube.com/@ColeMedin) and [Mike Russell](https://n8n.io/creators/mikerussell/).

---

<p align="center">
  <sub>© 2025 ChenAI Community · Built with ❤️ for the open-source AI community</sub>
</p>
