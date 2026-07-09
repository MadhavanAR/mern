# Base Sample n8n Agent

> Minimal n8n workflow template for building conversational AI agents with webhook and database integration.

Part of [ChenAI Agents](https://github.com/MadhavanAR/Agents) — open-source AI agent templates by the [ChenAI Community](https://www.linkedin.com/company/chenai/).

**Author:** [Cole Medin](https://www.youtube.com/@ColeMedin)

## Available Workflows

| Workflow | File | Description |
|----------|------|-------------|
| Base Sample Agent | `Base_Sample_Agent.json` | Full control over conversation history with Supabase |
| Agent Node Sample | `Agent_Node_Sample_Agent.json` | Uses n8n's built-in Agent node for simpler setup |

## Features

- Webhook endpoint with authentication
- Input processing (query, user_id, request_id, session_id)
- Supabase/Postgres message storage
- Structured JSON response format

## Prerequisites

- [n8n](https://n8n.io/) instance
- Supabase account (or PostgreSQL for Agent Node variant)

## Quick Start

### 1. Clone the repository

```bash
git clone https://github.com/MadhavanAR/Agents.git
cd Agents/templates/n8n-agent
```

### 2. Import the workflow

1. Open your n8n instance
2. Go to **Workflows** → **Import from File**
3. Select `Base_Sample_Agent.json` (or `Agent_Node_Sample_Agent.json`)

### 3. Configure credentials

| Credential | Purpose |
|------------|---------|
| Header Auth | Webhook authentication (optional) |
| Supabase API | Message storage |

### 4. Activate the workflow

Enable the workflow and use the webhook URL for API requests.

## Message Format

**Input:**
```json
{
  "query": "User's question or command",
  "user_id": "unique-user-identifier",
  "request_id": "request-tracking-id",
  "session_id": "conversation-session-id"
}
```

**Output:**
```json
{
  "success": true,
  "output": "AI response content",
  "data": "Additional response data"
}
```

## Workflow Structure

1. **Webhook Node** — Entry point, validates auth headers
2. **Prep Input Fields** — Extracts and validates request data
3. **Database Nodes** — Stores user messages and AI responses
4. **Output Preparation** — Formats structured response

## Files

| File | Description |
|------|-------------|
| `Base_Sample_Agent.json` | Primary workflow template |
| `Agent_Node_Sample_Agent.json` | Agent node variant |

## Contributing

Contributions are welcome! See [CONTRIBUTING.md](../../CONTRIBUTING.md).

## License

Licensed under the [MIT License](../../LICENSE).
