# Official Android AOSP documentation

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
      - [Input](#input)
      - [Haptics](#haptics)
      - [Neural Networks](#neural-networks)
      - [Peripherals](#peripherals)
      - [Sensors](#sensors)
      - [Context Hub Runtime Environment](#context-hub-runtime-environment)
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
* [HIDL Framework Backwards Compatibility Verification](https://source.android.com/docs/core/architecture/hal/framework-testing)
* [Dynamically Available HALs](https://source.android.com/docs/core/architecture/hal/dynamic-lifecycle)
* Archive
* [Legacy HALs](https://source.android.com/docs/core/architecture/hal/archive)

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
* [Interfaces & Packages](https://source.android.com/docs/core/architecture/hidl/interfaces)
* [Interface Hashing](https://source.android.com/docs/core/architecture/hidl/hashing)
* [Services & Data Transfer](https://source.android.com/docs/core/architecture/hidl/services)
* [Fast Message Queue (FMQ)](https://source.android.com/docs/core/architecture/hidl/fmq)
* [Using Binder IPC](https://source.android.com/docs/core/architecture/hidl/binder-ipc)
* [HIDL Memory Block](https://source.android.com/docs/core/architecture/hidl/memoryblock)
* [Network Stack Configuration Tools](https://source.android.com/docs/core/architecture/hidl/network-stack)
* [Threading Models](https://source.android.com/docs/core/architecture/hidl/threading)
* [Converting HAL Modules](https://source.android.com/docs/core/architecture/hidl/converting)
* [Data Types](https://source.android.com/docs/core/architecture/hidl/types)
* [Safe Union](https://source.android.com/docs/core/architecture/hidl/safe_union)
* [Versioning](https://source.android.com/docs/core/architecture/hidl/versioning)
* [Code Style Guide](https://source.android.com/docs/core/architecture/hidl/code-style)

##### HIDL (C++)

* [HIDL C++](https://source.android.com/docs/core/architecture/hidl-cpp)
* [Packages](https://source.android.com/docs/core/architecture/hidl-cpp/packages)
* [Interfaces](https://source.android.com/docs/core/architecture/hidl-cpp/interfaces)
* [Data Types](https://source.android.com/docs/core/architecture/hidl-cpp/types)
* [Functions](https://source.android.com/docs/core/architecture/hidl-cpp/functions)

##### HIDL (Java)

* [HIDL Java](https://source.android.com/docs/core/architecture/hidl-java)
* [Data Types](https://source.android.com/docs/core/architecture/hidl-java/types)
* [Interface Methods & Errors](https://source.android.com/docs/core/architecture/hidl-java/interfaces)
* [Exporting Constants](https://source.android.com/docs/core/architecture/hidl-java/constants)

##### Configuration

* [Configuration overview](https://source.android.com/docs/core/architecture/configuration)
* [Implementing System Properties as APIs](https://source.android.com/docs/core/architecture/configuration/sysprops-apis)
* [Add System Properties](https://source.android.com/docs/core/architecture/configuration/add-system-properties)
* [Implementing Config File Schema API](https://source.android.com/docs/core/architecture/configuration/config-file-schema-api)
* Archive
  * [ConfigStore HAL](https://source.android.com/docs/core/architecture/configuration/archive)
  * [ConfigStore](https://source.android.com/docs/core/architecture/configuration/archive/config-store)
  * [Creating the HAL Interface](https://source.android.com/docs/core/architecture/configuration/archive/interface)
  * [Implementing the Servic](https://source.android.com/docs/core/architecture/configuration/archive/service)
  * [Client-Side Usage](https://source.android.com/docs/core/architecture/configuration/archive/client)
  * [Adding ConfigStore Classes and Items](https://source.android.com/docs/core/architecture/configuration/archive/add-class-item)

##### Device Tree Overlays

* [Device tree overlays](https://source.android.com/docs/core/architecture/dto)
* [Implementing DTOs](https://source.android.com/docs/core/architecture/dto/implement)
* [DTO Syntax](https://source.android.com/docs/core/architecture/dto/syntax)
* [Compiling & Verifying](https://source.android.com/docs/core/architecture/dto/compile)
* [Using Multiple DTs](https://source.android.com/docs/core/architecture/dto/multiple)
* [DTB/DTBO Partitions](https://source.android.com/docs/core/architecture/dto/partitions)
* [Optimizing DTOs](https://source.android.com/docs/core/architecture/dto/optimize)

##### Vendor NDK

* [Vendor Native Development Kit (VNDK) overview](https://source.android.com/docs/core/architecture/vndk)
* [Enabling the VNDK](https://source.android.com/docs/core/architecture/vndk/enabling)
* [VNDK Build System Support](https://source.android.com/docs/core/architecture/vndk/build-system)
* [VNDK Extensions](https://source.android.com/docs/core/architecture/vndk/extensions)
* [VNDK Snapshot Design](https://source.android.com/docs/core/architecture/vndk/snapshot-design)
* [Generating VNDK Snapshots](https://source.android.com/docs/core/architecture/vndk/snapshot-generate)
* [Generating Vendor Snapshots](https://source.android.com/docs/core/architecture/vndk/snapshot-vendor)
* [Linker Namespace](https://source.android.com/docs/core/architecture/vndk/linker-namespace)
* [Directories, Rules, and sepolicy](https://source.android.com/docs/core/architecture/vndk/dir-rules-sepolicy)
* [Renderscript](https://source.android.com/docs/core/architecture/vndk/renderscript)
* [ABI Stability](https://source.android.com/docs/core/architecture/vndk/abi-stability)
* [Prebuilt ABI Usages Checker](https://source.android.com/docs/core/architecture/vndk/abi-use-check)

##### Vendor Interface Object

* [Vendor Interface Object](https://source.android.com/docs/core/architecture/vintf)
* [Manifests](https://source.android.com/docs/core/architecture/vintf/objects)
* [Compatibility Matrixes](https://source.android.com/docs/core/architecture/vintf/comp-matrices)
* [FCM Lifecycle](https://source.android.com/docs/core/architecture/vintf/fcm)
* [Device Manifest Development](https://source.android.com/docs/core/architecture/vintf/dm)
* [Matching Rules](https://source.android.com/docs/core/architecture/vintf/match-rules)
* [Additional Resources](https://source.android.com/docs/core/architecture/vintf/resources)

##### AIDL

* [AIDL Overview](https://source.android.com/docs/core/architecture/aidl)
* [AIDL Language](https://source.android.com/docs/core/architecture/aidl/aidl-language)
* [AIDL Backends](https://source.android.com/docs/core/architecture/aidl/aidl-backends)
* [Stable AIDL](https://source.android.com/docs/core/architecture/aidl/stable-aidl)
* [AIDL for HALs](https://source.android.com/docs/core/architecture/aidl/aidl-hals)
* [Running AIDL Services Dynamically](https://source.android.com/docs/core/architecture/aidl/dynamic-aidl)
* [Annotations in AIDL](https://source.android.com/docs/core/architecture/aidl/aidl-annotations)
* [Fast Message Queue with AIDL](https://source.android.com/docs/core/architecture/aidl/fmq)
* [AIDL Fuzzing](https://source.android.com/docs/core/architecture/aidl/aidl-fuzzing)

##### Bootloader

* [Bootloader overview](https://source.android.com/docs/core/architecture/bootloader)
* [Canonical Boot Reason](https://source.android.com/docs/core/architecture/bootloader/boot-reason)
* [Boot Image Header](https://source.android.com/docs/core/architecture/bootloader/boot-image-header)
* [Implementing Bootconfig in Android 12](https://source.android.com/docs/core/architecture/bootloader/implementing-bootconfig)
* [Recovery Images](https://source.android.com/docs/core/architecture/bootloader/recovery-images)
* [DTB Images](https://source.android.com/docs/core/architecture/bootloader/dtb-images)
* [Supporting OTA Updates](https://source.android.com/docs/core/architecture/bootloader/updating)
* [Locking/Unlocking the Bootloader](https://source.android.com/docs/core/architecture/bootloader/locking_unlocking)
* [Version Information in AVB properties](https://source.android.com/docs/core/architecture/bootloader/version-info-avb)
* [Moving Fastboot to Userspace](https://source.android.com/docs/core/architecture/bootloader/fastbootd)

##### Partitions

* [Overview](https://source.android.com/docs/core/architecture/partitions)
* [Partition Layout](https://source.android.com/docs/core/architecture/partitions/system-as-root)
* [Vendor Boot Partitions](https://source.android.com/docs/core/architecture/partitions/vendor-boot-partitions)
* [Vendor/ODM DLKM Partition](https://source.android.com/docs/core/architecture/partitions/vendor-odm-dlkm-partition)
* [Android Shared System Image](https://source.android.com/docs/core/architecture/partitions/shared-system-image)
* [Ramdisk Partitions](https://source.android.com/docs/core/architecture/partitions/ramdisk-partitions)
* [Generic Boot Partition](https://source.android.com/docs/core/architecture/partitions/generic-boot)
* [ODM Partitions](https://source.android.com/docs/core/architecture/partitions/odm-partitions)
* [Product Partitions](https://source.android.com/docs/core/architecture/partitions/product-partitions)
* [Implement a GKI module partition](https://source.android.com/docs/core/architecture/partitions/gki-partitions)
* [Enforcing Product Partition Interfaces](https://source.android.com/docs/core/architecture/partitions/product-interfaces)
* [Trusty OS (TOS) Partitions](https://source.android.com/docs/core/architecture/partitions/tos-partitions)

#### Audio

* [Audio](https://source.android.com/docs/core/audio)
* ...

#### Camera

* [Camera](https://source.android.com/docs/core/camera)
* ...

#### Connectivity

* [Connectivity](https://source.android.com/docs/core/connect)
* Bluetooth and NFC
  * [Bluetooth](https://source.android.com/docs/core/connect/bluetooth)
  * [Bluetooth Services](https://source.android.com/docs/core/connect/bluetooth/services)
  * [Bluetooth Low Energy](https://source.android.com/docs/core/connect/bluetooth/ble)
  * [Hearing Aid Audio Support Using Bluetooth LE](https://source.android.com/docs/core/connect/bluetooth/asha)
  * [Bluetooth Low Energy Advertising](https://source.android.com/docs/core/connect/bluetooth/ble_advertising)
  * [Verifying and Debugging](https://source.android.com/docs/core/connect/bluetooth/verifying_debugging)
  * [HCI Requirements](https://source.android.com/docs/core/connect/bluetooth/hci_requirements)
  * [Host Card Emulation of FeliCa](https://source.android.com/docs/core/connect/felica)
  * [NFC Off-Host Payment Synchronization](https://source.android.com/docs/core/connect/offhost-payment-sync)
  * [Presence Calibration Requirements](https://source.android.com/docs/core/connect/presence-requirements)
  * [Secure NFC](https://source.android.com/docs/core/connect/secure-nfc)
  * [Quick Access Wallet](https://source.android.com/docs/core/connect/quick-access-wallet)
* Calling and Messaging
  * [5G Non-Standalone (NSA)](https://source.android.com/docs/core/connect/5g-nsa)
  * [Implementing Block Phone Numbers](https://source.android.com/docs/core/connect/block-numbers)
  * [Call Notifications](https://source.android.com/docs/core/connect/call-notification)
  * [Implementing Emergency Affordance](https://source.android.com/docs/core/connect/emergency-affordance)
  * [Android Emergency Number Database](https://source.android.com/docs/core/connect/emergency-number-db)
  * [Emergency Numbers and Emergency Calling](https://source.android.com/docs/core/connect/emergency-call)
  * [Implementing IMS](https://source.android.com/docs/core/connect/ims)
  * [IMS Service Entitlement](https://source.android.com/docs/core/connect/ims-service-entitlement)
  * [IMS Single Registration](https://source.android.com/docs/core/connect/ims-single-registration)
  * [Phone Account Suggestion](https://source.android.com/docs/core/connect/phone-account-suggestion)
  * [Implementing Real-Time Text](https://source.android.com/docs/core/connect/rtt)
  * [Supporting Third-Party Calling Apps](https://source.android.com/docs/core/connect/third-party-call-apps)
  * [Visual Voicemail](https://source.android.com/docs/core/permissions/voicemail)
* Carrier
  * [Carrier Configuration](https://source.android.com/docs/core/connect/carrier)
  * [5G Network Slicing](https://source.android.com/docs/core/connect/5g-slicing)
  * [APN and CarrierConfig](https://source.android.com/docs/core/connect/update)
  * [Carrier Identification](https://source.android.com/docs/core/connect/carrierid)
  * [Implementing Data Plans](https://source.android.com/docs/core/connect/data-plans)
  * [Device Identifiers](https://source.android.com/docs/core/connect/device-identifiers)
  * eSIM
    * [Implementing eSIM](https://source.android.com/docs/core/connect/esim-overview)
    * [Modem Requirements for eSIM Support](https://source.android.com/docs/core/connect/esim-modem-requirements)
    * [eUICC APIs](https://source.android.com/docs/core/connect/esim-euicc-api)
    * [Multiple Enabled Profiles](https://source.android.com/docs/core/connect/esim-mep)
    * [Handling eUICC API Errors](https://source.android.com/docs/core/connect/esim-error-handling)
    * [Downloadable Test Profiles](https://source.android.com/docs/core/connect/esim-test-profiles)
  * [Multi-Operator Network Support](https://source.android.com/docs/core/connect/multi-operator-networks)
  * [Customizing Device Behavior for Out-of-Balance Users](https://source.android.com/docs/core/connect/oob-users)
  * [RIL Refactoring](https://source.android.com/docs/core/connect/ril)
  * [Small Cell Support](https://source.android.com/docs/core/connect/small-cell)
  * [UICC Carrier Privileges](https://source.android.com/docs/core/connect/uicc)
* Time
  * [Time Overview](https://source.android.com/docs/core/connect/time)
  * [Location Time Zone Detection](https://source.android.com/docs/core/connect/time/location-tz-detection)
  * [Telephony Time Zone Detection](https://source.android.com/docs/core/connect/time/telephony-tz-detection)
  * [GNSS Time Detection](https://source.android.com/docs/core/connect/time/gnss-time-detection)
  * [External Time Detection](https://source.android.com/docs/core/connect/time/external-time-detection)
  * [Time Source Priority](https://source.android.com/docs/core/connect/time-source)
  * [Time Zone Policy and Recommendations](https://source.android.com/docs/core/connect/time/time-zone-policy-recommendations)
  * [Time Zone Rules](https://source.android.com/docs/core/permissions/timezone-rules)
* Ultra-wideband
  * [Ultra-wideband](https://source.android.com/docs/core/connect/uwb)
  * [UWB HAL Interface](https://source.android.com/docs/core/connect/uwb-hal-interface)
* Wi-Fi
  * [Overview](https://source.android.com/docs/core/connect/wifi-overview)
  * [Wi-Fi HAL](https://source.android.com/docs/core/connect/wifi-hal)
  * [Wi-Fi Infrastructure Features](https://source.android.com/docs/core/connect/wifi-infrastructure)
  * [Testing, Debugging, and Tuning Wi-Fi](https://source.android.com/docs/core/connect/wifi-debug)
  * [Carrier Wi-Fi](https://source.android.com/docs/core/connect/carrier-wifi)
  * [MAC Randomization Behavior](https://source.android.com/docs/core/connect/wifi-mac-randomization-behavior)
  * [Implementing MAC Randomization](https://source.android.com/docs/core/connect/wifi-mac-randomization)
  * [Passpoint (Hotspot 2.0)](https://source.android.com/docs/core/connect/wifi-passpoint)
  * [Wi-Fi STA/AP concurrency](https://source.android.com/docs/core/connect/wifi-sta-ap-concurrency)
  * [Wi-Fi STA/STA Concurrency](https://source.android.com/docs/core/connect/wifi-sta-sta-concurrency)
  * [Trust on First Use (TOFU)](https://source.android.com/docs/core/connect/wifi-tofu)
  * [Wi-Fi Aware](https://source.android.com/docs/core/connect/wifi-aware)
  * [Wi-Fi/Cellular Coex Channel Avoidance](https://source.android.com/docs/core/connect/wifi-coex-channel-avoidance)
  * [Wi-Fi Direct](https://source.android.com/docs/core/connect/wifi-direct)
  * [Wi-Fi Easy Connect](https://source.android.com/docs/core/connect/wifi-easy-connect)
  * [Wi-Fi Hotspot (Soft AP)](https://source.android.com/docs/core/connect/wifi-softap)
  * [Wi-Fi AP/AP Concurrency](https://source.android.com/docs/core/connect/wifi-ap-ap-concurrency)
  * [Wi-Fi Low-Latency Mode](https://source.android.com/docs/core/connect/wifi-low-latency)
  * [Android Wi-Fi Network Selection](https://source.android.com/docs/core/connect/wifi-network-selection)
  * [Wi-Fi Preferred Network Offload Scanning](https://source.android.com/docs/core/connect/wifi-scan)
  * [Wi-Fi RTT (IEEE 802.11mc)](https://source.android.com/docs/core/connect/wifi-rtt)
  * [WPA3 and Wi-Fi Enhanced Open](https://source.android.com/docs/core/connect/wifi-wpa3-owe)
* ACTS Tests
  * [ACTS Telephony Tests](https://source.android.com/docs/core/connect/acts)
  * [Advanced ACTS guide](https://source.android.com/docs/core/connect/acts-advanced-guide)
  * [Configuring ACTS Tests](https://source.android.com/docs/core/connect/acts-config)
  * [User Parameters](https://source.android.com/docs/core/connect/acts-user-params)
  * [5G Testing](https://source.android.com/docs/core/connect/acts-5g-testing)
* [Companion Device Profiles](https://source.android.com/docs/core/connect/companion-device-profile)
* [Connectivity Diagnostics API](https://source.android.com/docs/core/connect/connectivity-diagnostics-api)
* [Connectivity User Interface](https://source.android.com/docs/core/connect/connectivity-ui)
* [Network Selection](https://source.android.com/docs/core/connect/network-selection)
* [Signal Strength Reporting](https://source.android.com/docs/core/connect/signal-strength)

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

##### Input

* [Input](https://source.android.com/docs/core/interaction/input)
* [Key layout files](https://source.android.com/docs/core/interaction/input/key-layout-files)
* [Key character map files](https://source.android.com/docs/core/interaction/input/key-character-map-files)
* [Input device configuration files](https://source.android.com/docs/core/interaction/input/input-device-configuration-files)
* [Migration guide](https://source.android.com/docs/core/interaction/input/migration-guide)
* [Keyboard devices](https://source.android.com/docs/core/interaction/input/keyboard-devices)
* [Touch devices](https://source.android.com/docs/core/interaction/input/touch-devices)
* [Getevent](https://source.android.com/docs/core/interaction/input/getevent)
* [Validate keymaps tool](https://source.android.com/docs/core/interaction/input/validate-keymaps)

##### Haptics

* [Haptics](https://source.android.com/docs/core/interaction/haptics)
* [Implementing haptics](https://source.android.com/docs/core/interaction/haptics/haptics-implement)
* [UX foundation for haptic framework](https://source.android.com/docs/core/interaction/haptics/haptics-ux-foundation)
* [Haptics UX design](https://source.android.com/docs/core/interaction/haptics/haptics-ux-design)

##### Neural Networks

* [Neural Networks API Drivers](https://source.android.com/docs/core/interaction/neural-networks)
* [Burst Executions and Fast Message Queues](https://source.android.com/docs/core/interaction/neural-networks/burst-executions)
* [Compilation Caching](https://source.android.com/docs/core/interaction/neural-networks/compilation-caching)
* [Control Flow](https://source.android.com/docs/core/interaction/neural-networks/control-flow)
* [Device Discovery and Assignment](https://source.android.com/docs/core/interaction/neural-networks/device-discovery)
* [Memory Pool](https://source.android.com/docs/core/interaction/neural-networks/memory-pools)
* [NNAPI Driver Implementation Best Practices](https://source.android.com/docs/core/interaction/neural-networks/best-practices)
* [Quality of Service](https://source.android.com/docs/core/interaction/neural-networks/quality-of-service)
* [Vendor Extensions](https://source.android.com/docs/core/interaction/neural-networks/vendor-extensions)

##### Peripherals

* [Android Peripherals and Accessories](https://source.android.com/docs/core/interaction/accessories)
* Audio Accessories
  * [Building audio accessories](https://source.android.com/docs/core/interaction/accessories/audio)
  * 3.5 mm Headset
    * [3.5 mm Headset: Accessory Specification](https://source.android.com/docs/core/interaction/accessories/headset/plug-headset-spec)
    * [3.5 mm Headset Jack: Device Specification](https://source.android.com/docs/core/interaction/accessories/headset/jack-headset-spec)
  * USB Headset
    * [USB Headset: Accessory Specification](https://source.android.com/docs/core/interaction/accessories/headset/usb-headset-spec)
    * [USB-C-to-Analog Audio Adapter](https://source.android.com/docs/core/interaction/accessories/headset/usb-adapter)
    * [USB Headset: Device Specification](https://source.android.com/docs/core/interaction/accessories/headset/usb-device)
  * [Headset Expected Behavior](https://source.android.com/docs/core/interaction/accessories/headset/expected-behavior)
  * [Testing](https://source.android.com/docs/core/interaction/accessories/headset/testing)
* Custom Accessories
  * [Custom Accessories](https://source.android.com/docs/core/interaction/accessories/custom)
  * AOA
    * [Android Open Accessory (AOA)](https://source.android.com/docs/core/interaction/accessories/protocol)
    * [Android Open Accessory Protocol 2.0](https://source.android.com/docs/core/interaction/accessories/aoa2)
    * [Android Open Accessory Protocol 1.0](https://source.android.com/docs/core/interaction/accessories/aoa)
    * [Disabling Data Signaling Over USB](https://source.android.com/docs/core/interaction/accessories/disable-signaling)
  * [Stylus](https://source.android.com/docs/core/interaction/accessories/stylus)

##### Sensors

* [Sensors](https://source.android.com/docs/core/interaction/sensors)
* [Sensor stack](https://source.android.com/docs/core/interaction/sensors/sensor-stack)
* [Sensor types](https://source.android.com/docs/core/interaction/sensors/sensor-types)
* [Interaction](https://source.android.com/docs/core/interaction/sensors/interaction)
* [Head Tracker HID Protocol](https://source.android.com/docs/core/interaction/sensors/head-tracker-hid-protocol)
* Power
  * [Batching](https://source.android.com/docs/core/interaction/sensors/batching)
  * [Power consumption](https://source.android.com/docs/core/interaction/sensors/power-use)
* Modes
  * [Reporting modes](https://source.android.com/docs/core/interaction/sensors/report-modes)
  * [Suspend mode](https://source.android.com/docs/core/interaction/sensors/suspend-mode)
  * [Sensors Off](https://source.android.com/docs/core/interaction/sensors/sensors-off)
* Sensors HAL
  * [Sensors AIDL HAL](https://source.android.com/docs/core/interaction/sensors/sensors-aidl-hal)
  * [Sensors Multi-HAL](https://source.android.com/docs/core/interaction/sensors/sensors-multihal)
  * [Sensors HAL 2](https://source.android.com/docs/core/interaction/sensors/sensors-hal2)
  * [Sensors HAL 1.0](https://source.android.com/docs/core/interaction/sensors/hal-interface)
  * [HAL version deprecation](https://source.android.com/docs/core/interaction/sensors/versioning)

##### Context Hub Runtime Environment

* [Context Hub Runtime Environment (CHRE)](https://source.android.com/docs/core/interaction/contexthub)

#### Media

* [Media](https://source.android.com/docs/core/media)
* [Media modules](https://source.android.com/docs/core/media/media-modules)
* [MediaProvider module](https://source.android.com/docs/core/media/media-provider)
* [Customizing media components](https://source.android.com/docs/core/media/updatable-media)
* [Low latency decoding in MediaCode](https://source.android.com/docs/core/media/low-latency-media)
* [Media framework hardening](https://source.android.com/docs/core/media/framework-hardening)
* [SoC vendor dependencies for media resource manager](https://source.android.com/docs/core/media/soc)
* [OEM dependencies for media resource manager](https://source.android.com/docs/core/media/oem)
* [DRM](https://source.android.com/docs/core/media/drm)
* [Compatible media transcoding](https://source.android.com/docs/core/media/media-transcoding)
* [Exporting Video Encoding Statistics](https://source.android.com/docs/core/media/encoding-stats)

#### Performance

* [Android Performance Optimization](https://source.android.com/docs/core/perf)
* [APK Caching](https://source.android.com/docs/core/perf/apk-caching)
* [Cached Apps Freezer](https://source.android.com/docs/core/perf/cached-apps-freezer)
* [Optimizing Boot Times](https://source.android.com/docs/core/perf/boot-times)
* Health
  * [Android Health](https://source.android.com/docs/core/perf/health)
  * [Implementing Health 2.0](https://source.android.com/docs/core/perf/health/implementation)
  * [Implementing Health 2.1](https://source.android.com/docs/core/perf/health/implementation-2-1)
  * [Deprecating health@1.0](https://source.android.com/docs/core/perf/health/deprecation)
* [Cgroup Abstraction Layer](https://source.android.com/docs/core/perf/cgroups)
* [Low Memory Killer Daemon](https://source.android.com/docs/core/perf/lmkd)
* [Using Profile-Guided Optimization (PGO)](https://source.android.com/docs/core/perf/pgo)
* [Task Snapshots](https://source.android.com/docs/core/perf/task-snapshots)
* [Compatibility WAL (Write-Ahead Logging) for Apps](https://source.android.com/docs/core/perf/compatibility-wal)
* [App Hibernation](https://source.android.com/docs/core/perf/hiber)
* [Performance Boost At Game Loading Time](https://source.android.com/docs/core/perf/boost)
* [MM Events - Historical Memory Statistics](https://source.android.com/docs/core/perf/mmevents-stats)

#### Permissions

* [Android Permissions](https://source.android.com/docs/core/permissions)
* [Ambient Capabilities](https://source.android.com/docs/core/permissions/ambient)
* [Background Location Access Reminder](https://source.android.com/docs/core/permissions/background-location-access)
* [Contacts Provider and Affinities Information](https://source.android.com/docs/core/permissions/contacts-affinities)
* [Discretionary Access Control (DAC)](https://source.android.com/docs/core/permissions/filesystem)
* [Immutable Device IDs](https://source.android.com/docs/core/permissions/immutable-device-ids)
* [Namespaces for Native Libraries](https://source.android.com/docs/core/permissions/namespaces_libraries)
* [Privileged Permission Allowlisting](https://source.android.com/docs/core/permissions/perms-allowlist)
* [Preinstalled System Packages](https://source.android.com/docs/core/permissions/preinstalled-packages)
* [Privacy Indicator](https://source.android.com/docs/core/permissions/privacy-indicators)
* [Restrict Opportunistic Locations](https://source.android.com/docs/core/permissions/restrict-opportunistic-locations)
* [Restricted Screen Reading](https://source.android.com/docs/core/permissions/restricted-screen-reading)
* [Android Roles](https://source.android.com/docs/core/permissions/android-roles)
* [Runtime Permissions](https://source.android.com/docs/core/permissions/runtime_perms)
* [Tristate Location Permissions](https://source.android.com/docs/core/permissions/tristate-perms)
* [Implementing USB HAL](https://source.android.com/docs/core/permissions/usb-hal)
* [Companion App Streaming](https://source.android.com/docs/core/permissions/app-streaming)

#### Power

* [Power Profiles for Android](https://source.android.com/docs/core/power)
* [Power Management](https://source.android.com/docs/core/power/mgmt)
* [Thermal Mitigation](https://source.android.com/docs/core/power/thermal-mitigation)
* [Power Stats HAL](https://source.android.com/docs/core/power/power-stats-hal)
* [App Power Management](https://source.android.com/docs/core/power/app_mgmt)
* [Platform Power Management](https://source.android.com/docs/core/power/platform_mgmt)
* [Performance Management](https://source.android.com/docs/core/power/performance)
* [App background behavior trackers](https://source.android.com/docs/core/power/trackers)
* [Supporting Batteryless Devices](https://source.android.com/docs/core/power/batteryless)
* [Measuring Component Power](https://source.android.com/docs/core/power/component)
* [Measuring Device Power](https://source.android.com/docs/core/power/device)
* [Measuring Power Values](https://source.android.com/docs/core/power/values)
* [Routine Battery Saver](https://source.android.com/docs/core/power/routine-battery-saver)
* [TV Standby](https://source.android.com/docs/core/power/tv-standby)
* [SystemSuspend service](https://source.android.com/docs/core/power/systemsuspend)

#### Runtime

* [Android Runtime (ART) and Dalvik](https://source.android.com/docs/core/runtime)
* ...
* [Change the value of an app's resources at runtime](https://source.android.com/docs/core/runtime/rros)
* ...

#### Settings

* [Android Settings Menu](https://source.android.com/docs/core/settings)
* [Android Settings Design Guidelines](https://source.android.com/docs/core/settings/settings-guidelines)
* [Patterns and Components](https://source.android.com/docs/core/settings/patterns-components)
* [nformation Architecture](https://source.android.com/docs/core/settings/info-architecture)
* [Personalized Settings](https://source.android.com/docs/core/settings/personalized)
* [Universal Search](https://source.android.com/docs/core/settings/universal-search)

#### Storage

* [Storage](https://source.android.com/docs/core/storage)
* [Traditional Storage](https://source.android.com/docs/core/storage/traditional)
* [Adoptable Storage](https://source.android.com/docs/core/storage/adoptable)
* [Scoped Storage](https://source.android.com/docs/core/storage/scoped)
* [FUSE Passthrough](https://source.android.com/docs/core/storage/fuse-passthrough)
* [Device Configuration](https://source.android.com/docs/core/storage/config)
* [Configuration Examples](https://source.android.com/docs/core/storage/config-example)
* [Faster Storage Statistics](https://source.android.com/docs/core/storage/faster-stats)
* [SDCardFS Deprecation](https://source.android.com/docs/core/storage/sdcardfs-deprecate)

#### Virtualization

* [Android Virtualization Framework (AVF) overview](https://source.android.com/docs/core/virtualization)
* ...

#### Tests

* [Android Platform Testing](https://source.android.com/docs/core/tests)

##### Test Development Workflow

* [Test Development Workflow](https://source.android.com/docs/core/tests/development)
* [Simple Build Configuration](https://source.android.com/docs/core/tests/development/blueprints)
* [Complex Test Configuration](https://source.android.com/docs/core/tests/development/test-config)
* Instrumentation Tests
  * [Instrumentation Tests](https://source.android.com/docs/core/tests/development/instrumentation)
  * [Self-Instrumenting Tests Example](https://source.android.com/docs/core/tests/development/instr-self-e2e)
  * [Targeting an Application Example](https://source.android.com/docs/core/tests/development/instr-app-e2e)
* GTest
  * [GoogleTest](https://source.android.com/docs/core/tests/development/gtest)
  * [Adding New GoogleTests (GTests)](https://source.android.com/docs/core/tests/development/gtest-func-e2e)
  * [Metric Tests](https://source.android.com/docs/core/tests/development/metrics)
* [JAR (Java) Host Tests](https://source.android.com/docs/core/tests/development/jar)
* [Test Mapping](https://source.android.com/docs/core/tests/development/test-mapping)
* [Running Tests (Atest)](https://source.android.com/docs/core/tests/development/atest)
* Android Test Station
  * [Android Test Station](https://source.android.com/docs/core/tests/development/android-test-station/ats-user-guide)
  * [Virtual Devices in Android Test Station](https://source.android.com/docs/core/tests/development/android-test-station/ats-virtual-devices)
  * [Auto-enable USB Debugging on User Builds](https://source.android.com/docs/core/tests/development/android-test-station/ats-user-builds)
  * [Running UIConductor tests with ATS](https://source.android.com/docs/core/tests/development/android-test-station/ats-uicd)
  * [Android Test Station API](https://source.android.com/docs/core/tests/development/android-test-station/ats-api)
  * [Android Test Station Release Notes](https://source.android.com/docs/core/tests/development/android-test-station/ats-release-notes)
  * [ATS frequently asked questions](https://source.android.com/docs/core/tests/development/android-test-station/faq)

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
* APEX
  * [APEX File Format](https://source.android.com/docs/core/ota/apex)
  * [Vendor APEX](https://source.android.com/docs/core/ota/vendor-apex)
* [Building OTA Packages](https://source.android.com/docs/core/ota/tools)
* [Signing Builds for Release](https://source.android.com/docs/core/ota/sign_builds)
* [Reducing OTA Size](https://source.android.com/docs/core/ota/reduce_size)
* A/B System Updates
  * [A/B (Seamless) System Updates](https://source.android.com/docs/core/ota/ab)
  * [Implementing A/B Updates](https://source.android.com/docs/core/ota/ab/ab_implement)
  * [Frequently asked questions](https://source.android.com/docs/core/ota/ab/ab_faqs)
* Non-A/B System Updates
  * [Non-A/B System Updates](https://source.android.com/docs/core/ota/nonab)
  * [Block-Based OTAs](https://source.android.com/docs/core/ota/nonab/block)
  * [Inside OTA Packages](https://source.android.com/docs/core/ota/nonab/inside_packages)
  * [Device-Specific Code](https://source.android.com/docs/core/ota/nonab/device_code)
* Dynamic Partitions
  * [Dynamic Partitions](https://source.android.com/docs/core/ota/dynamic_partitions)
  * [Implementing Dynamic Partitions](https://source.android.com/docs/core/ota/dynamic_partitions/implement)
  * [OTA for A/B Devices with Dynamic Partitions](https://source.android.com/docs/core/ota/dynamic_partitions/ab_launch)
  * [OTA for A/B Devices without Dynamic Partitions](https://source.android.com/docs/core/ota/dynamic_partitions/ab_legacy)
  * [OTA for Non-A/B Devices with Dynamic Partitions](https://source.android.com/docs/core/ota/dynamic_partitions/nonab)
  * [How to Size Super](https://source.android.com/docs/core/ota/dynamic_partitions/how_to_size_super)
* Virtual A/B
  * [Virtual A/B Overview](https://source.android.com/docs/core/ota/virtual_ab)
  * [Implementing Virtual A/B](https://source.android.com/docs/core/ota/virtual_ab/implement)
  * [Implementing Virtual A/B - Patches](https://source.android.com/docs/core/ota/virtual_ab/implement-patches)
* [Time Zone Rules](https://source.android.com/docs/core/permissions/timezone-rules)
* [User Data Checkpoint (UDC)](https://source.android.com/docs/core/ota/user-data-checkpoint)
* [Dynamic System Updates](https://source.android.com/docs/core/ota/dynamic-system-updates)
* [Resume-on-Reboot](https://source.android.com/docs/core/ota/resume-on-reboot)
* [Android Upgrade Party for OS updates](https://source.android.com/docs/core/ota/upgrade-party)
* Modular System Components
  * [Modular System Components](https://source.android.com/docs/core/ota/modular-system)
  * [AdServices](https://source.android.com/docs/core/ota/modular-system/adservices)
  * [adbd](https://source.android.com/docs/core/ota/modular-system/adbd)
  * [AppSearch](https://source.android.com/docs/core/ota/modular-system/appsearch)
  * [Android Runtime (ART)](https://source.android.com/docs/core/ota/modular-system/art)
  * [Bluetooth](https://source.android.com/docs/core/ota/modular-system/bluetooth)
  * [CellBroadcast](https://source.android.com/docs/core/ota/modular-system/cellbroadcast)
  * [Conscrypt](https://source.android.com/docs/core/ota/modular-system/conscrypt)
  * [Device Scheduling](https://source.android.com/docs/core/ota/modular-system/scheduling)
  * [DNS Resolver](https://source.android.com/docs/core/ota/modular-system/dns-resolver)
  * [DocumentsUI](https://source.android.com/docs/core/ota/modular-system/documentsui)
  * [ExtServices](https://source.android.com/docs/core/ota/modular-system/extservices)
  * [IPsec/IKEv2 Library](https://source.android.com/docs/core/ota/modular-system/ipsec)
  * [Media](https://source.android.com/docs/core/ota/modular-system/media)
  * [MediaProvider](https://source.android.com/docs/core/ota/modular-system/mediaprovider)
  * [ModuleMetadata](https://source.android.com/docs/core/ota/modular-system/metadata)
  * [Network Stack](https://source.android.com/docs/core/ota/modular-system/networking)
  * [NNAPI Runtime](https://source.android.com/docs/core/ota/modular-system/nnapi)
  * [OnDevicePersonalization](https://source.android.com/docs/core/ota/modular-system/ondevicepersonalization)
  * [PermissionController](https://source.android.com/docs/core/ota/modular-system/permissioncontroller)
  * [SDK Extensions](https://source.android.com/docs/core/ota/modular-system/sdk-extension)
  * [Statsd](https://source.android.com/docs/core/ota/modular-system/statsd)
  * [Tethering](https://source.android.com/docs/core/ota/modular-system/tethering)
  * [Time Zone Data](https://source.android.com/docs/core/ota/modular-system/timezone)
  * [UWB](https://source.android.com/docs/core/ota/modular-system/uwb)
  * [Wi-Fi](https://source.android.com/docs/core/ota/modular-system/wifi)
  
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
* [Android Debug Bridge (adb)](https://developer.android.com/studio/command-line/adb)
