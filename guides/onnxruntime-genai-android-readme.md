---
title: android README
author: vraspar
created: '2026-03-30T22:37:04.087Z'
updated: '2026-03-30T22:37:04.087Z'
tags:
  - java
  - ort-genai
type: guide
status: active
source_repo: onnxruntime-genai
source_path: src/java/src/test/android/README.md
source_content_hash: 1a54f651df502686ddd4091d02dc99f89c707df541f2e9fdf49a792d38aee150
---
# Android Test Application for ONNX Runtime GenAI

This directory contains a simple android application for testing the ONNX Runtime GenaI AAR package.

### Test Android Application Overview

This android application is mainly aimed for testing:

- Model used: test/test_models/hf-internal-testing/tiny-random-gpt2-fp32
- Main test file: An android instrumentation test under `app\src\androidtest\java\ai.onnxruntime.genai.example.javavalidator\SimpleTest.kt`
- The main dependency of this application is `onnxruntime-genai` aar package under `app\libs`.
- The onnxruntime dependency is provided by the latest released onnxruntime-android package.
- The MainActivity of this application is set to be empty.

### Requirements

- JDK version 11 or later is required.
- The [Gradle](https://gradle.org/) build system is required for building the APKs used to run [android instrumentation tests](https://source.android.com/compatibility/tests/development/instrumentation). Version 7.5 or newer is required.
  The Gradle wrapper at `java/gradlew[.bat]` may be used.

### Building

Build for Android with the additional  `--build_java` and `--android_run_emulator` options.

e.g.
`./build --android --android_home D:\Android --android_ndk_path D:\Android\ndk\26.3.11579264\ --android_abi x86_64 --ort_home 'path to unzipped onnxruntime-android.aar from https://mvnrepository.com/artifact/com.microsoft.onnxruntime/onnxruntime-android/<version>' --build_java --android_run_emulator`

Please note that you must set the `--android_abi` value to match the local system architecture, as the Android instrumentation test is run on an Android emulator on the local system.

See ../../AndroidBuild.md for more information on building for Android.

#### Build Output

The build will generate two apks which is required to run the test application in `$YOUR_BUILD_DIR/src/java/androidtest/app/build/outputs/apk`:

* `androidTest/debug/app-debug-androidTest.apk`
* `debug/app-debug.apk`

After running the build script, the two apks will be installed on `ort_genai_android` emulator and it will automatically run the test application in an adb shell.
---
<!-- brain:links (auto-generated, do not edit) -->
**Related:** [[onnxruntime-genai-java-readme|java README]], [[android-build-setup|Android Build Setup]], [[onnx-runtime-genai|ONNX Runtime GenAI]], [[package|PACKAGE]], [[onnxruntime-genai-modelvalidation-readme|model validation README]]
