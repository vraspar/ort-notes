---
title: How To Configure Olive Engine
author: vraspar
created: '2026-03-30T22:26:54.731Z'
updated: '2026-03-30T22:26:54.731Z'
tags:
  - azure
  - python
  - olive
type: guide
status: active
source_repo: olive
source_path: docs/source/how-to/configure-workflows/engine-configuration.md
source_content_hash: ac98de6f9bc8c98040a09a559245c804c8a37ffd25296b5e9d0d8c6ba3e8bb21
---
# How To Configure Olive Engine
Engine, in Olive, is the driver of the entire workflow. Engine dictates how a model gets processed, cached, evaluated, and finally packaged. As a developer, you can configure each of these aspects of the engine through the various available options.

## Output configuration

Use `output_dir` option to provide a path to customize where the generated outputs gets saved. For dry runs i.e. process the model but generate no output, set `no_artifacts` option to true.

Below is an example of providing a locally saved ONNX model as input and customizing the output path.
```json
{
    "input_model": {
        "type": "ONNXModel",
        "model_path": "path/to/model.onnx"
    },
    //...
    "no_artifacts": false,
    "output_dir": "path/where/generated/model/gets/saved"
}
```

## Caching configuration

Developers have a few different options to customize caching.
- `cache_dir`: [str]:  Use this option to customize where local caching is saved.
- `cache_config`: [CacheConfig]: Use this option to customize shared i.e. in Azure cloud. Shared cache can be toggled ON and OFF using the `enable_shared_cache` option.
- `enable_shared_cache`: [bool]: Toggle to enable/disable use of shared cache.
- `clean_cache`: [bool]: To clean the local cache on next run, set `clean_cache` to true.
- `clean_evaluation_cache`: [bool]: To force clean only the evaluation results cache, set this to true.

**NOTE**: Don't forget to toggle the `clean_cache` option back to default to avoid force cleaning previously generated cache on each run. Cache helps improve performance and cleaning the cache on each run and degrade performance substantially.

```json
{
    //...
    "cache_dir": "path/to/local/dir",
    "cache_config": {
        "account_name": "account-name",
        "container_name": "container-name",
        "update_shared_cache": true
    },
    "enable_shared_cache": true,
    "clean_cache": false,
    "clean_evaluation_cache": true
    //...
}
```

For detailed discussion on configuring shared cache, see [shared-cache](../../features/azure-ai/shared-model-cache.md).

## Logging configuration

Logging is controlled by four different options, all configurable as input to the engine.
- `log_severity_level`: [int]: Controls verbosity of logging output from Olive.
- `ort_log_severity_level`: [int]: Controls verbosity of logging from use of ONNX runtime.
- `ort_py_log_severity_level`: [int]: Set logging verbosity of ONNX runtime python module.
- `log_to_file`: [str]: Set this to redirect all console logs to a local file.

Developers can configure each of the above three flags to any of the following to control the verbosity of the output log during workflow runs.
- 0: VERBOSE (or DEBUG)
- 1: INFO
- 2: WARNING
- 3: ERROR
- 4: FATAL (or CRITICAL)

```json
{
    //...
    "log_severity_level": 2,
    "ort_log_severity_level": 3,
    "ort_py_log_severity_level": 3,
    "log_to_file": "path/to/a/local/file"
}
```

**NOTE**: If `log_to_file` is a relative path, it is considered relative to the current working directory.
---
<!-- brain:links (auto-generated, do not edit) -->
**Related:** [[shared-cache|Shared Cache]], [[python-interface|Python Interface]], [[olive-options|Olive Options]], [[how-to-install-olive|How To Install Olive]], [[olive-design|Olive Design]]
