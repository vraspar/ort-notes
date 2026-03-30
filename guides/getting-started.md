---
title: Getting Started with Brain
author: vraspar
created: "2026-03-30T22:26:20.446Z"
updated: "2026-03-30T22:26:20.446Z"
tags:
  - onboarding
  - getting-started
type: guide
status: active
summary: How to use this team brain to share and discover knowledge.
---

Welcome to your team's shared brain! Here's how to get started.

## Sharing Knowledge

Write a markdown file and push it:

```bash
brain push --title "How to Deploy" --type guide --file ./deploy-guide.md
```

Tags are auto-detected from content, or add them manually:

```bash
brain push --title "Docker Tips" --tags "docker,containers" --file ./tips.md
```

## Discovering Knowledge

See what's new since your last check:

```bash
brain digest
```

Search for specific topics:

```bash
brain search "kubernetes deployment"
```

List all entries:

```bash
brain list
```

## Entry Types

- **guide** — How-to docs, tutorials, runbooks
- **skill** — Reusable patterns, snippets, techniques

## Inviting Teammates

Share the remote URL and have them run:

```bash
brain connect <remote-url>
```

They'll get a full clone with search index built automatically.
