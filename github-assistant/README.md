# GitHub Assistant Agent

> Intelligent GitHub repository assistant — explore structure, files, and code organization.

Part of [ChenAI Agents](https://github.com/MadhavanAR/Agents) — open-source AI agent templates by the [ChenAI Community](https://www.linkedin.com/company/chenai/).

**Author:** [Cole Medin](https://www.youtube.com/@ColeMedin)

## Features

- Repository structure analysis and navigation
- File content lookup and exploration
- Context tracking for follow-up questions
- Secure GitHub API integration

## Prerequisites

- [n8n](https://n8n.io/) instance
- GitHub API credentials
- OpenAI API key
- Supabase account (for conversation history)

## Quick Start

### 1. Clone the repository

```bash
git clone https://github.com/MadhavanAR/Agents.git
cd Agents/github-assistant
```

### 2. Import the workflow

1. Open your n8n instance
2. Go to **Workflows** → **Import from File**
3. Select `GitHub_Assistant_Agent.json`

### 3. Configure credentials

| Credential | Purpose |
|------------|---------|
| GitHub API | Repository access |
| OpenAI API | LLM responses |
| Supabase API | Conversation history |
| Header Auth | Webhook authentication (optional) |

### 4. Activate the workflow

Enable the workflow and use the webhook URL for API requests.

## API Usage

```json
{
  "query": "What is the structure of https://github.com/user/repo?",
  "user_id": "your_user_id",
  "request_id": "unique_request_id",
  "session_id": "session_identifier"
}
```

## Example Queries

- "What is the structure of this repository?"
- "Show me the contents of the main configuration file"
- "What are the key components in this project?"

## Limitations

- Requires valid GitHub repository URLs
- Public repositories only (unless GitHub token has private access)
- Response times vary with repository size

## Files

| File | Description |
|------|-------------|
| `GitHub_Assistant_Agent.json` | n8n workflow |

## Contributing

Contributions are welcome! See [CONTRIBUTING.md](../CONTRIBUTING.md).

## License

Licensed under the [MIT License](../LICENSE).
