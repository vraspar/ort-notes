---
title: opencv README
author: vraspar
created: '2026-03-30T22:37:04.043Z'
updated: '2026-03-30T22:37:04.043Z'
tags:
  - ort-genai
type: guide
status: active
source_repo: onnxruntime-genai
source_path: cmake/external/opencv/README.md
source_content_hash: c651a339fa28d7642a2a779388911c3c19625a65dcbf1148faa64f3ec629f77a
---
This directory contains a subset of the files in the OpenCV repo at the 4.5.4 tag. In particular:
- https://github.com/opencv/opencv/tree/4.5.4/platforms/ios/cmake/Toolchains
- https://github.com/opencv/opencv/tree/4.5.4/platforms/ios/cmake/Modules/Platform
- https://github.com/opencv/opencv/blob/4.5.4/COPYRIGHT
- https://github.com/opencv/opencv/blob/4.5.4/LICENSE

We duplicate them in this repo in order to use the OpenCV-specific CMake toolchain files for iOS builds.
It's a hacky solution that works for now.
---
<!-- brain:links (auto-generated, do not edit) -->
**Related:** [[onnxruntime-genai-modelvalidation-readme|model validation README]], [[onnxruntime-genai-python-readme|python README]], [[onnxruntime-genai-models-readme|models README]], [[onnxruntime-genai-android-readme|android README]], [[onnxruntime-genai-java-readme|java README]]
