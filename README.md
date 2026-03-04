# LLMSE Plugin for Claude

A Claude plugin and marketplace package that integrates [LLMSE.AI](https://llmse.ai) content classification and analysis capabilities directly into Claude.

## Overview

This repository serves a dual purpose:

- **Claude Plugin** — Connects Claude to the LLMSE.AI backend via the Model Context Protocol (MCP), enabling content classification, EEAT analysis, and SEO evaluation from within Claude.
- **Marketplace Package** — Structured for distribution through the Claude plugin marketplace, supporting versioned releases and multi-plugin bundles.

## Features

- **Content Classification** — AI/ML-powered content categorization
- **EEAT Analysis** — Evaluate content against Google's Experience, Expertise, Authoritativeness, and Trustworthiness framework
- **AEO Scoring** — Answer Engine Optimization metrics and insights
- **SEO Evaluation** — Search engine optimization analysis and recommendations
- **Remote MCP Integration** — Communicates with the LLMSE.AI service over HTTP via the Model Context Protocol

## Repository Structure

```
llmse-plugin/
├── .claude-plugin/
│   └── marketplace.json              # Marketplace registry metadata
├── providers/
│   └── claude/
│       └── plugin/
│           ├── .claude-plugin/
│           │   └── plugin.json       # Plugin definition
│           └── .mcp.json             # MCP server configuration
└── LICENSE                           # BSD 3-Clause
```

## Installation

Install from the Claude plugin marketplace by searching for **llmse**, or install directly from this repository:

```
https://github.com/tb0hdan/llmse-plugin
```

Once installed, Claude connects to the LLMSE.AI MCP server automatically. No additional configuration is required.

## How It Works

The plugin registers an HTTP-based MCP server pointing to `https://llmse.ai/mcp`. When Claude invokes LLMSE tools, requests are sent to the remote service, and results are returned directly into the conversation context.

## License

BSD 3-Clause. See [LICENSE](LICENSE) for details.

## Links

- **LLMSE.AI** — https://llmse.ai
- **DomainsProject** — https://domainsproject.org
- **Repository** — https://github.com/tb0hdan/llmse-plugin
