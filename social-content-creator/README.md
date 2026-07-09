# Content Creator Agent

> Generate engaging, research-backed content for LinkedIn, X, and blog posts.

Part of [ChenAI Agents](https://github.com/MadhavanAR/Agents) — open-source AI agent templates by the [ChenAI Community](https://www.linkedin.com/company/chenai/).

**Author:** [Nate Herkelman](https://www.youtube.com/@nateherk)

## Features

- Web research on specified topics
- Platform-specific content generation (LinkedIn, X, blog)
- Audience-aware messaging and multi-platform strategies
- SEO-friendly blog post structure

## Prerequisites

- [n8n](https://n8n.io/) instance
- OpenAI API key

## Quick Start

### 1. Clone the repository

```bash
git clone https://github.com/MadhavanAR/Agents.git
cd Agents/social-content-creator
```

### 2. Import the workflow

1. Open your n8n instance
2. Go to **Workflows** → **Import from File**
3. Select `Content_Creator.json`

### 3. Configure credentials

| Credential | Purpose |
|------------|---------|
| OpenAI API | Content generation |
| Header Auth | Webhook authentication (optional) |

### 4. Activate the workflow

Enable the workflow and use the webhook URL for API requests.

## Use Cases

- Social media marketing across LinkedIn and X
- Blog content creation with research and citations
- Audience-targeted content strategies
- Industry trend analysis and talking points

## Files

| File | Description |
|------|-------------|
| `Content_Creator.json` | n8n workflow |

## Contributing

Contributions are welcome! See [CONTRIBUTING.md](../CONTRIBUTING.md).

## License

Licensed under the [MIT License](../LICENSE).
