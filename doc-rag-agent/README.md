# Documentation Crawler & RAG Agent

> Crawl documentation websites, store content in Supabase, and answer questions with RAG using Pydantic AI.

Part of [ChenAI Agents](https://github.com/MadhavanAR/Agents) — open-source AI agent templates by the [ChenAI Community](https://www.linkedin.com/company/chenai/).

**Author:** [Cole Medin](https://www.youtube.com/@ColeMedin)

## Features

- Documentation website crawling and chunking
- Vector database storage with Supabase
- Semantic search using OpenAI embeddings
- RAG-based question answering with code block preservation
- Streamlit UI for interactive querying

## Prerequisites

- Python 3.11+
- Supabase account and database
- OpenAI API key

## Quick Start

### 1. Clone the repository

```bash
git clone https://github.com/MadhavanAR/Agents.git
cd Agents/doc-rag-agent
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
OPENAI_API_KEY=your_openai_api_key
SUPABASE_URL=your_supabase_url
SUPABASE_SERVICE_KEY=your_supabase_service_key
LLM_MODEL=gpt-4o-mini
```

### 4. Set up the database

Run the SQL in `site_pages.sql` to create tables and enable vector search.

### 5. Crawl and query

```bash
# Crawl documentation and store embeddings
python crawl_pydantic_ai_docs.py

# Launch interactive UI
streamlit run streamlit_ui.py
```

The Streamlit UI will be available at `http://localhost:8501`.

## Configuration

### Database Schema

```sql
CREATE TABLE site_pages (
    id UUID PRIMARY KEY DEFAULT uuid_generate_v4(),
    url TEXT,
    chunk_number INTEGER,
    title TEXT,
    summary TEXT,
    content TEXT,
    metadata JSONB,
    embedding VECTOR(1536)
);
```

### Chunking

Adjust `chunk_size` in `crawl_pydantic_ai_docs.py` (default: 5000 characters). The chunker preserves code blocks, paragraphs, and sentence boundaries.

## Files

| File | Description |
|------|-------------|
| `crawl_pydantic_ai_docs.py` | Documentation crawler and processor |
| `pydantic_ai_agent.py` | RAG agent implementation |
| `streamlit_ui.py` | Web interface |
| `site_pages.sql` | Database setup |
| `examples/` | Example crawling scripts |
| `requirements.txt` | Python dependencies |
| `.env.example` | Environment variable template |

## Contributing

Contributions are welcome! See [CONTRIBUTING.md](../CONTRIBUTING.md).

## License

Licensed under the [MIT License](../LICENSE).
