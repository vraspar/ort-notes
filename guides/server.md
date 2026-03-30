---
title: Server
author: vraspar
created: '2026-03-30T22:36:12.837Z'
updated: '2026-03-30T22:36:12.837Z'
tags:
  - linux
  - api
  - github
  - ort
type: guide
status: active
source_repo: onnxruntime
source_path: docs/Server.md
source_content_hash: ff4aeea07036069b3c9829c8e78cf1d64803744453f45a1f7fab614cdbe506cd
---
## Build ONNX Runtime Server on Linux

**Deprecation Note: This feature is deprecated and no longer supported.**

Read more about ONNX Runtime Server [here](./ONNX_Runtime_Server_Usage.md).

### Prerequisites

1. [golang](https://golang.org/doc/install)
2. [grpc](https://github.com/grpc/grpc/blob/master/BUILDING.md). Please be aware that the docs at "[https://grpc.io/docs/quickstart/cpp/](https://grpc.io/docs/quickstart/cpp/)" is outdated, because building with make on UNIX systems is deprecated.
3. [re2](https://github.com/google/re2)
4. cmake
5. gcc and g++
6. onnxruntime C API binaries. Please get it from [github releases](https://github.com/microsoft/onnxruntime/releases) then extract it to your "/usr" or "/usr/local" folder.

See [install_server_deps.sh](../tools/ci_build/github/linux/docker/scripts/install_server_deps.sh) for more details.

### Build Instructions
```
cd server
mkdir build
cmake -DCMAKE_BUILD_TYPE=Debug ..
make
```

ONNX Runtime Server supports sending logs to [rsyslog](https://www.rsyslog.com/) daemon. To enable it, please run the cmake command with an additional parameter: `-Donnxruntime_USE_SYSLOG=1`.
---
<!-- brain:links (auto-generated, do not edit) -->
**Related:** [[onnx-runtime-roadmap|ONNX Runtime Roadmap]], [[onnxruntime-ccxx-readme|c cxx README]], [[abi-dev-notes|ABI Dev Notes]], [[privacy-2|Privacy]], [[how-to-use-build-onnx-runtime-server-for-prediction|How to Use build ONNX Runtime Server for Prediction]]
