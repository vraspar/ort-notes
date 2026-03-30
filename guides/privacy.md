---
title: Privacy
author: vraspar
created: '2026-03-30T22:26:54.660Z'
updated: '2026-03-30T22:26:54.660Z'
tags:
  - api
  - olive
type: guide
status: active
source_repo: olive
source_path: docs/Privacy.md
source_content_hash: 29eae87af0fb16778846b35e475a72b9940dcecbbcf5eeaa97f8c2b857675384
---
# Privacy

## Data Collection
The software may collect information about you and your use of the software and send it to Microsoft. Microsoft may use this information to provide services and improve our products and services. You may turn off the telemetry as described in the repository. There are also some features in the software that may enable Microsoft to collect data from users of your applications. If you use these features, you must comply with applicable law, including providing appropriate notices to users of your applications together with a copy of Microsoft's privacy statement. Our privacy statement can be found [here](https://go.microsoft.com/fwlink/?LinkID=824704). You can learn more about data collection and use in the help documentation and our privacy statement. Your use of the software operates as your consent to these practices.

***

## Technical Details
Olive uses the [OpenTelemetry](https://opentelemetry.io/) API for its implementation. Telemetry is turned ON by default. Based on user consent, this data may be periodically sent to Microsoft servers following GDPR and privacy regulations for anonymity and data access controls. Application, device, and version information is collected automatically.

In addition, Olive may collect additional telemetry data such as:
- Invoked commands
- Performance data
- Exception information

Collection of this additional telemetry can be disabled by adding the `--disable_telemetry` flag to any Olive CLI command, or by setting the `OLIVE_DISABLE_TELEMETRY` environment variable to `1` before running. If telemetry is enabled, but cannot be sent to Microsoft, it will be stored locally and sent when a connection is available. You can override the default cache location by setting the `OLIVE_TELEMETRY_CACHE_PATH` environment variable to a valid file path.
---
<!-- brain:links (auto-generated, do not edit) -->
**Related:** [[privacy-2|Privacy]], [[server|Server]], [[python-interface|Python Interface]], [[olive-reference-index|reference index]], [[how-to-use-python-interface|How to Use Python Interface]]
