# Examples

> Example scripts demonstrating different documentation crawling strategies.

Part of [ChenAI Agents](https://github.com/MadhavanAR/Agents) — open-source AI agent templates by the [ChenAI Community](https://www.linkedin.com/company/chenai/).

These scripts complement the main [Documentation Crawler & RAG Agent](../README.md).

## Scripts

| Script | Description |
|--------|-------------|
| `1-crawl_single_page.py` | Crawl a single documentation page |
| `2-crawl_docs_sequential.py` | Sequential multi-page crawling |
| `3-crawl_docs_FAST.py` | Parallel/fast crawling approach |

## Usage

Run from the parent `doc-rag-agent` directory after installing dependencies:

```bash
cd ../doc-rag-agent
pip install -r requirements.txt
cp .env.example .env
# Edit .env with your keys

cd examples
python 1-crawl_single_page.py
```

## Contributing

Contributions are welcome! See [CONTRIBUTING.md](../../CONTRIBUTING.md).

## License

Licensed under the [MIT License](../../LICENSE).
