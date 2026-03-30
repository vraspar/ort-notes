---
title: ConstrainedDecoding
author: vraspar
created: '2026-03-30T22:37:04.045Z'
updated: '2026-03-30T22:56:14.866Z'
tags:
  - genai
  - constrained-decoding
  - llm
  - inference
type: guide
status: active
source_repo: onnxruntime-genai
source_path: docs/ConstrainedDecoding.md
source_content_hash: f03226e4559770856ef74b1f9e4d8148d2fd22738ee7d583b82279bf2c644b1d
---
## Constrained Decoding

Constrained Decoding is useful when using function/tool calling as it helps in ensuring the output is in the correct format (i.e. ensures structured outputs).

We have integrated [LLGuidance](https://github.com/guidance-ai/llguidance) for constrained decoding. There are three types of constrained decoding enabled right now:
1. Lark Grammar (Recommended): This option allows you to have an option for a regular output as well as function/tool output in JSON format.
2. JSON Schema: Output will be JSON schema and it will be one of the function/tools provided.
3. Regex: If a particular regular expression is desired.

To ensure that the function/tool calling works correctly with constrained decoding, you need to modify your tokenizer.json file. For each model that has its own tool calling token, the tool calling token's `special` attribute needs to be set to true. For example, Phi-4 mini uses the <|tool_call|> and <|/tool_call|> tokens so you should set the `special` attribute for them as `true` inside `tokenizer.json`.
---
<!-- brain:links (auto-generated, do not edit) -->
**Related:** [[onnxruntime-genai-csharp-readme|csharp README]], [[onnxruntime-genai-c-readme|c README]], [[onnx|ONNX]]
