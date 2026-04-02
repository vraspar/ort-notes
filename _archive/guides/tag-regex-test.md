---
title: Tag Regex Test
author: vraspar
created: '2026-04-02T20:37:41.239Z'
updated: '2026-04-02T20:37:41.239Z'
tags:
  - inference-session
  - gptq-quantizer
  - execution-provider
  - model-optimization
  - model
  - optimization
type: guide
status: archived
archived_at: '2026-04-02T20:37:43.867Z'
archived_reason: retracted
---
# Model Optimization

```python
from onnxruntime import InferenceSession
from olive.quantization import GptqQuantizer, AutoAWQQuantizer
session = InferenceSession("model.onnx", providers=["CUDAExecutionProvider"])
quantizer = GptqQuantizer(model)
```
