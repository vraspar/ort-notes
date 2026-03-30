---
title: c cxx README
author: vraspar
created: '2026-03-30T22:36:12.777Z'
updated: '2026-03-30T22:36:12.777Z'
tags:
  - api
  - github
  - ort
type: guide
status: active
source_repo: onnxruntime
source_path: docs/c_cxx/README.md
source_content_hash: 40c933fabc00733e71addbe200609fcd544250c595ed934c6b2ea4b379aaf09e
---
# ONNX Runtime C/C++ docs source files

This directory contains doxygen configuration to generate the C/C++ API docs for ONNX Runtime.

The actual generation is performed by a GitHub actions workflow: [publish-c-apidocs.yml](../../.github/workflows/publish-c-apidocs.yml).

# C/C++ API Documentation Conventions

## Handling API changes across versions
When a new API is added or an existing API is changed, indicate this in the API's documentation with the Doxygen `\since` command.
This lets readers know the availability and behavior in different versions.

For a new API in version X, add `\since Version X.`. If an API's behavior changes in version Y, add `\since Version Y: <change description>`.
Put each API change entry for a version on its own line.

For example:
```c++
/**
 * \brief My API function.
 * \since Version X.
 * \since Version Y: Does things differently.
 */
void MyApi();
```
---
<!-- brain:links (auto-generated, do not edit) -->
**Related:** [[server|Server]], [[onnx-runtime-roadmap|ONNX Runtime Roadmap]], [[contributing-to-windows-ml|Contributing to Windows ML]], [[versioning|Versioning]], [[privacy-2|Privacy]]
