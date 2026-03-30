---
title: How to Use Python Interface
author: vraspar
created: '2026-03-30T22:26:54.771Z'
updated: '2026-03-30T22:26:54.771Z'
tags:
  - python
  - api
  - olive
type: guide
status: active
source_repo: olive
source_path: docs/source/how-to/python-api.md
source_content_hash: f09ec95429f324a133656b55237bff6706e89f8f77b3d6bca235a392c04ad751
---
# How to Use Python Interface

Olive provides Python API to transform models. See [Python API Reference](../reference/python_api.md) for list of supported APIs.

```python
from olive import run, WorkflowOutput

workflow_output: WorkflowOutput = run("config.json")

# Check if optimization produced any results
if workflow_output.has_output_model():
    # Get the best model overall
    best_model = workflow_output.get_best_candidate()
    print(f"Model path: {best_model.model_path}")
    print(f"Model type: {best_model.model_type}")
    print(f"Device: {best_model.from_device()}")
    print(f"Execution provider: {best_model.from_execution_provider()}")
    print(f"Metrics: {best_model.metrics_value}")
```

## Accessing Metrics and Configuration

```python
# Access metrics for input model
input_metrics = workflow_output.get_input_model_metrics()
```

# Practical Tips

- Use `get_best_candidate()` to quickly obtain the model with the best metrics across all devices
- Use `get_output_models()` to get a list of all optimized models sorted by metrics
- Always verify the existence of specific devices or execution providers before accessing them, since the output model might be empty if a pass run has failed.
- Compare the input model metrics with optimized model metrics to quantify improvements
---
<!-- brain:links (auto-generated, do not edit) -->
**Related:** [[python-interface|Python Interface]], [[olive-reference-index|reference index]], [[olive-how-to-index|how to index]], [[olive-design-documentation|Olive Design Documentation]], [[olive-options|Olive Options]]
