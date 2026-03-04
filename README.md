# LLMSE Plugin

A plugin and marketplace package that integrates [LLMSE.AI](https://llmse.ai) content classification and analysis capabilities directly into Claude and Cursor.

## Overview

This repository provides LLMSE.AI plugins for multiple AI coding assistants:

- **Claude Plugin** — Connects Claude to the LLMSE.AI backend via the Model Context Protocol (MCP), enabling content classification, EEAT analysis, and SEO evaluation from within Claude.
- **Cursor Plugin** — Brings the same LLMSE.AI capabilities into Cursor via its MCP plugin system.
- **Marketplace Packages** — Structured for distribution through both the Claude and Cursor plugin marketplaces, supporting versioned releases and multi-plugin bundles.

## Features

- **Content Classification** — AI/ML-powered content categorization
- **EEAT Analysis** — Evaluate content against Google's Experience, Expertise, Authoritativeness, and Trustworthiness framework
- **AEO Scoring** — Answer Engine Optimization metrics and insights
- **SEO Evaluation** — Search engine optimization analysis and recommendations
- **GARM Brand Safety** — Brand suitability scoring based on the GARM framework
- **WCAG Accessibility** — Automated WCAG 2.1 Level A accessibility checks
- **Remote MCP Integration** — Communicates with the LLMSE.AI service over HTTP via the Model Context Protocol

## Repository Structure

```
llmse-plugin/
├── .claude-plugin/
│   └── marketplace.json              # Claude marketplace registry metadata
├── .cursor-plugin/
│   └── marketplace.json              # Cursor marketplace registry metadata
├── providers/
│   ├── claude/
│   │   └── plugin/
│   │       ├── .claude-plugin/
│   │       │   └── plugin.json       # Claude plugin definition
│   │       └── .mcp.json             # MCP server configuration
│   └── cursor/
│       └── plugin/
│           ├── .cursor-plugin/
│           │   └── plugin.json       # Cursor plugin definition
│           └── mcp.json              # MCP server configuration
└── LICENSE                           # BSD 3-Clause
```

## Installation

### Claude

Install from the Claude plugin marketplace by searching for **llmse**, or install directly from this repository:

```
https://github.com/tb0hdan/llmse-plugin
```

### Cursor

Install from the Cursor plugin marketplace by searching for **llmse**, or install directly from this repository.

Once installed, the plugin connects to the LLMSE.AI MCP server automatically. No additional configuration is required.

## How It Works

The plugin registers an HTTP-based MCP server pointing to `https://llmse.ai/mcp`. When the AI assistant invokes LLMSE tools, requests are sent to the remote service, and results are returned directly into the conversation context.

## License

BSD 3-Clause. See [LICENSE](LICENSE) for details.

## Links

- **LLMSE.AI** — https://llmse.ai
- **DomainsProject** — https://domainsproject.org
- **Repository** — https://github.com/tb0hdan/llmse-plugin
