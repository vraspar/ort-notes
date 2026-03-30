# ort-notes 🧠

A team knowledge base for Microsoft's ONNX ecosystem, powered by [Brain CLI](https://github.com/vraspar/brain).

**Three repos. One brain. Search once.**

## What's Inside

| Source | Entries | What It Covers |
|--------|---------|----------------|
| [Olive](https://github.com/microsoft/olive) | 45 | Model optimization, quantization (AWQ, GPTQ, RTN), CLI tools |
| [ONNX Runtime](https://github.com/microsoft/onnxruntime) | 29 | Inference engine, execution providers, APIs, deployment |
| [ONNX Runtime GenAI](https://github.com/microsoft/onnxruntime-genai) | 26 | LLM generation, constrained decoding, model building |

**100 entries** from 3 repos — searchable, connected, and always fresh.

## Quick Start

```bash
# Install Brain CLI
npm install -g @vraspar/brain

# Join this brain
brain connect https://github.com/vraspar/ort-notes.git

# Search across all 3 repos at once
brain search "quantization"

# See what's new
brain digest

# Explore connections
brain trail "execution providers"

# Dashboard
brain status
```

## Why This Exists

A developer working across Olive, ONNX Runtime, and GenAI today has to search 3 separate GitHub repos manually. Knowledge about quantization lives in Olive's docs AND ORT's operator specs AND GenAI's model builder — but nothing connects them.

Brain makes it one command:

```bash
$ brain search "quantization"
# → 20 results spanning Olive, ORT, and GenAI
```

```bash
$ brain trail "quantization"
# → Olive's quantization passes → ORT's quantization operators → GenAI's model download flow
```

## For AI Agents

Brain has a built-in [MCP server](https://modelcontextprotocol.io) — your AI coding agents can search this knowledge base automatically:

```bash
brain serve
# Agents can now call search_knowledge, get_recommendations, etc.
```

## Keeping It Fresh

```bash
# Pull latest from all 3 source repos
brain sync

# Check health
brain status
```

---

Built with [Brain CLI](https://github.com/vraspar/brain) — turn scattered docs into a searchable team brain.
