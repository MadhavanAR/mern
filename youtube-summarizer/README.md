# YouTube Video Summarizer Agent

> Summarize YouTube videos and chat about their content using captions and AI.

Part of [ChenAI Agents](https://github.com/MadhavanAR/Agents) — open-source AI agent templates by the [ChenAI Community](https://www.linkedin.com/company/chenai/).

**Author:** [Mike Russell](https://n8n.io/creators/mikerussell/)

## Features

- Processes YouTube video IDs and full URLs
- Retrieves and analyzes video captions
- Generates detailed summaries with follow-up Q&A
- Maintains conversational context

## Prerequisites

- [n8n](https://n8n.io/) instance
- YouTube OAuth2 credentials (your own account)
- OpenAI API key

> **Important:** YouTube OAuth2 must be from your own account to access captions. The agent cannot use credentials from other accounts.

## Quick Start

### 1. Clone the repository

```bash
git clone https://github.com/MadhavanAR/Agents.git
cd Agents/youtube-summarizer
```

### 2. Import the workflow

1. Open your n8n instance
2. Go to **Workflows** → **Import from File**
3. Select `YouTube_Video_Summarizer.json`

### 3. Configure credentials

| Credential | Purpose |
|------------|---------|
| YouTube OAuth2 | Video caption access |
| OpenAI API | Summarization and chat |
| Header Auth | Webhook authentication (optional) |

### 4. Activate the workflow

Enable the workflow and use the webhook URL for API requests.

## Example Queries

```
"Summarize this video: https://youtube.com/watch?v=..."
"What were the main points about [topic]?"
"What tools or technologies were mentioned?"
```

## Files

| File | Description |
|------|-------------|
| `YouTube_Video_Summarizer.json` | n8n workflow |

## Contributing

Contributions are welcome! See [CONTRIBUTING.md](../CONTRIBUTING.md).

## License

Licensed under the [MIT License](../LICENSE).
