---
title: net9.0 maccatalyst README
author: vraspar
created: '2026-03-30T22:37:04.081Z'
updated: '2026-03-30T22:37:04.081Z'
tags:
  - ort-genai
type: guide
status: active
source_repo: onnxruntime-genai
source_path: nuget/targets/net9.0-maccatalyst/README.md
source_content_hash: 5917d74a31c13e4f08261a5e8a69ae2098683c52db7d12d5b940cf736f8a0027
---
### Notes for maccatalyst .NET targets:

We only add a blank file for the target framework folder here and thus will be including blank TFM under build/ and buildTransitive/ in the Nuget package. The reason is for Mac Catalyst platform, it directly will resolve the xcframework from the runtimes/native/ios folder based on this [RuntimeidentifierGraph](https://github.com/dotnet/sdk/blob/main/src/Layout/redist/PortableRuntimeIdentifierGraph.json#L300-L304)
---
<!-- brain:links (auto-generated, do not edit) -->
**Related:** [[package|PACKAGE]], [[onnxruntime-genai-modelvalidation-readme|model validation README]], [[onnxruntime-genai-python-readme|python README]], [[onnxruntime-genai-models-readme|models README]], [[onnxruntime-genai-android-readme|android README]]
