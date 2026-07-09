# n8n Expert Agent

> Find and understand n8n automation workflows from natural language queries.

Part of [ChenAI Agents](https://github.com/MadhavanAR/Agents) — open-source AI agent templates by the [ChenAI Community](https://www.linkedin.com/company/chenai/).

**Author:** [Cole Medin](https://www.youtube.com/@ColeMedin)

> **Note:** This agent is in beta. Workflow recommendations may not always match your query as the knowledge base grows.

## Features

- Natural language workflow discovery and recommendations
- Workflow analysis with LLM-powered summaries
- Legitimacy validation to filter test/spam workflows
- Vector embeddings for semantic search via Supabase
- Webhook-based API with session management

## Prerequisites

- [n8n](https://n8n.io/) instance (self-hosted or cloud)
- Supabase account
- OpenAI API key

## Quick Start

### 1. Clone the repository

```bash
git clone https://github.com/MadhavanAR/Agents.git
cd Agents/n8n-workflow-finder
```

### 2. Import the workflow

1. Open your n8n instance
2. Go to **Workflows** → **Import from File**
3. Select `N8N_Expert_Agent.json`

### 3. Configure credentials

In n8n, set up:

| Credential | Purpose |
|------------|---------|
| Supabase API | Workflow storage and message history |
| OpenAI API | LLM analysis and embeddings |
| Header Auth | Webhook authentication (optional) |

For the Python ingestion script, copy and configure environment:

```bash
cp .env.example .env
```

```env
LLM_MODEL=gpt-4
EMBEDDING_MODEL=text-embedding-3-small
SUPABASE_URL=your_supabase_url
SUPABASE_SERVICE_KEY=your_supabase_service_key
```

### 4. Ingest workflows (optional)

Populate the knowledge base:

```bash
pip install -r requirements.txt
python ingest-n8n-workflows.py
```

### 5. Activate the workflow

Enable the workflow and use the webhook URL (`/invoke-n8n-expert`) for API requests.

## Example

```
User: "I need to automatically post tweets when new blog posts are published"
Agent: Recommends WordPress-to-Twitter, RSS-to-social, and content distribution workflows
```

## Files

| File | Description |
|------|-------------|
| `N8N_Expert_Agent.json` | Main n8n workflow |
| `ingest-n8n-workflows.py` | Workflow ingestion script |
| `sql_script.sql` | Database schema |
| `requirements.txt` | Python dependencies |
| `.env.example` | Environment variable template |

## Contributing

Contributions are welcome! See [CONTRIBUTING.md](../CONTRIBUTING.md).

## License

Licensed under the [MIT License](../LICENSE).
