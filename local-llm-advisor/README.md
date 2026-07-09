# Local AI Expert Agent

> Personal consultant for local AI deployments, open-source LLMs, and hardware requirements.

Part of [ChenAI Agents](https://github.com/MadhavanAR/Agents) — open-source AI agent templates by the [ChenAI Community](https://www.linkedin.com/company/chenai/).

**Author:** [Cole Medin](https://www.youtube.com/@ColeMedin)

## Features

- Guidance on trending open-source LLMs
- Hardware requirements for running different models
- Local AI deployment strategies and troubleshooting
- Searches Ollama and HuggingFace model catalogs

## Prerequisites

- [n8n](https://n8n.io/) instance
- Anthropic API credentials

## Quick Start

### 1. Clone the repository

```bash
git clone https://github.com/MadhavanAR/Agents.git
cd Agents/local-llm-advisor
```

### 2. Import the workflow

1. Open your n8n instance
2. Go to **Workflows** → **Import from File**
3. Select `Local_AI_Expert.json`

### 3. Configure credentials

| Credential | Purpose |
|------------|---------|
| Anthropic API | Claude 3.5 Haiku |
| Header Auth | Webhook authentication (optional) |

### 4. Activate the workflow

Enable the workflow and use the webhook URL for API requests.

## Example Queries

- "What are the top 3 open-source LLMs for local deployment?"
- "What are the minimum hardware requirements to run Llama 3.2 locally?"
- "How can I optimize my local LLM for better performance?"

## Files

| File | Description |
|------|-------------|
| `Local_AI_Expert.json` | n8n workflow |

## Contributing

Contributions are welcome! See [CONTRIBUTING.md](../CONTRIBUTING.md).

## License

Licensed under the [MIT License](../LICENSE).
