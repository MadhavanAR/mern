# Tech Stack Expert Agent

> Guided conversational assistant that recommends the ideal tech stack for full-stack applications.

Part of [ChenAI Agents](https://github.com/MadhavanAR/Agents) — open-source AI agent templates by the [ChenAI Community](https://www.linkedin.com/company/chenai/).

**Author:** [Cole Medin](https://www.youtube.com/@ColeMedin)

## Features

- Guided conversation to understand project requirements
- Tailored recommendations for frontend, backend, auth, database, and LLM integration
- Postgres chat memory for conversation context
- Powered by Claude 3.5 Haiku

## Prerequisites

- [n8n](https://n8n.io/) instance
- Anthropic API credentials
- PostgreSQL database (for chat memory)

## Quick Start

### 1. Clone the repository

```bash
git clone https://github.com/MadhavanAR/Agents.git
cd Agents/tech-stack-advisor
```

### 2. Import the workflow

1. Open your n8n instance
2. Go to **Workflows** → **Import from File**
3. Select `Tech_Stack_Expert.json`

### 3. Configure credentials

| Credential | Purpose |
|------------|---------|
| Anthropic API | Claude 3.5 Haiku |
| Postgres | Chat memory |
| Header Auth | Webhook authentication (optional) |

### 4. Activate the workflow

Enable the workflow and use the webhook URL for API requests.

## How It Works

1. Gathers information about your application concept
2. Assesses experience with frontend and backend technologies
3. Evaluates expected user scale and specific requirements
4. Provides a comprehensive tech stack recommendation

## API Usage

```json
{
  "query": "I want to build a SaaS app for small teams",
  "user_id": "unique-user-identifier",
  "request_id": "request-tracking-id",
  "session_id": "conversation-session-id"
}
```

## Files

| File | Description |
|------|-------------|
| `Tech_Stack_Expert.json` | n8n workflow |

## Contributing

Contributions are welcome! See [CONTRIBUTING.md](../CONTRIBUTING.md).

## License

Licensed under the [MIT License](../LICENSE).
