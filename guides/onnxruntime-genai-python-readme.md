---
title: python README
author: vraspar
created: '2026-03-30T22:37:04.097Z'
updated: '2026-03-30T22:37:04.097Z'
tags:
  - python
  - ort-genai
type: guide
status: active
source_repo: onnxruntime-genai
source_path: test/python/README.md
source_content_hash: fce440917578a55926cef1a98a82515f615519918330b12e00506933fe7d1537
---
To run a test:

python -m pytest -sv test_onnxruntime_genai_api.py -k "<your_test_name>" --test_models ..\test_models

For example:

python -m pytest -sv test_onnxruntime_genai_api.py -k "test_greedy_search" --test_models ..\test_models
---
<!-- brain:links (auto-generated, do not edit) -->
**Related:** [[onnxruntime-genai-modelvalidation-readme|model validation README]], [[onnxruntime-genai-models-readme|models README]], [[design-of-onnx-runtime-genai-model-builder|Design of ONNX Runtime GenAI Model Builder]], [[updating-java-bindings|Updating Java Bindings]], [[onnxruntime-genai-android-readme|android README]]
