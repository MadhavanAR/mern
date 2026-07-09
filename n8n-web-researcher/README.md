# Advanced Web Researcher Agent

> Deep web research with Brave Search API and AI summarization via n8n.

Part of [ChenAI Agents](https://github.com/MadhavanAR/Agents) — open-source AI agent templates by the [ChenAI Community](https://www.linkedin.com/company/chenai/).

**Author:** [Cole Medin](https://www.youtube.com/@ColeMedin)

## Features

- Brave Search API for high-quality search results
- Automatic article summarization
- Source attribution and relevance filtering
- Complex multi-source research queries

## Prerequisites

- [n8n](https://n8n.io/) instance
- Brave Search API key
- OpenAI API key

## Quick Start

### 1. Clone the repository

```bash
git clone https://github.com/MadhavanAR/Agents.git
cd Agents/n8n-web-researcher
```

### 2. Import the workflow

1. Open your n8n instance
2. Go to **Workflows** → **Import from File**
3. Select `Advanced_Web_Researcher.json`

### 3. Configure credentials

| Credential | Purpose |
|------------|---------|
| Brave Search API | Web search |
| OpenAI API | Summarization and analysis |
| Header Auth | Webhook authentication (optional) |

### 4. Activate the workflow

Enable the workflow and use the webhook URL for API requests.

## Use Cases

- Deep topic research and fact verification
- Market and competitive analysis
- Cross-source information synthesis
- Technical documentation search

## Files

| File | Description |
|------|-------------|
| `Advanced_Web_Researcher.json` | n8n workflow |

## Contributing

Contributions are welcome! See [CONTRIBUTING.md](../CONTRIBUTING.md).

## License

Licensed under the [MIT License](../LICENSE).
