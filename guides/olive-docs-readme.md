---
title: docs README
author: vraspar
created: '2026-03-30T22:26:54.665Z'
updated: '2026-03-30T22:26:54.665Z'
tags:
  - bash
  - html
  - python
  - olive
type: guide
status: active
source_repo: olive
source_path: docs/README.md
source_content_hash: 8923a9b66ae5e799bb70f7ac3ffbfd968dc4769bf3d78ca2a32e882a37005266
---
# Generating the documentation

To generate the documentation, you first have to build it.

## Pre-requisites

Install Olive. At the root of the code repository:

```bash
pip install -e .
```

Install pip requirements. At `docs`:

```bash
pip install -r requirements.txt
```

## Building the documentation

At `docs`:

```bash
make html
make linkcheck
```

## Previewing the documentation

At `docs/build/html`:

```bash
python -m http.server {port-number}
```

The documentation site will be running at `http://localhost:<port-number>`
---
<!-- brain:links (auto-generated, do not edit) -->
**Related:** [[how-to-install-olive|How To Install Olive]], [[how-to-setup-custom-dataset-for-calibration-and-evaluation|How to Setup Custom Dataset for Calibration and Evaluation]], [[how-to-write-new-olive-workflow|How To Write New Olive workflow]], [[olive-getting-started-getting-started|Getting started]], [[diffusion-model-lora-training|Diffusion Model LoRA Training]]
