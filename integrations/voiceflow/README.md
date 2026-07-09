# Voiceflow Dialog API Integration

> Connect Voiceflow agents to a FastAPI backend with Supabase conversation storage.

Part of [ChenAI Agents](https://github.com/MadhavanAR/Agents) — open-source AI agent templates by the [ChenAI Community](https://www.linkedin.com/company/chenai/).

**Author:** [Cole Medin](https://www.youtube.com/@ColeMedin)

> For Voiceflow Dialog API details, see the [official documentation](https://docs.voiceflow.com/reference/overview).

## Features

- Real-time conversation handling via Voiceflow Dialog API
- Automatic message history tracking in Supabase
- Session management for conversation context
- Secure API authentication
- Frontend component for rich Voiceflow responses

## Prerequisites

- Python 3.11+
- Supabase account
- Voiceflow account with API key

## Quick Start

### 1. Clone the repository

```bash
git clone https://github.com/MadhavanAR/Agents.git
cd Agents/integrations/voiceflow
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
SUPABASE_URL=your_supabase_url
SUPABASE_SERVICE_KEY=your_supabase_key
API_BEARER_TOKEN=your_api_token
VOICEFLOW_AGENT_API_KEY=your_voiceflow_api_key
```

### 4. Run

```bash
python voiceflow_integration.py
```

**Docker:**

```bash
docker build -t voiceflow-integration .
docker run -d --name voiceflow-integration -p 8001:8001 --env-file .env voiceflow-integration
```

## API Endpoint

**POST** `/api/sample-voiceflow-agent`

```json
{
  "query": "Hello!",
  "user_id": "user123",
  "request_id": "req123",
  "session_id": "sess123"
}
```

## Frontend Integration

`VoiceflowFrontendComponent.tsx` demonstrates rendering Voiceflow trace types (text, choice, knowledgeBase) in a custom frontend.

## Files

| File | Description |
|------|-------------|
| `voiceflow_integration.py` | FastAPI integration server |
| `VoiceflowFrontendComponent.tsx` | Example frontend component |
| `Dockerfile` | Container definition |
| `requirements.txt` | Python dependencies |
| `.env.example` | Environment variable template |

## Contributing

Contributions are welcome! See [CONTRIBUTING.md](../../CONTRIBUTING.md).

## License

Licensed under the [MIT License](../../LICENSE).
