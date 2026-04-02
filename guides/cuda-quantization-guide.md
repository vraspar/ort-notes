---
title: CUDA Quantization Guide
author: vraspar
created: '2026-04-02T20:21:32.605Z'
updated: '2026-04-02T20:21:32.605Z'
tags:
  - cuda-quantization-guide
  - inference-session
  - gptq-quantizer
  - nference-session
  - ptq-quantizer
  - cuda
  - quantization
  - guide
type: guide
status: active
---
# CUDA Quantization Guide

Use GptqQuantizer and AutoAWQQuantizer for model optimization.

```python
from onnxruntime import InferenceSession
quantizer = GptqQuantizer(model)
```

## Concepts
- INT4 quantization
- ONNX optimization
