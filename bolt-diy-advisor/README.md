# bolt.diy Expert Agent

> Expert assistant for bolt.diy — the open-source bolt.new with multiple LLM provider support.

Part of [ChenAI Agents](https://github.com/MadhavanAR/Agents) — open-source AI agent templates by the [ChenAI Community](https://www.linkedin.com/company/chenai/).

**Author:** [Cole Medin](https://www.youtube.com/@ColeMedin)

## Features

- Answers questions about bolt.diy features and capabilities
- Installation, setup, and LLM provider configuration guidance
- Troubleshooting and contribution support
- Knowledge base from official bolt.diy documentation

## Prerequisites

- [n8n](https://n8n.io/) instance
- OpenAI API key (or configured LLM credentials)

## Quick Start

### 1. Clone the repository

```bash
git clone https://github.com/MadhavanAR/Agents.git
cd Agents/bolt-diy-advisor
```

### 2. Import the workflow

1. Open your n8n instance
2. Go to **Workflows** → **Import from File**
3. Select `bolt_diy_Expert.json`

### 3. Configure credentials

| Credential | Purpose |
|------------|---------|
| OpenAI API | LLM responses |
| Header Auth | Webhook authentication (optional) |

### 4. Activate the workflow

Enable the workflow and use the webhook URL for API requests.

## Example Queries

- "How do I install bolt.diy?"
- "Which LLM providers are supported?"
- "How do I set up my API keys?"

## External Resources

- [bolt.diy Documentation](https://stackblitz-labs.github.io/bolt.diy/)
- [GitHub Repository](https://github.com/stackblitz-labs/bolt.diy)

## Files

| File | Description |
|------|-------------|
| `bolt_diy_Expert.json` | n8n workflow |

## Contributing

Contributions are welcome! See [CONTRIBUTING.md](../CONTRIBUTING.md).

## License

Licensed under the [MIT License](../LICENSE).
