---
title: PyTorch
author: vraspar
created: '2026-03-30T22:26:54.699Z'
updated: '2026-03-30T22:26:54.699Z'
tags:
  - olive
type: guide
status: active
source_repo: olive
source_path: docs/source/features/model-conversion/convert-pytorch.md
source_content_hash: 917dd394439ac1f91f0f198f11a5f96e419c4f18debaf98e0707d93d6ced6f9c
---
# PyTorch

PyTorch is an optimized tensor library for deep learning using GPUs and CPUs.

## TorchTRTConversion
`TorchTRTConversion` converts the `torch.nn.Linear` modules in the transformer layers in a Hugging Face PyTorch model to `TRTModules` from `torch_tensorrt` with fp16 precision and sparse weights, if
applicable. `torch_tensorrt` is an extension to `torch` where TensorRT compiled engines can be used like regular `torch.nn.Module`s. This pass can be used to accelerate inference on transformer models
with sparse weights by taking advantage of the 2:4 structured sparsity pattern supported by TensorRT.

This pass only supports HfModels. Please refer to [TorchTRTConversion](torch_trt_conversion) for more details on the types of transformers models supported.

### Example Configuration
```json
{
    "type": "TorchTRTConversion"
}
```
---
<!-- brain:links (auto-generated, do not edit) -->
**Related:** [[overview|Overview]], [[python-interface|Python Interface]], [[olive-options|Olive Options]], [[olive-how-to-index|how to index]], [[how-to-define-input-model-for-a-new-workflow|How to Define Input Model for a New Workflow]]
