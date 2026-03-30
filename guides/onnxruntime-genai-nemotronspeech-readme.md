---
title: NemotronSpeech README
author: vraspar
created: '2026-03-30T22:37:04.055Z'
updated: '2026-03-30T22:37:04.055Z'
tags:
  - api
  - bash
  - dotnet
  - ort-genai
type: guide
status: active
source_repo: onnxruntime-genai
source_path: examples/csharp/NemotronSpeech/README.md
source_content_hash: 87a8c088ad88a11352e8e826e80d207ec6714228665c62f803e9d78a5be58aa5
---
# Nemotron Speech Streaming ASR — C# Example

This example demonstrates real-time streaming speech recognition using the
NVIDIA Nemotron Speech Streaming model with the ONNX Runtime GenAI C# API.

Audio is streamed through the model in chunks (simulating a microphone feed),
and transcribed text is printed incrementally as it becomes available.

## Prerequisites

- .NET 8.0 SDK or later
- ONNX Runtime GenAI C# package ([installation instructions](https://onnxruntime.ai/docs/genai/howto/install))
- A Nemotron Speech Streaming ONNX model (e.g., `nvidia/nemotron-speech-streaming-en-0.6b`)

## Build

```bash
cd examples/csharp/
dotnet build NemotronSpeech -c Release
```

## Run

```bash
cd ./NemotronSpeech/bin/Release/net8.0/
./NemotronSpeech <model_path> <audio_file.wav> [execution_provider]
```

### Arguments

| Argument | Description |
|---|---|
| `model_path` | Path to the Nemotron ONNX model directory |
| `audio_file.wav` | Path to a WAV audio file (any sample rate — resampled automatically) |
| `execution_provider` | *(Optional)* Execution provider: `cpu`, `cuda`, `dml`, or `follow_config` (default: `follow_config`) |

### Example

```bash
# CPU inference
./NemotronSpeech /path/to/nemotron-cpu-int4 /path/to/audio.wav

# CUDA inference
./NemotronSpeech /path/to/nemotron-cuda-int4 /path/to/audio.wav cuda
```

### Output

The example prints transcribed text incrementally as each audio chunk is processed,
followed by a summary with the full transcript, audio duration, wall-clock time,
and real-time factor (RTFx).

```
------------------------------------------------------------
 This is an example of streaming speech recognition...
============================================================
  This is an example of streaming speech recognition using Nemotron.
============================================================
  Audio: 10.50s | Wall: 2.13s | RTFx: 4.93x
```
---
<!-- brain:links (auto-generated, do not edit) -->
**Related:** [[onnxruntime-genai-modelvalidation-readme|model validation README]], [[onnxruntime-genai-csharp-readme|csharp README]], [[package|PACKAGE]], [[onnxruntime-genai-java-readme|java README]], [[onnxruntime-genai-c-readme|c README]]
