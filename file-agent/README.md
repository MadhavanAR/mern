# File Processing Agent

> FastAPI agent that handles file uploads, stores content with conversation history, and integrates files into AI context.

Part of [ChenAI Agents](https://github.com/MadhavanAR/Agents) — open-source AI agent templates by the [ChenAI Community](https://www.linkedin.com/company/chenai/).

**Author:** [Cole Medin](https://www.youtube.com/@ColeMedin)

Built on the [Python Agent Template](../templates/python-agent/) with file handling capabilities.

## Features

- Process uploaded files in base64 format
- Store file content with conversation history in Supabase
- Integrate file content into AI model context
- Handle multiple files in a single conversation

## Prerequisites

- Python 3.11+
- Supabase account
- OpenAI API key

## Quick Start

### 1. Clone the repository

```bash
git clone https://github.com/MadhavanAR/Agents.git
cd Agents/file-agent
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
API_BEARER_TOKEN=your_bearer_token
OPENAI_API_KEY=your_openai_key
```

### 4. Run

```bash
python file_agent.py
```

Available at `http://localhost:8001`.

## API Usage

Send POST requests to `/api/file-agent`:

```json
{
  "query": "What does this file contain?",
  "files": [{
    "name": "example.txt",
    "type": "text/plain",
    "base64": "VGhpcyBpcyBhIHRlc3QgZmlsZS4="
  }],
  "session_id": "unique-session-id",
  "user_id": "user-id",
  "request_id": "request-id"
}
```

## Files

| File | Description |
|------|-------------|
| `file_agent.py` | FastAPI agent with file handling |
| `requirements.txt` | Python dependencies |
| `.env.example` | Environment variable template |

## Contributing

Contributions are welcome! See [CONTRIBUTING.md](../CONTRIBUTING.md).

## License

Licensed under the [MIT License](../LICENSE).
