# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

DeepThought is an exploration and documentation repository focused on GenAI tools and CLI clients. This is a work-in-progress project (as of 2025-08-01) for exploring various AI assistants and their capabilities.

## Repository Structure

This repository is primarily documentation-focused with minimal code structure:

- `README.md` - Main project documentation explaining purpose and tools being explored
- `Images/` - Contains project assets (DEEPTHOUGHT-Banner.png)
- `LICENSE` - GPL v3 license

## Tools Being Explored

Based on the README, this repository documents exploration of:

- **Perplexity.AI** (WebUI and CLI) - for general web search and guidance
- **Anthropic Claude Pro / Claude Code** - code assistant capabilities  
- **Amazon Bedrock** - for Nova and Claude access via AWS
- **VS Code integration** - using AI assistants within the editor

## AWS Bedrock Configuration

The repository includes examples of working with Amazon Bedrock models:

```bash
# List available foundation models
aws bedrock list-foundation-models --query 'modelSummaries[*].[modelArn, modelId, modelName]' --output text | grep nova

# Configure chat-cli with a specific model
chat-cli config set model-id amazon.nova-lite-v1:0

# Test a query
chat-cli prompt "your question here"
```

## Related Projects

The README references several related CLI tools:
- [chat-cli](https://github.com/chat-cli/chat-cli) - Amazon Bedrock Chat CLI client
- [perplexity-cli](https://github.com/cloudxabide/perplexity-cli) - Perplexity.AI CLI client

## Development Notes

- This is not a traditional software project with build/test processes
- No package managers or build tools are configured
- Focus is on documentation and exploration rather than code development
- Licensed under GPL v3