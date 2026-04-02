---
title: Kubernetes Pod Scheduling
author: vraspar
created: '2026-04-02T20:28:24.322Z'
updated: '2026-04-02T20:28:24.322Z'
tags:
  - kubernetes-pod-scheduling-kubernetes
  - nodes-key-concepts-nodeselector
  - complex-rules-taints
  - api-version
  - node-selector
  - kubernetes
  - assign-pods
  - node-restrictions
type: guide
status: active
---
# Kubernetes Pod Scheduling

Kubernetes uses a scheduler to assign pods to nodes. Key concepts:
- NodeSelector for simple constraints
- Affinity/anti-affinity for complex rules
- Taints and tolerations for node restrictions

```yaml
apiVersion: v1
kind: Pod
metadata:
  name: nginx
spec:
  nodeSelector:
    disktype: ssd
```
