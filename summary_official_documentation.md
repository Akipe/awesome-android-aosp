# Awesome Android AOSP - Official Android AOSP documentation

Summary of both official Android documentation (<https://source.android.com/> & <https://developer.android.com/>) for easily navigate and find resources.

## Contents

- [Contents](#contents)
- [Android Open Source Project](#android-open-source-project)
  - [Getting Started](#getting-started)
    - [About](#about)
    - [Start](#start)
    - [Download](#download)
    - [Build](#build)
    - [Create](#create)
    - [Contribute](#contribute)
    - [Community](#community)
  - [Security](#security)
    - [Security Overview](#security-overview)
    - [Android Security Bulletins](#android-security-bulletins)
    - [Features](#features)
      - [Application Signing](#application-signing)
      - [Authentication](#authentication)
      - [Encryption](#encryption)
      - [Keystore](#keystore)
      - [Identity Credential](#identity-credential)
      - [SELinux](#selinux)
      - [Trusty TEE](#trusty-tee)
      - [Verified Boot](#verified-boot)
    - [Testing](#testing)
    - [Best Practices](#best-practices)
  - [Core Topics](#core-topics)
    - [Architecture](#architecture)
      - [Hardware Abstraction Layer (HAL)](#hardware-abstraction-layer-hal)
      - [Kernel](#kernel)
      - [HIDL (General)](#hidl-general)
      - [HIDL (C++)](#hidl-c)
      - [HIDL (Java)](#hidl-java)
      - [Configuration](#configuration)
      - [Device Tree Overlays](#device-tree-overlays)
      - [Vendor NDK](#vendor-ndk)
      - [Vendor Interface Object](#vendor-interface-object)
      - [AIDL](#aidl)
      - [Bootloader](#bootloader)
      - [Partitions](#partitions)
    - [Audio](#audio)
    - [Camera](#camera)
    - [Connectivity](#connectivity)
    - [Data](#data)
    - [Display](#display)
    - [Fonts](#fonts)
    - [Graphics](#graphics)
    - [Interaction](#interaction)
    - [Media](#media)
    - [Performance](#performance)
    - [Permissions](#permissions)
    - [Power](#power)
    - [Runtime](#runtime)
    - [Settings](#settings)
    - [Storage](#storage)
    - [Virtualization](#virtualization)
    - [Tests](#tests)
      - [Test Development Workflow](#test-development-workflow)
      - [Vendor Test Suite (VTS) 11](#vendor-test-suite-vts-11)
      - [Vendor Test Suite (VTS) 10](#vendor-test-suite-vts-10)
      - [Trade Federation (TF) Test Harness](#trade-federation-tf-test-harness)
      - [Debugging](#debugging)
    - [Updates](#updates)
  - [Compatibility](#compatibility)
    - [Compatibility](#compatibility-1)
    - [Compatibility Test Suite (CTS)](#compatibility-test-suite-cts)
  - [Android Devices](#android-devices)
  - [Reference](#reference)
    - [HIDL](#hidl)
    - [HAL](#hal)
    - [Trade Federation](#trade-federation)
    - [Security Test Suite](#security-test-suite)
- [Android for Developers](#android-for-developers)
  - [Guides](#guides)

## Android Open Source Project

*Accessible at <https://source.android.com/>*

### Getting Started

#### About

* [Set up for Android Development](https://source.android.com/docs/setup/about)
* [Android Software Management](https://source.android.com/docs/setup/about/codelines)
* [Codenames, Tags, and Build Numbers](https://source.android.com/docs/setup/about/build-numbers)
* [Brand Guidelines](https://source.android.com/docs/setup/about/brands)
* [Licenses](https://source.android.com/docs/setup/about/licenses)
* [Frequently asked questions](https://source.android.com/docs/setup/about/faqs)
* [Android 13 release notes](https://source.android.com/docs/setup/about/android-13-release)
* [Android 12 release notes](https://source.android.com/docs/setup/about/android-12-release)
* [Android 11 release notes](https://source.android.com/docs/setup/about/android-11-release)
* [Android 10 release notes](https://source.android.com/docs/setup/about/android-10-release)
* [Android 9 release notes](https://source.android.com/docs/setup/about/p-release-notes)
* [Site updates](https://source.android.com/docs/setup/about/site-updates?version=12)
  
#### Start

* [Android developer codelab](https://source.android.com/docs/setup/start)
* [Android platform glossary](https://source.android.com/docs/setup/start/glossary)
* [Requirements](https://source.android.com/docs/setup/start/requirements)
* [Supporting Older Versions](https://source.android.com/docs/setup/start/older-versions)
* [Establishing a build environment](https://source.android.com/docs/setup/start/initializing)

#### Download

* [Source control tools](https://source.android.com/docs/setup/download)
* [Downloading the Source](https://source.android.com/docs/setup/download/downloading)

#### Build

* [Soong Build System](https://source.android.com/docs/setup/build)
* [Building Android](https://source.android.com/docs/setup/build/building)
* [Android Debug Bridge (ADB)](https://source.android.com/docs/setup/build/adb)
* [Flashing devices](https://source.android.com/docs/setup/build/running)
* [Android flash tool](https://source.android.com/docs/setup/build/flash)
* [Building Kernels](https://source.android.com/docs/setup/build/building-kernels)
* [Implementing Java SDK Library](https://source.android.com/docs/setup/build/java-library)
* [Source Sync Issues](https://source.android.com/docs/setup/build/known-issues)
* [Android Rust Introduction](https://source.android.com/docs/setup/build/rust/building-rust-modules/overview)
* [Android on Bazel](https://source.android.com/docs/setup/build/bazel/introduction)

#### Create
 
* [Source Control Workflow](https://source.android.com/docs/setup/create/coding-tasks)
* [Repo Command Reference](https://source.android.com/docs/setup/create/repo)
* [Adding a New Device](https://source.android.com/docs/setup/create/new-device)
* [Understanding 64-bit Builds](https://source.android.com/docs/setup/create/64-bit-builds)
* [Using Reference Boards](https://source.android.com/docs/setup/create/devices)
* [Generic system images](https://source.android.com/docs/setup/create/gsi)
* Cuttlefish
  * [Cuttlefish Virtual Android Devices](https://source.android.com/docs/setup/create/cuttlefish)
  * [Use Cuttlefish to Launch an AOSP Build](https://source.android.com/docs/setup/create/cuttlefish-use)
  * [Cuttlefish: GPU Graphics Acceleration](https://source.android.com/docs/setup/create/cuttlefish-ref-gpu)
  * [Cuttlefish: Restarting and Resetting](https://source.android.com/docs/setup/create/cuttlefish-restart)
  * [Cuttlefish: Multi-tenancy](https://source.android.com/docs/setup/create/cuttlefish-ref-multi-tenancy)
  * [Testing Connectivity of Multiple Devices](https://source.android.com/docs/setup/create/cuttlefish-connectivity)
  * [Cuttlefish: WebRTC Streaming](https://source.android.com/docs/setup/create/cuttlefish-ref-webrtc)
  * [Cuttlefish Control Panel](https://source.android.com/docs/setup/create/cuttlefish-control-panel)
  * [Cuttlefish: Running Stable CTS](https://source.android.com/docs/setup/create/cuttlefish-cts)
* [Using Android Emulator Virtual Devices](https://source.android.com/docs/setup/create/avd)
* [Compiling with Jack for Android 6.0–8.1](https://source.android.com/docs/setup/create/jack)
* [AndroidX and Jetpack](https://source.android.com/docs/setup/create/androidx-and-jetpack)

#### Contribute

* [Contributing](https://source.android.com/docs/setup/contribute)
* [Project Roles](https://source.android.com/docs/setup/contribute/roles)
* [Code search](https://source.android.com/docs/setup/contribute/code-search)
* [Life of a patch](https://source.android.com/docs/setup/contribute/life-of-a-patch)
* [Submitting patches](https://source.android.com/docs/setup/contribute/submit-patches)
* [Git source editor](https://source.android.com/docs/setup/contribute/source-editor)
* [Viewing patches](https://source.android.com/docs/setup/contribute/view-patches)
* [Android Continuous Integration](https://source.android.com/docs/setup/contribute/dashboard)
* [Life of a bug](https://source.android.com/docs/setup/contribute/life-of-a-bug)
* [Reporting bugs](https://source.android.com/docs/setup/contribute/report-bugs)
* [Coding with respect](https://source.android.com/docs/setup/contribute/respectful-code)
* [AOSP Java code style for contributors](https://source.android.com/docs/setup/contribute/code-style)

#### Community

* [Code of conduct](https://source.android.com/docs/setup/community/cofc)
* [Android community and contacts](https://source.android.com/docs/setup/community)

### Security
  * [Overview](https://source.android.com/docs/security)

#### Security Overview

* [Secure an Android Device](https://source.android.com/docs/security/overview)
* ...

#### Android Security Bulletins

* [Bulletins Home](https://source.android.com/docs/security/bulletin)
* [Android security bulletin](https://source.android.com/docs/security/bulletin/asb-overview)
* ...

#### Features

* [Android Security Features](https://source.android.com/docs/security/features)
* ...
##### Application Signing

* [Application Signing](https://source.android.com/docs/security/features/apksigning)
* ...

##### Authentication

* [Authentication](https://source.android.com/docs/security/features/authentication)
* ...
  
##### Encryption

* [Encryption](https://source.android.com/docs/security/features/encryption)
* [File-Based Encryption](https://source.android.com/docs/security/features/encryption/file-based)
* [Full-Disk Encryption](https://source.android.com/docs/security/features/encryption/full-disk)
* [Metadata Encryption](https://source.android.com/docs/security/features/encryption/metadata)
* [Enabling Adiantum](https://source.android.com/docs/security/features/encryption/adiantum)
* [Hardware-Wrapped Keys](https://source.android.com/docs/security/features/encryption/hw-wrapped-keys)

##### Keystore

* [Hardware-backed Keystore](https://source.android.com/docs/security/features/keystore)
* ...

##### Identity Credential

* [Identity Credential](https://source.android.com/docs/security/features/identity-credentials)

##### SELinux

* [Security-Enhanced Linux in Android](https://source.android.com/docs/security/features/selinux)
* [SELinux concepts](https://source.android.com/docs/security/features/selinux/concepts)
* [Implementing SELinux](https://source.android.com/docs/security/features/selinux/implement)
* [Customizing SELinux](https://source.android.com/docs/security/features/selinux/customize)
* [Building SELinux Policy](https://source.android.com/docs/security/features/selinux/build)
* [Policy Compatibility](https://source.android.com/docs/security/features/selinux/compatibility)
* [Validating SELinux](https://source.android.com/docs/security/features/selinux/validate)
* [Writing SELinux Policy](https://source.android.com/docs/security/features/selinux/device-policy)
* [Writing SELinux Policy](https://source.android.com/docs/security/features/selinux/device-policy)
* ...

##### Trusty TEE

* [Trusty TEE](https://source.android.com/docs/security/features/trusty)
* ...

##### Verified Boot

* [Verified Boot](https://source.android.com/docs/security/features/verifiedboot)
* [Device State](https://source.android.com/docs/security/features/verifiedboot/device-state)
* [Verifying Boot](https://source.android.com/docs/security/features/verifiedboot/verified-boot)
* [Boot Flow](https://source.android.com/docs/security/features/verifiedboot/boot-flow)
* [Implementing dm-verity](https://source.android.com/docs/security/features/verifiedboot/dm-verity)
* [Verifying system_other Partition](https://source.android.com/docs/security/features/verifiedboot/verify-system-other-partition)
* [Android Verified Boot](https://source.android.com/docs/security/features/verifiedboot/avb)

#### Testing

* [Security Testing](https://source.android.com/docs/security/test/fuzz-sanitize)
* ...

#### Best Practices

* [Android Security Best Practices](https://source.android.com/docs/security/best-practices)
* ...

### Core Topics
* [Overview](https://source.android.com/docs/core)

#### Architecture

* [Architecture overview](https://source.android.com/docs/core/architecture)

##### Hardware Abstraction Layer (HAL)

* [Hardware Abstraction Layer (HAL) overview](https://source.android.com/docs/core/architecture/hal)
* ...

##### Kernel

* [Kernel overview](https://source.android.com/docs/core/architecture/kernel)
* [Stable Kernel Releases & Updates](https://source.android.com/docs/core/architecture/kernel/releases)
* [Android Common Kernels](https://source.android.com/docs/core/architecture/kernel/android-common)
* [The Generic Kernel Image (GKI) project](https://source.android.com/docs/core/architecture/kernel/generic-kernel-image)
* [GKI development](https://source.android.com/docs/core/architecture/kernel/gki-dev)
* [GKI Versioning](https://source.android.com/docs/core/architecture/kernel/gki-versioning)
* GKI Release Builds
  * [Generic Kernel Image (GKI) release builds](https://source.android.com/docs/core/architecture/kernel/gki-release-builds)
  * ...
* [Generic Kernel Image (GKI) Release Process](https://source.android.com/docs/core/architecture/kernel/gki-releases)
* [Maintain a stable Kernel Module Interface (KMI)](https://source.android.com/docs/core/architecture/kernel/stable-kmi)
* [Android Kernel ABI Monitoring](https://source.android.com/docs/core/architecture/kernel/abi-monitor)
* Modules
  * [Kernel modules overview](https://source.android.com/docs/core/architecture/kernel/modules)
  * [Configure kernel features as GKI modules](https://source.android.com/docs/core/architecture/kernel/convert-or-add)
  * [Vendor module guidelines](https://source.android.com/docs/core/architecture/kernel/vendor-module-guidelines)
  * [Loadable Kernel Modules](https://source.android.com/docs/core/architecture/kernel/loadable-kernel-modules)
  * [Kernel Module Support](https://source.android.com/docs/core/architecture/kernel/kernel-module-support)
  * [Test GKI modules](https://source.android.com/docs/core/architecture/kernel/test-kernel)
* [Boot Time Optimization](https://source.android.com/docs/core/architecture/kernel/boot-time-opt)
* [Debugging](https://source.android.com/docs/core/architecture/kernel/debugging-with-gki)
* [Develop Kernel Code for GKI](https://source.android.com/docs/core/architecture/kernel/kernel-code)
* [Android Kernel File System Support](https://source.android.com/docs/core/architecture/android-kernel-file-system-support)
* [Extending the Kernel with eBPF](https://source.android.com/docs/core/architecture/kernel/bpf)
* [Using DebugFS in Android 12](https://source.android.com/docs/core/architecture/kernel/using-debugfs-12)
* [FIPS 140-3 certifiable GKI crypto module](https://source.android.com/docs/core/architecture/kernel/gki-fips140-module)
* [Android kernel frequently asked questions](https://source.android.com/docs/core/architecture/kernel/gki-faq)
* GKI 1.0
  * [GKI 1.0 overview](https://source.android.com/docs/core/architecture/kernel/gki1-overview)
  * [GKI 1.0: Compatibility Testing](https://source.android.com/docs/core/architecture/kernel/gki-compat-test-1.0)
* Previous Kernels (<=4.19)
  * [Previous kernels (<=4.19)](https://source.android.com/docs/core/architecture/kernel/previous-kernel-overview)
  * [Linux-stable Merges](https://source.android.com/docs/core/architecture/kernel/linux-stable-merges)
  * [Kernel Hardening](https://source.android.com/docs/core/architecture/kernel/hardening)
  * [Android Live-LocK Daemon (llkd)](https://source.android.com/docs/core/architecture/kernel/llkd)
  * [Kernel Configuration](https://source.android.com/docs/core/architecture/kernel/config)
  * [Interface Requirements](https://source.android.com/docs/core/architecture/kernel/reqs-interfaces)
  * [Incremental File System](https://source.android.com/docs/core/architecture/kernel/incfs)
  * [Kernel Networking Unit Tests](https://source.android.com/docs/core/architecture/kernel/network_tests)
  * Modular Kernels
    * [Mounting Partitions Early](https://source.android.com/docs/core/architecture/kernel/mounting-partitions-early)
    * [DTO Support](https://source.android.com/docs/core/architecture/kernel/dto-support)
  * [Ion ABI Changes](https://source.android.com/docs/core/architecture/kernel/ion_abi_changes)
  * [Modularizing ION Heaps for GKI](https://source.android.com/docs/core/architecture/kernel/ion_abi_changes)
  * [Transitioning from ION to DMA-BUF Heaps](https://source.android.com/docs/core/architecture/kernel/ion_abi_changes)
  * [Core Kernel Requirements](https://source.android.com/docs/core/architecture/kernel/ion_abi_changes)
* [EROFS](https://source.android.com/docs/core/architecture/kernel/ion_abi_changes)

##### HIDL (General)

* [HIDL](https://source.android.com/docs/core/architecture/hidl)
* ...

##### HIDL (C++)

* [HIDL C++](https://source.android.com/docs/core/architecture/hidl-cpp)
* ...

##### HIDL (Java)

* [HIDL Java](https://source.android.com/docs/core/architecture/hidl-java)
* ...

##### Configuration

* [Configuration overview](https://source.android.com/docs/core/architecture/configuration)
* ...

##### Device Tree Overlays

* [Device tree overlays](https://source.android.com/docs/core/architecture/dto)
* ...

##### Vendor NDK

* [Vendor Native Development Kit (VNDK) overview](https://source.android.com/docs/core/architecture/vndk)
* ...

##### Vendor Interface Object

* [Vendor Interface Object](https://source.android.com/docs/core/architecture/vintf)
* ...

##### AIDL

* [AIDL Overview](https://source.android.com/docs/core/architecture/aidl)
* ...
* [AIDL for HALs](https://source.android.com/docs/core/architecture/aidl/aidl-hals)
* ...

##### Bootloader

* [Bootloader overview](https://source.android.com/docs/core/architecture/bootloader)
* ...

##### Partitions

* [Overview](https://source.android.com/docs/core/architecture/partitions)

#### Audio

* [Audio](https://source.android.com/docs/core/audio)
* ...

#### Camera

* [Camera](https://source.android.com/docs/core/camera)
* ...

#### Connectivity

* [Connectivity](https://source.android.com/docs/core/connect)
* ...

#### Data

* [Android data use](https://source.android.com/docs/core/data)
* ...

#### Display

* [Android display](https://source.android.com/docs/core/display)
* ...

#### Fonts

* [Implementing Custom Font Fallback](https://source.android.com/docs/core/fonts/custom-font-fallback)

#### Graphics

* [Graphics](https://source.android.com/docs/core/graphics)
* ...

#### Interaction

* [Interaction in Android](https://source.android.com/docs/core/interaction)
* ...

#### Media

* [Media](https://source.android.com/docs/core/media)
* ...

#### Performance

* [Android Performance Optimization](https://source.android.com/docs/core/perf)
* ...
* [Optimizing Boot Times](https://source.android.com/docs/core/perf/boot-times)
* ...

#### Permissions

* [Android Permissions](https://source.android.com/docs/core/permissions)
* ...

#### Power

* [Power Profiles for Android](https://source.android.com/docs/core/power)
* ...

#### Runtime

* [Android Runtime (ART) and Dalvik](https://source.android.com/docs/core/runtime)
* ...

#### Settings

* [Android Settings Menu](https://source.android.com/docs/core/settings)
* ...

#### Storage

* [Storage](https://source.android.com/docs/core/storage)
* ...

#### Virtualization

* [Android Virtualization Framework (AVF) overview](https://source.android.com/docs/core/virtualization)
* ...

#### Tests

* [Android Platform Testing](https://source.android.com/docs/core/tests)

##### Test Development Workflow

* [Test Development Workflow](https://source.android.com/docs/core/tests/development)
* ...

##### Vendor Test Suite (VTS) 11

* [Vendor Test Suite (VTS) and infrastructure](https://source.android.com/docs/core/tests/vts)
* ...

##### Vendor Test Suite (VTS) 10

* [Vendor Test Suite (VTS) & infrastructure for Android 10 and lower](https://source.android.com/docs/core/tests/vts/index10)
* ...

##### Trade Federation (TF) Test Harness

* Getting Started
  * [Trade Federation Overview](https://source.android.com/docs/core/tests/tradefed)
  * ...
* Testing with TF
  * [Write and Run Tradefed Tests](https://source.android.com/docs/core/tests/tradefed/testing)
  * ...
* Developing TF
  * [Developing Tradefed](https://source.android.com/docs/core/tests/tradefed/development)
  * ...
* Architecture
  * [Overview of Trade Federation Architecture](https://source.android.com/docs/core/tests/tradefed/architecture)
  * ...

##### Debugging

* [Debugging Native Android Platform Code](https://source.android.com/docs/core/tests/debug)
* [Reading bug reports](https://source.android.com/docs/core/tests/debug/read-bug-reports)
* [Understanding Logging](https://source.android.com/docs/core/tests/debug/understanding-logging)
* [Implementing Scoped Vendor Logging](https://source.android.com/docs/core/tests/debug/scoped-vendor-logging)
* [Diagnosing Native Crashes](https://source.android.com/docs/core/tests/debug/native-crash)
* Evaluating Performance
  * [Evaluating Performance](https://source.android.com/docs/core/tests/debug/eval_perf)
  * [Understanding Systrace](https://source.android.com/docs/core/tests/debug/systrace)
  * [Using ftrace](https://source.android.com/docs/core/tests/debug/ftrace)
  * [Identifying Capacity-Related Jank](https://source.android.com/docs/core/tests/debug/jank_capacity)
  * [Identifying Jitter-Related Jank](https://source.android.com/docs/core/tests/debug/jank_jitter)
* Feature Implementation
  * [Implementing Test Harness Mode](https://source.android.com/docs/core/tests/debug/harness)
* [Using Debuggers](https://source.android.com/docs/core/tests/debug/gdb)
* [Debugging Native Memory Use](https://source.android.com/docs/core/tests/debug/native-memory)
* [Network Connectivity Tests](https://source.android.com/docs/core/connect/connect_tests)
* [Rescue Party](https://source.android.com/docs/core/tests/debug/rescue-party)
* [Implementing storaged](https://source.android.com/docs/core/tests/debug/storaged)
* [Using Strace](https://source.android.com/docs/core/tests/debug/strace)

#### Updates

* [OTA Updates](https://source.android.com/docs/core/ota)
* ...
  
### Compatibility

* [Overview](https://source.android.com/docs/compatibility)

#### Compatibility

* [Android Compatibility Program Overview](https://source.android.com/docs/compatibility/overview)
* [Android Compatibility Definition Document (CDD)](https://source.android.com/docs/compatibility/cdd)
* ...

#### Compatibility Test Suite (CTS)

* [Compatibility Test Suite](https://source.android.com/docs/compatibility/cts)
* ...

### Android Devices

* [Overview](https://source.android.com/docs/devices)
* ...

### Reference

* [Overview](https://source.android.com/reference)

#### HIDL

* [Documentation for HIDL interfaces](https://source.android.com/reference/hidl)

#### HAL

* [Android HAL Reference (legacy)](https://source.android.com/reference/hal)
* [Data Structures](https://source.android.com/reference/hal/annotated)
* [Data Structure Index](https://source.android.com/reference/hal/classes)
* [Data Fields](https://source.android.com/reference/hal/functions)
* [File List](https://source.android.com/reference/hal/files)
* [Globals](https://source.android.com/reference/hal/globals)
* [Deprecated List](https://source.android.com/reference/hal/deprecated)

#### Trade Federation

* [Class Index](https://source.android.com/reference/tradefed/classes)
* [Package Index](https://source.android.com/reference/tradefed/packages)
* ...

#### Security Test Suite

* [Class Index](https://source.android.com/reference/sts/classes)
* [Package Index](https://source.android.com/reference/sts/packages)
* ...

## Android for Developers

*Accessible at <https://developer.android.com/*

### Guides

* Introduction
  * ...
* Build your project
  * ...
  * ndk-build
    * ...
    * [Android.mk](https://developer.android.com/ndk/guides/android_mk)
    * ...
* [Capture a system trace on the command line](https://developer.android.com/topic/performance/tracing/command-line)
* [Capture a system trace on a device](https://developer.android.com/topic/performance/tracing/on-device)
* [The Android Profiler](https://developer.android.com/studio/profile/android-profiler)
* [Environment variables](https://developer.android.com/studio/command-line/variables)
* [Inspect CPU activity with CPU Profiler](https://developer.android.com/studio/profile/cpu-profiler)
* [Analyze with Profile GPU Rendering](https://developer.android.com/topic/performance/rendering/profile-gpu)
* [Inspect GPU rendering speed and overdraw](https://developer.android.com/topic/performance/rendering/inspect-gpu-rendering)
