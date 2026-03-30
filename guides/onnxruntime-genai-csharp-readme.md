---
title: csharp README
author: vraspar
created: '2026-03-30T22:37:04.057Z'
updated: '2026-03-30T22:37:04.057Z'
tags:
  - bash
  - dotnet
  - linux
  - ort-genai
type: guide
status: active
source_repo: onnxruntime-genai
source_path: examples/csharp/README.md
source_content_hash: b031335ae1a5a0db8f159e78048674b308d1dafda554ce40e7a7782130c865bf
---
# ONNX Runtime GenAI C# Examples

> 📝 **Note:** The examples from the main branch of this repository are compatible with the binaries built from the same commit. Therefore, if using the example from `main`, ONNX Runtime GenAI needs to be built from source. If this is your scenario, just build the library and the examples will be auto built along with the library. If this is not your scenario, please use prebuilt binaries from the release you're interested in and use the examples from the same version tag and follow the steps below.

## Install ONNX Runtime GenAI

Install the C# package according to the [installation instructions](https://onnxruntime.ai/docs/genai/howto/install) or [build from source](https://onnxruntime.ai/docs/genai/howto/build-from-source.html).

## Download a Model

There are many places to obtain a model. Please read through [our download options](https://github.com/microsoft/onnxruntime-genai/blob/main/docs/DownloadModels.md).

## Build an Example

```bash
# Prerequisite: navigate to the C# examples folder
cd examples/csharp/
```

ModelChat:

```bash
# Change `Release` to your desired target. This is just an example.
dotnet build ModelChat -c Release
```

ModelMM:

```bash
# Change `Release` to your desired target. This is just an example.
dotnet build ModelMM -c Release
```

## Run an Example

1. On Windows:

```powershell
# Prerequisite: navigate to the compiled binaries. This is an example. Your navigation may change depending on your target.
cd ./ModelChat/bin/Debug/net8.0/

# The `model-chat` script allows for multi-turn conversations.
.\ModelChat.exe -m {path to model folder} -e {execution provider}
```

```powershell
# Prerequisite: navigate to the compiled binaries. This is an example. Your navigation may change depending on your target.
cd ./ModelMM/bin/Debug/net8.0/

# The `model-mm` script works for multi-modal models and streams the output text token by token.
.\ModelMM.exe -m {path to model folder} -e {execution provider}
```

2. On Linux and macOS:

```bash
# Prerequisite: navigate to the compiled binaries. This is an example. Your navigation may change depending on your target.
cd ./ModelChat/bin/Debug/net8.0/

# The `model-chat` script allows for multi-turn conversations.
./ModelChat -m {path to model folder} -e {execution provider}
```

```bash
# Prerequisite: navigate to the compiled binaries. This is an example. Your navigation may change depending on your target.
cd ./ModelMM/bin/Debug/net8.0/

# The `model-mm` script works for multi-modal models and streams the output text token by token.
./ModelMM -m {path to model folder} -e {execution provider}
```

## Tool Calling

Please read through [our constrained decoding](https://github.com/microsoft/onnxruntime-genai/blob/main/docs/ConstrainedDecoding.md) options to learn more.

Here are some examples of how you can run the C# examples with function/tool calling.

```
# Using JSON Schema with only tool call output
.\ModelChat.exe -m {path to model folder} -e {execution provider} --response_format json_schema --tools_file {path to json file} --tool_output --tool_call_start "{starting tool call token}" --tool_call_end "{ending tool call token}"

# Using Lark Grammar with only tool call output
.\ModelMM.exe -m {path to model folder} -e {execution provider} --response_format lark_grammar --tools_file {path to json file} --tool_output --tool_call_start "{starting tool call token}" --tool_call_end "{ending tool call token}"

# Using Lark Grammar with text or tool call output
.\ModelChat.exe -m {path to model folder} -e {execution provider} --response_format lark_grammar --tools_file {path to json file} --text_output --tool_output --tool_call_start "{starting tool call token}" --tool_call_end "{ending tool call token}"
```
---
<!-- brain:links (auto-generated, do not edit) -->
**Related:** [[onnxruntime-genai-nemotronspeech-readme|NemotronSpeech README]], [[onnxruntime-genai-c-readme|c README]], [[onnxruntime-genai-modelvalidation-readme|model validation README]], [[run-the-phi-3-models-with-onnx-runtime-genai|Run the Phi-3 models with ONNX Runtime GenAI]], [[constraineddecoding|ConstrainedDecoding]]
