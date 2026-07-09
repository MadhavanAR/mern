# Advanced Web Researcher (Pydantic AI)

> Web search agent powered by Pydantic AI and the Brave Search API, with CLI and Streamlit interfaces.

Part of [ChenAI Agents](https://github.com/MadhavanAR/Agents) — open-source AI agent templates by the [ChenAI Community](https://www.linkedin.com/company/chenai/).

**Author:** [Cole Medin](https://www.youtube.com/@ColeMedin) · [YouTube walkthrough](https://youtu.be/pC17ge_2n0Q)

## Features

- Brave Search API integration with article summarization
- Command-line interface and Streamlit web UI
- Supports OpenAI GPT and Ollama local models
- API endpoint variant in `studio-integration-version/`

## Prerequisites

- Python 3.11+
- Brave Search API key
- OpenAI API key (if using GPT models)
- [Ollama](https://ollama.ai/) (optional, for local LLM usage)

## Quick Start

### 1. Clone the repository

```bash
git clone https://github.com/MadhavanAR/Agents.git
cd Agents/web-researcher
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

Edit `.env`:

```env
OPENAI_API_KEY=your_openai_api_key   # Only needed if using GPT models
BRAVE_API_KEY=your_brave_api_key
LLM_MODEL=gpt-4o                     # Or qwen2.5:32b for Ollama
```

### 4. Run

**Command-line interface:**

```bash
python web_search_agent.py
```

**Streamlit web interface:**

```bash
streamlit run streamlit_ui.py
```

Opens at `http://localhost:8501`.

## Configuration

### LLM Models

- OpenAI: `LLM_MODEL=gpt-4o`
- Ollama: `LLM_MODEL=qwen2.5:32b` (ensure Ollama is running)

### API Keys

- **Brave Search API** — [Brave Search API](https://brave.com/search/api/)
- **OpenAI API** — [OpenAI Platform](https://platform.openai.com/api-keys)

## Files

| File | Description |
|------|-------------|
| `web_search_agent.py` | CLI agent |
| `streamlit_ui.py` | Streamlit web interface |
| `web_search_agent_streamlit.py` | Streamlit agent logic |
| `requirements.txt` | Python dependencies |
| `.env.example` | Environment variable template |
| `studio-integration-version/` | FastAPI endpoint reference |

## Troubleshooting

1. **Ollama** — Run `ollama serve` and `ollama pull your_model_name`
2. **API keys** — Verify keys in `.env` and check Brave API credits
3. **Memory** — Use a smaller Ollama model if you hit RAM limits

## Contributing

Contributions are welcome! See [CONTRIBUTING.md](../CONTRIBUTING.md).

## License

Licensed under the [MIT License](../LICENSE).
