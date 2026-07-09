# Base Python Docker Image

> Shared Docker base image for Python-based ChenAI Agents with common dependencies pre-installed.

Part of [ChenAI Agents](https://github.com/MadhavanAR/Agents) — open-source AI agent templates by the [ChenAI Community](https://www.linkedin.com/company/chenai/).

**Author:** [Cole Medin](https://www.youtube.com/@ColeMedin)

## Features

- Python 3.11 slim base image
- Common dependencies pre-installed (FastAPI, Uvicorn, Pydantic, etc.)
- Non-root user for security
- Port 8001 exposed by default

## Quick Start

### Build the image

```bash
git clone https://github.com/MadhavanAR/Agents.git
cd Agents/docker/python-base
docker build -t chenai/base-python:latest .
```

### Use in your agent Dockerfile

```dockerfile
FROM chenai/base-python:latest

WORKDIR /app
COPY . .

CMD ["uvicorn", "your_app:app", "--host", "0.0.0.0", "--port", "8001"]
```

## Included Packages

See `requirements.txt` for the full list of pre-installed packages.

## Files

| File | Description |
|------|-------------|
| `Dockerfile` | Base image definition |
| `requirements.txt` | Pre-installed Python packages |

## Contributing

Contributions are welcome! See [CONTRIBUTING.md](../../CONTRIBUTING.md).

## License

Licensed under the [MIT License](../../LICENSE).
