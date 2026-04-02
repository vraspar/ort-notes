---
title: Docker Container Networking
author: vraspar
created: '2026-04-02T20:28:55.264Z'
updated: '2026-04-02T20:28:55.264Z'
tags:
  - container-communication-bridge-network
  - network-driver-containers
  - containers-network-isolation
  - flag-dns-resolution
  - docker-container-networking
  - networking-drivers
  - custom-bridges
  - docker
type: guide
status: archived
archived_at: '2026-04-02T20:29:16.123Z'
archived_reason: retracted
---
# Docker Container Networking

## Overview
Docker provides several networking drivers for container communication.

## Bridge Network
The default network driver. Containers on the same bridge can communicate.

```bash
docker network create my-network
docker run --network my-network --name web nginx
docker run --network my-network --name api node:18
```

## Key Concepts
- Port mapping with -p flag
- DNS resolution between containers
- Network isolation with custom bridges
---
<!-- brain:links (auto-generated, do not edit) -->
**Related:** [[overview|Overview]]
