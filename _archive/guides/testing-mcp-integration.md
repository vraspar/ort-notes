---
title: Testing MCP Integration
author: vraspar
created: '2026-03-30T22:49:09.153Z'
updated: '2026-03-30T22:51:22.875Z'
tags:
  - mcp
  - testing
  - integration
  - qa
  - updated
type: guide
status: archived
summary: Updated via MCP update_entry tool
archived_at: '2026-03-30T22:51:25.925Z'
archived_reason: retracted
---
# MCP Integration Testing

This entry verifies the Brain MCP server works correctly when called by an AI agent.

## Key Findings
- The MCP server starts via `brain serve` command
- It uses stdio JSON-RPC transport
- Tool discovery works via `tools/list`
- Resources available via `resources/list`

## Test Scenarios
1. Push a new knowledge entry
2. Search for the pushed entry
3. Get recommendations
4. List all entries
5. Get digest summary
