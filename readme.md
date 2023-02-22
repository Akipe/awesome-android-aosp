# Awesome Android AOSP [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A collection of Android AOSP system (Android Open Source Project) and ROM development related resources.

This collection does not concern the development of application, there is a awesome list concerning this case at [JStumpp/awesome-android](https://github.com/JStumpp/awesome-android#readme).

Inspired by many awesome list like [sindresorhus/awesome](https://github.com/sindresorhus/awesome).

**This project is in work in progress !!! Some links may be not valid or not so useful.**

Contributions are welcome! I am looking for any kind of information that can help in the development of Android ROM. Don't hesitate to participate to make pull requests and or to exchange in the issues. You can read the [contribution guidelines](contributing.md) to know how to help me.

*English is not my primary language, there might be some language mistakes (feel free to correct them!).*

## Contents

- [Contents](#contents)
- [Learning](#learning)
  - [Where to start (complete guide)](#where-to-start-complete-guide)
  - [Specific point](#specific-point)
    - [Introduction](#introduction)
    - [General](#general)
    - [Building](#building)
      - [Automation](#automation)
    - [Device tree](#device-tree)
    - [Android Framework](#android-framework)
    - [Kernel](#kernel)
      - [Qualcomm](#qualcomm)
      - [Sony](#sony)
      - [Other vendors](#other-vendors)
    - [Blob and dump](#blob-and-dump)
    - [Feature](#feature)
      - [Telephony](#telephony)
      - [Encryption](#encryption)
    - [Security](#security)
      - [SELinux](#selinux)
    - [App integration](#app-integration)
    - [Optimization](#optimization)
    - [Android CTS/VTS \& test](#android-ctsvts--test)
    - [Treble GSI](#treble-gsi)
    - [Debugging](#debugging)
    - [Vendor specific](#vendor-specific)
      - [Qualcomm](#qualcomm-1)
      - [MediaTek](#mediatek)
      - [Raspberry Pi](#raspberry-pi)
      - [Samsung](#samsung)
      - [Google](#google)
      - [Other vendors](#other-vendors-1)
    - [Rom specific](#rom-specific)
      - [TWRP](#twrp)
      - [LineageOS](#lineageos)
      - [ArrowOS](#arrowos)
      - [OmniROM](#omnirom)
      - [Other](#other)
  - [Tools](#tools)
    - [Bash \& shell](#bash--shell)
    - [Git, Gerrit \& merging](#git-gerrit--merging)
    - [GNU Make](#gnu-make)
    - [Soong](#soong)
    - [Ninja build](#ninja-build)
  - [Formation](#formation)
  - [Documentation](#documentation)
    - [Qualcomm](#qualcomm-2)
    - [Sony](#sony-1)
  - [Official Android Documentation](#official-android-documentation)
  - [Video Channel](#video-channel)
- [Information](#information)
  - [Devices databases](#devices-databases)
- [Tools](#tools-1)
  - [General](#general-1)
  - [Generator](#generator)
  - [Extractor](#extractor)
  - [Kernel](#kernel-1)
  - [Blob \& vendor](#blob--vendor)
  - [Conversion](#conversion)
  - [Informations](#informations)
  - [Debugging](#debugging-1)
  - [Partitions, storage \& data](#partitions-storage--data)
  - [Vendor specific](#vendor-specific-1)
    - [Nexus](#nexus)
    - [LG](#lg)
    - [MediaTek](#mediatek-1)
    - [Samsung](#samsung-1)
    - [Sony](#sony-2)
  - [Users scripts](#users-scripts)
- [Books](#books)
- [Online groupes](#online-groupes)
  - [Telegram channel](#telegram-channel)
  - [Forum](#forum)
- [News](#news)
- [Vendors sources](#vendors-sources)
- [Blob](#blob)
- [ROMs](#roms)
- [Sources example](#sources-example)
  - [Device project](#device-project)
- [Related awesome](#related-awesome)
- [Todo](#todo)
- [Contributing](#contributing)

## Learning

### Where to start (complete guide)

* [Get started with Android Development](https://source.android.com/docs/setup) (official guide) - Official guide to beginning Android AOSP development.
* [Android Porting Guidebook](https://github.com/eyedeekay/android_porting_guidebook) (unfinished) - An (incomplete) guide book for porting Android ROM.
* [Android OS Internals / AOSP Mobile ROM Development](https://www.udemy.com/course/android-os-internals-aosp-mobile-development-2020-edition/) (udemy/not free) - Mobile Development.
* [Android OS Internals / AOSP Automotive ROM Development](https://www.udemy.com/course/android-os-internals-aosp-automotive-development/) (udemy/not free) - Android Automotive.
* [Android OS Internals / AOSP in Depth](https://www.udemy.com/course/android-os-internals-aosp-in-depth/) (udemy/not free) - Deep OS Analysis, Android Startup, AMS, WMS, System UI and more.
* [Android ROM Development From Source To End](https://forum.xda-developers.com/t/guide-complete-android-rom-development-from-source-to-end.2814763/) - The ultimate guide for ROM development starting from source to end.
* [How to build Android.... Where do I start?](https://www.youtube.com/watch?v=yNVe3mjCI1k) - Where newcomers should start.
* [Linux Device Driver Programming Using Beaglebone Black](https://www.udemy.com/course/linux-device-driver-programming-using-beaglebone-black/) (kernel/udemy/not free) - Foundation course on practical Linux device driver programming
* [AOSP - Android OS Internals Series](https://www.youtube.com/playlist?app=desktop&list=PLAlSOSt8vS8Ss3uEshNXQe3cbx9qtl8m4) (Youtube playlist) - Explore Android 12 from an AOSP point of view.

### Specific point

#### Introduction

* [Android Getting Started Guide](https://boundarydevices.com/android-getting-started-guide/)
* [Beginners Guide to Android ROM Development](https://forum.xda-developers.com/t/how-to-beginners-guide-to-android-rom-development.1272270/)
* [Introduction to AOSP](https://blog.realogs.in/getting-started-with-aosp/)
* [AOSP Introduction : AOSP Source Code Analysis Lecture 1](https://www.youtube.com/watch?v=MsUhQMz30J4)
* [Getting Started | AOSP Rom Development](https://adityatelange.in/blog/aosp/aosp-getting-started/)
* [Android rom building made easy - a beginers Guide part 1](https://www.youtube.com/watch?v=LPXK2Lv0nmk) [part 2](https://www.youtube.com/watch?v=Zr7esDS-QrI)
* [Android: What is...](https://www.youtube.com/playlist?list=PLRJ9-cX1yE1nbaEuyRi60ZWVP8_gGQb0J)

#### General

* [Android Tools (Github)](https://github.com/nathanchance/Android-Tools/) - Contains public guides and scripts tailored for custom Android Development.
* [AOSP Part 3: Developing Efficiently](https://blog.udinic.com/2014/07/24/aosp-part-3-developing-efficiently/)
* [AOSP: Advanced Development Tricks ](https://www.inovex.de/de/blog/aosp-advanced-development-tricks/)
* [How to build Custom ROMs and Kernels![10,P,O,N,M,L]](https://forum.xda-developers.com/t/guide-video-tutorial-how-to-build-custom-roms-and-kernels-10-p-o-n-m-l.3814251/)
* [Intermediate to Advanced Custom Rom and Kernel Building](https://forum.xda-developers.com/t/guide-video-tutorial-intermediate-to-advanced-custom-rom-and-kernel-building.3823927/)
* [Building AOSP, fastbooting on device](https://scribe.rip/@sohambhattacharya/building-aosp-fastbooting-on-device-eae05938cef8)
* [Some problems that can occur while rom compilation and their solutions(especially for lettuce)](https://github.com/hpnightowl/android_helpful/blob/master/errors.txt)
* [Embedded Android](https://www.opersys.com/downloads/cc-slides/embedded-android/embedded-android-141125.pdf)
* [AOSP Build References](https://www.youtube.com/playlist?list=PLeiDFxcsdhUq6Ch-9AAtiVU7Lw0tTSnKb)
* [Building My Product on Android Open Source Project](https://elinux.org/images/2/29/Customizing_AOSP_for_my_Device.pdf)
* [Android System Development](https://bootlin.com/pub/conferences/2012/captronic/android/android-captronic.pdf)
* [Android System Development (2019)](https://bootlin.com/doc/legacy/android/)
* [Android Hacks, Variants, Tricks and Resources](https://www.slideshare.net/opersys/android-variants-hacks-tricks-and-resources-presented-at-andevconii)
* [Android Cookbook: AOSP Custom ROM Building 201](https://tomwwolf.wordpress.com/android/android-cookbook-custom-aosp-rom-building-201/)
* [Android Cookbook: AOSP ROM Building 102](https://tomwwolf.wordpress.com/android/android-cookbook-aosp-rom-building-101/)
* [Complete Android ROM development and essential tutorials](https://forum.xda-developers.com/t/guide-complete-android-rom-development-and-essential-tutorials-by-nero-young.1661770/)
* [How To Port ROMS to Your Device [AOSP]](https://forum.xda-developers.com/t/guide-how-to-port-roms-to-your-device-aosp.2483143/)
* [Create your Own Custom ROM an easy way](https://forum.xda-developers.com/t/guide-how-to-create-your-own-custom-rom-an-easy-way.2195858/)
* [Create own ROM (for any Android device)](https://forum.xda-developers.com/t/guide-how-to-create-own-rom-for-any-android-device-for-n00b-easiest-methods.1801690/)
* [All you need to know to build Android from scratch!](https://forum.xda-developers.com/t/guide-2018-all-you-need-to-know-to-build-android-from-scratch.3862893/)
* [AOSP Build Guide](https://www.youtube.com/watch?app=desktop&v=-OePyL55rvs)
* [Building AOSP](https://github.com/nathanchance/android-tools/blob/main/guides/building_aosp.txt)
* [Android Build System Ultimate Guide](https://aabdelfattah.me/2013/04/08/android-build-system-ultimate-guide/)
* [A practical approach to the AOSP build system](https://blog.jayway.com/2012/10/24/a-practical-approach-to-the-aosp-build-system/)
* [AOSP Build System](https://budhdisharma.medium.com/aosp-build-system-767deeb535fa)
* [AOSP System Image](https://scribe.privacydev.net/android-news/aosp-system-image-b80e44ddf4)
* [Android Build System](https://elinux.org/Android_Build_System)
* [Building Custom Roms](https://www.youtube.com/playlist?list=PLRJ9-cX1yE1m8k9gztsQnnXDg1G4X1f6z)
* [VirtualBox](https://www.youtube.com/playlist?list=PLRJ9-cX1yE1ltYDIzCsSMCOpxXJSjrZd5)

#### Building

* [Learning about the Android Build Process](https://forum.xda-developers.com/t/guide-learning-about-the-android-build-process.2751407/)
* [AOSP Part 1: Get the code using the Manifest and Repo tool](https://blog.udinic.com/2014/05/24/aosp-part-1-get-the-code-using-the-manifest-and-repo/)
* [AOSP Part 2: Build variants](https://blog.udinic.com/2014/06/04/aosp-part-2-build-variants/)
* [Switching to a custom toolchain](https://forum.xda-developers.com/t/guide-linux-switching-to-a-custom-toolchain-arm-aarch64-sm-linaro-uber.2927662/)
* [Tutorial: Android Internals - Building a Custom ROM, Pt. 1 of 2 (Youtube)](https://www.youtube.com/watch?v=1_H4AlQaNa0)
* [Building The Android Open Source Project 1](https://littlelostandroid.wordpress.com/2015/11/28/building-the-android-open-source-project/) [(archive)](https://web.archive.org/web/20230221162551/https://littlelostandroid.wordpress.com/2015/11/28/building-the-android-open-source-project/), [2](https://littlelostandroid.wordpress.com/2015/11/30/building-the-android-open-source-project-part-2-start-off-small/), [3](https://littlelostandroid.wordpress.com/2015/12/07/building-the-android-open-source-project-part-3-flashing/), [4](https://littlelostandroid.wordpress.com/2015/12/09/building-the-android-open-source-project-part-4-git-repositories/)
* [Prebuilt apk in Build | AOSP Rom Development](https://adityatelange.in/blog/aosp/aosp-adding-prebuilt-apk/)
* [Setting Up Build Environment | AOSP Rom Development](https://adityatelange.in/blog/aosp/aosp-setting-up-build-environment/)
* [Anatomy of cross-compilation toolchains](https://bootlin.com/pub/conferences/2016/elce/petazzoni-toolchain-anatomy/petazzoni-toolchain-anatomy.pdf)
* [Building Android O with a Mac](https://scribe.rip/@christopherney/building-android-o-with-a-mac-da07e8bd94f9)
* [Building AOSP on macOS](https://dev.to/sriteja777/building-aosp-on-macos-2473)
* [How to Build Android ROMs on Ubuntu 16.04](https://www.digitalocean.com/community/tutorials/how-to-build-android-roms-on-ubuntu-16-04)
* [How to build ROM with Google Cloud](https://forum.xda-developers.com/t/guide-complete-how-to-build-rom-with-google-cloud.3360430/)
* [How to import the sources to Android Studio / IntelliJ](https://wiki.lineageos.org/how-to/import-to-android-studio)
* [AOSP: Source Code, Repo, Git](https://scribe.bus-hit.me/android-knowledge-store/aosp-source-code-repo-git-afd973a00356)
* [AOSP Emulator Guide](https://budhdisharma.medium.com/aosp-emulator-guide-762879714cd2)
* [Android AOSP Source Code Download and Build](https://budhdisharma.medium.com/android-aosp-source-code-download-and-build-92843c782df5)
* [Envsetup.sh configuration lunch for Android development (translate)](https://blog-csdn-net.translate.goog/llping2011/article/details/9339373?_x_tr_sl=zh-CN&_x_tr_tl=en&_x_tr_hl=en&_x_tr_pto=sc) [(original link)](https://blog.csdn.net/llping2011/article/details/9339373)
* [Detailed explanation of Android compilation system (1) - build/envsetup.sh (translate)](https://blog-csdn-net.translate.goog/mzm2438975656/article/details/52571743?_x_tr_sl=zh-CN&_x_tr_tl=en&_x_tr_hl=en&_x_tr_pto=sc) [(original link)](https://blog.csdn.net/mzm2438975656/article/details/52571743)
* [Notes on GCC 7.x+ for Android](https://gist.github.com/nathanchance/965028fc180b1cced015ac7530b2eaeb)

##### Automation

* [Use Github Action to compile Recovery](https://github.com/CaptainThrowback/Action-Recovery-Builder)

#### Device tree

* [Device Tree Reference](https://elinux.org/Device_Tree_Reference)
* [How to adapt your Device Tree to aosp and compile AOSP-11 from source Full Guide](https://www.youtube.com/watch?v=evw3QkAE1Jw&t=123s)
* [how to compile AOSP-10 from source and adapt device tree to pure aosp full guide](https://www.youtube.com/watch?v=KV0IkuRgZpA)
* [Android Framework - Device Tree in Android](https://www.youtube.com/watch?v=KA4TKFKyCMc&t=11s)
* [Creating a device tree from scratch](https://www.youtube.com/playlist?list=PLRJ9-cX1yE1nnhWBrZtuVz5YC2OPfQVVp)
* [How to make a device-tree for your phone](https://forum.xda-developers.com/t/guide-how-to-make-a-device-tree-for-your-phone.3698419/)
* [AOSP Folder Description](https://budhdisharma.medium.com/aosp-folder-description-ac1d55aa8bb2)
* [Android Device Tree Bringup](https://blog.realogs.in/android-device-tree-bringup/)
* [The method of independently compiling the device tree multi-file multi-dts dependency (translate)](https://blog-csdn-net.translate.goog/vesamount/article/details/83350300?_x_tr_sl=zh-CN&_x_tr_tl=en&_x_tr_hl=en&_x_tr_pto=sc) [(original link)](https://blog.csdn.net/vesamount/article/details/83350300)

#### Android Framework

* [Fundamental of Android Framework](https://budhdisharma.medium.com/fundamental-of-android-framework-761e6da812b8)
* [Android Binder Framework](https://scribe.froth.zone/android-news/android-binder-framework-8a28fb38699a)
* [AndroidManifest.xml](https://scribe.esmailelbob.xyz/android-news/androidmanifest-xml-4d5a3e821f91)
* [Android's HIDL: Treble in the HAL](https://fr.slideshare.net/opersys/androids-hidl-treble-in-the-hal)
* [Connecting a native HIDL (Project Treble) to a Custom System Service](https://scribe.nixnet.services/@gilzhaiek/connecting-a-native-hidl-project-treble-to-a-custom-system-service-2194c9ed7e91)
* [What is HIDL ?](https://news.ycombinator.com/item?id=17770251)
* [Discovering, reverse-engineering and using vendor HALs](https://forum.xda-developers.com/t/development-discovering-reverse-engineering-and-using-vendor-hals.3733410/)
* [System Service In AOSP](https://scribe.nixnet.services/android-news/system-service-in-aosp-750007d39555)
* [Android: Unix Domain Socket](https://scribe.nixnet.services/android-knowledge-store/android-unix-domain-socket-2cfec4a12ee7)
* [Get Android System write permission](https://scribe.nixnet.services/android-knowledge-store/get-android-system-write-permission-ba53742405f3)
* [RRO (Runtime Resource Overlay) in Android AOSP](https://budhdisharma.medium.com/rro-runtime-resource-overlay-in-android-aosp-e094be17f4bc)
* [Android AIDL Deep Dive](https://budhdisharma.medium.com/aidl-and-its-uses-in-android-e7a2520093e)
* [Android Boot Process](https://scribe.froth.zone/android-news/android-boot-process-8f7d94ff9889)
* [Android HIDL and Project Treble](https://devarea.com/android-hidl-and-project-treble/)
* [Project Treble. What Makes Android 8 different?](https://events19.linuxfoundation.org/wp-content/uploads/2017/11/Project-Treble.-What-Makes-Android-8-Different_-Fedor-Tcymbal-Mera-Software-Services.pdf)

#### Kernel

* [Android kernel from scratch using latest stable from kernel.org?](https://stackoverflow.com/questions/29121136/android-kernel-from-scratch-using-latest-stable-from-kernel-org)
* [The Linux Kernel : Rebasing and merging](https://docs.kernel.org/maintainer/rebasing-and-merging.html)
* [How to get an Android kernel up to date with linux-stable](https://forum.xda-developers.com/t/reference-how-to-get-an-android-kernel-up-to-date-with-linux-stable.3626913/)
* [Linux kernel merge notes](https://github.com/android-linux-stable/notes)
* [How to Rebase a Kernel](https://cyberknight777.dev/posts/2021/09/how-to-rebase-a-kernel/)
* [Linux Device Tree Pinctrl Tutorial](https://blog.modest-destiny.com/posts/linux-device-tree-pinctrl-tutorial/)
* [How to compile an Android kernel](https://forum.xda-developers.com/t/reference-how-to-compile-an-android-kernel.3627297/)
* [Android kernel development](https://www.youtube.com/playlist?list=PLsljP0DCGt1Fn8Ie8KeJxW4PZcImVwDE2)
* [start working on android kernel from scratch add kernel commits history qlcom devices part 1](https://www.youtube.com/watch?v=89sQiVznZxM)
* [How To Build Android Kernel With Features](https://forum.xda-developers.com/t/guide-noobs-familiar-how-to-build-android-kernel-with-features.3654336/)
* [How to Build Linux Kernel with Android](https://gist.github.com/EduApps-CDG/733e29c28dd53e91128d384c2e879397)
* [How to compile any Android stock kernel](https://www.youtube.com/watch?v=cueEGjQES9o)
* [Kernel For Newbies](https://baalajimaestro.me/posts/kernel-for-newbies/)
* [how to upstream the android kernel](https://www.youtube.com/watch?v=ZDqJvOj3-aE)
* [Linux debugging, profiling, tracing and performance analysis](https://bootlin.com/doc/training/debugging/)
* [Real-time Linux with PREEMPT_RT](https://bootlin.com/doc/training/preempt-rt/)
* [How to Upstream Android kernel?](https://steemit.com/utopian-io/@drohan/upstream-android-kernel)
* [Working with Android Kernel from Scratch](https://forum.xda-developers.com/t/guide-working-with-android-kernel-from-scratch.3909887/)
* [How to Update your Android Kernel to Latest Linux Stable](https://appuals.com/how-to-update-your-android-kernel-to-latest-linux-stable/)
* [Android Kernel Features](https://elinux.org/Android_Kernel_Features)
* [Android Kernel Download](https://elinux.org/Android_Kernel_Download)
* [Linux kernel and driver development course](https://bootlin.com/doc/training/linux-kernel/)
* [Android 8.0 learning --- modular kernel (translate)](https://bbs-zecoki-com.translate.goog/thread-18911-1-1.html?_x_tr_sch=http&_x_tr_sl=zh-CN&_x_tr_tl=en&_x_tr_hl=en&_x_tr_pto=sc) [(original link)](http://bbs.zecoki.com/thread-18911-1-1.html)
* [Linux kernel device tree and compilation (translate)](https://blog-csdn-net.translate.goog/u014650722/article/details/79076352?_x_tr_sl=zh-CN&_x_tr_tl=en&_x_tr_hl=en&_x_tr_pto=sc) [(original link)](https://blog.csdn.net/u014650722/article/details/79076352)
* [KernelNewbies: KernelBuild](https://kernelnewbies.org/KernelBuild)
* [Compiling an Android kernel with Clang](https://github.com/nathanchance/android-kernel-clang)

##### Qualcomm

* [Codeaurora how to git merge release tag onto kernel/msm-4.4?](https://stackoverflow.com/questions/47505063/codeaurora-how-to-git-merge-release-tag-onto-kernel-msm-4-4)
* [Merge Latest CAF Tags in Your Custom Kernel](https://www.youtube.com/watch?v=8WcVfTnToCI)
* [Merge latest CAF Tag in Kernel](https://forum.xda-developers.com/t/reference-merge-latest-caf-tag-in-kernel.3787564/)
* [How to merge a newer CAF tag in an android kernel](https://gist.github.com/JackLI9/741e47f26ff062a450a94476e3fa7580)
* [How to merge a newer CAF tag in an android kernel](https://gist.github.com/DD3Boh/6c51fd3c5f91b1042e956771483714de)
* [Porting Kernel Source to Snapdragon Device](https://forum.xda-developers.com/t/guide-porting-kernel-source-to-snapdragon-device.4042829/)

##### Sony

* [How to Build AOSP Pie Custom ROM for Xperia Devices](https://forum.xda-developers.com/t/guide-how-to-build-aosp-pie-custom-rom-for-xperia-devices.3921641/)

##### Other vendors

* [Compile a custom android kernel for Asus ROG Phone 2 using clang 10](https://www.youtube.com/watch?v=b8-eOfWviU0)
* [How to port a newer kernel to android-x86?](https://groups.google.com/g/android-x86/c/corNvvbjjSo)

#### Blob and dump

* [Extract vendor from stock firmware (Sony Xperia Z7 Premium)](https://forum.xda-developers.com/t/guide-extract-vendor-from-stock-firmware.4212587/)
* [Making Dump Files Out of Android Device Partitions](https://forum.xda-developers.com/t/guide-making-dump-files-out-of-android-device-partitions.2450045/)
* [Vendor Blob Extraction (v2)](https://baalajimaestro.me/posts/extract-vendor-2/) [old version](https://baalajimaestro.me/posts/extract-vendor/)
* [How To Extract Your Stock Firmware from Your Android Device](https://techsbyte.com/how-to-extract-your-stock-firmware-from-your-android-device/)
* [Find out which shared libs (.so) are missing](https://forum.xda-developers.com/t/tutorial-find-out-which-shared-libs-so-are-missing.2737126/)
* [ldd equivalent on android](https://stackoverflow.com/questions/15534104/ldd-equivalent-on-android)
* [What are blobs and HALs? ](https://www.reddit.com/r/Android/comments/52ovsh/eli5_what_are_blobs_and_hals/)
* [What are Blobs on Android?](https://www.quora.com/What-are-Blobs-on-Android)
* [Guide for full firmware extractors](https://github.com/Akianonymus/Firmware_Extraction)

#### Feature

##### Telephony

* [Enable VoLTE trhough modem mod (NV Items) ](https://www.reddit.com/r/GooglePixel/comments/7n8pes/enable_volte_trhough_modem_mod_nv_items/)
* [Android Telephony Basics](https://lineageos.org/engineering/Telephony/)

##### Encryption

* [Revisiting Android disk encryption](https://nelenkov.blogspot.com/2014/10/revisiting-android-disk-encryption.html?m=1)
* [Analysis of Android cryptfs](https://jsteward.moe/analysis-of-android-cryptfs.html)

#### Security

* [Building and flashing a secured AOSP build with verified boot and separate lockscreen password for the Nexus 5X](https://www.howtoforge.com/tutorial/building-and-flashing-a-secured-aosp-build-with-verified-boot-and-separate-lockscreen-password-for-the-nexus-5x/)
* [Signing Builds](https://wiki.lineageos.org/signing_builds)

##### SELinux

* [How to examine Android SELinux policy](https://www.whitewinterwolf.com/posts/2016/08/15/examine-android-selinux-policy/)
* [Working with SELinux on Android](https://lineageos.org/engineering/HowTo-SELinux/)
* [SELinux for Android 8.0](https://source.android.com/static/docs/security/features/selinux/images/SELinux_Treble.pdf)

#### App integration

* [How to Port OEM Apps / Vendor Apps to Your Current ROM](https://forum.xda-developers.com/t/guide-tips-how-to-port-oem-apps-vendor-apps-to-your-current-rom.2476050/)
* [System App In Android](https://scribe.nixnet.services/android-news/system-app-in-android-f003d418b4cc)
* [System App In Android](https://sc.vern.cc/android-news/system-app-in-android-f003d418b4cc)

#### Optimization

* [Speed up your app](https://blog.udinic.com/2015/09/15/speed-up-your-app/)
* [Timing Boot Time Reduction Technique](https://bootlin.com/pub/conferences/2019/elce/opdenacker-timing-boot-time-reduction-techniques/opdenacker-timing-boot-time-reduction-techniques.pdf)

#### Android CTS/VTS & test

* [How to build android cts? And how to add and run your test case?](https://stackoverflow.com/questions/2824015/how-to-build-android-cts-and-how-to-add-and-run-your-test-case)
* [Android VTS](https://budhdisharma.medium.com/android-vts-9e6ff95f075f)
* [Android CTS](https://budhdisharma.medium.com/android-cts-c790df99080)
* [Android System Stability Basics](https://budhdisharma.medium.com/android-system-stability-basics-e3bf63a928ca)

#### Treble GSI

* [How to build a Project Treble GSI ROM from source?](https://forum.xda-developers.com/t/guide-how-to-build-a-project-treble-gsi-rom-from-source-31-08.3801803/)

#### Debugging

* [Battery Status: Android](https://scribe.nixnet.services/android-knowledge-store/battery-status-android-fe3fd63f7ae5)
* [How to Find App UID](https://scribe.froth.zone/swlh/how-to-find-app-uid-9c9029063666)
* [Make Android Application Debugging Easier with STrace](https://www.xda-developers.com/make-android-application-debugging-easier-with-strace/)
* [Android Debug Bridge Fundamentals](https://scribe.privacydev.net/android-news/android-debug-bridge-fundamentals-2071363824cd)
* [Can I enable USB debugging using adb?](https://android.stackexchange.com/questions/120394/can-i-enable-usb-debugging-using-adb)
* [Enable ADB from recovery](https://gist.github.com/varhub/7b9555cdd1e5ad785ffde2300fcfd0bd)
* [7 Strace Examples to Debug the Execution of a Program in Linux](https://www.thegeekstuff.com/2011/11/strace-examples/)
* [Strace outil de dépannage Linux / debugging](https://math-linux.com/linux-2/tutoriels-linux/article/strace-outil-de-depannage-linux-debugging)
* [Strace et Ltrace : tracez les appels systèmes et librairies](https://wiki.deimos.fr/Strace_et_Ltrace_:_tracez_les_appels_syst%C3%A8mes_et_librairies.html)
* [Android Log Analysis](https://budhdisharma.medium.com/android-log-analysis-176f9b9dafaf)
* [How to Acquire Logs](https://telegra.ph/HOW-TO-TAKE-LOGS-06-11)
* [Proper AOSP bug reporting](https://github.com/nathanchance/android-tools/blob/main/guides/proper_bug_reporting.txt)
* [Troubleshooting examples](https://www.youtube.com/playlist?list=PLRJ9-cX1yE1lQwh_NHLAzcZsW5lMerXby)
* [Errors - Common or Not](https://www.youtube.com/playlist?list=PLRJ9-cX1yE1kokIK8VfyE09RoCNqefoY3)

#### Vendor specific

##### Qualcomm

* [Qualcomm’s Chain of Trust](https://lineageos.org/engineering/Qualcomm-Firmware/)
* [CAF's Android for MSM](https://adityatelange.in/blog/aosp/caf-android-for-msm/)
* [Software Build and Installation Guide, Linux Android (Qualcomm)](https://developer.qualcomm.com/download/db410c/linux-android-software-build-and-installation-guide.pdf)
* [Adreno and Vulkan drivers for Snapdragon 820/1](https://forum.xda-developers.com/t/mod-adreno-nougat-vulkan-thdr-adreno-and-vulkan-drivers-for-snapdragon-820-1.3555141/)
* [Hardware rendering of SurfaceFlinger on Qualcomm Adreno GPUs](https://mjanja.ch/2012/12/hardware-rendering-of-surfaceflinger-on-qualcomm-adreno-gpus/)
* [How does someone find which CAF tag of the camera HAL is closest to stock one? / CameraWrapper ](https://www.reddit.com/r/LineageOS/comments/8pv0lz/devq_how_does_someone_find_which_caf_tag_of_the/)
* [Qualcomm Code Aurora caf-manifest tags](https://gitlab.com/simonsmh/caf-manifest/-/tags)
* [How do I compile Android 4.4.2 for Qualcomm MSM systems?](https://stackoverflow.com/questions/29763302/how-do-i-compile-android-4-4-2-for-qualcomm-msm-systems)
* [The Compilation Process of Qualcomm Projects written by Beginners](https://programmer.help/blogs/the-compilation-process-of-qualcomm-projects-written-by-beginners.html)

##### MediaTek

* [How To Port TWRP For MediaTek Android Devices](https://techsbyte.com/how-to-port-twrp-for-mediatek-android-devices/)
* [How To Port TWRP To A/B Partitioned Devices (MediaTek)](https://techsbyte.com/how-to-port-twrp-to-a-b-partitioned-devices-mediatek/)

##### Raspberry Pi

* [Android On Raspberry Pi](https://budhdisharma.medium.com/android-on-raspberry-pi-7795e4914dc0)

##### Samsung

* [How To Build CyanogenMod For Samsung Galaxy Note 4 International ("trltexx")](https://fat-tire.github.io/build-los-trltexx.html)
* [How To Build CyanogenMod For Samsung Galaxy Note 4 T-Mobile ("trltetmo")](https://fat-tire.github.io/build-los-trltetmo.html)

##### Google

* [Android Cookbook: Nexus Device Hacking 101](https://tomwwolf.wordpress.com/android/android-cookbook-hacking101-nexus/)

##### Other vendors

* [Building and Deploying Android AOSP 6.01 for the Wandboard](https://android.serverbox.ch/?p=1738)
* [Device Tree overlays and U-boot extension board management](https://bootlin.com/pub/conferences/2021/lee/maincent-devicetree-overlay-and-uboot-extension-board-management/maincent-devicetree-overlay-and-uboot-extension-board-management.pdf)
* [How To Build LineageOS For Barnes & Noble Nook Color ("encore")](https://fat-tire.github.io/build-los-encore.html)
* [Cara Port Custom ROM AOSP | Android 10](https://www.youtube.com/watch?v=kwnQVY1Wn6s)
* [Embedded Linux boot time reduction course](https://bootlin.com/doc/training/boot-time/)
* [Understanding the Linux graphics stack](https://bootlin.com/doc/training/graphics/)
* [Buildroot development course](https://bootlin.com/doc/training/buildroot/)
* [Yocto Project and OpenEmbedded development course](https://bootlin.com/doc/training/yocto/)
* [Embedded Linux system development course](https://bootlin.com/doc/training/embedded-linux/)

#### Rom specific

##### TWRP

* [How to create twrp device tree from scratch](https://www.youtube.com/playlist?list=PLsljP0DCGt1EBN4X-NR3-oS6f1NYxLLQA)
* [How to DIY Port TWRP for Android](https://appuals.com/how-to-diy-port-twrp-for-android/)
* [How to compile TWRP from source step by step](https://forum.xda-developers.com/t/guide-noob-friendly-how-to-compile-twrp-from-source-step-by-step.3404024/)
* [Compile LineageOS TWRP: Setting up minimal LineageOS TWRP](https://www.youtube.com/watch?v=7xdIxiiHLlc&t=9s)
* [TWRP Flags for BoardConfig.mk](https://forum.xda-developers.com/t/twrp-flags-for-boardconfig-mk.3333970/)
* [How to compile TWRP touch recovery](https://forum.xda-developers.com/t/dev-how-to-compile-twrp-touch-recovery.1943625/)
* [TWRP standard device files for Qualcomm SoCs decryption](https://github.com/TeamWin/android_device_qcom_twrp-common)
* [How generate TWRP with TwrpBuilder](https://github.com/TwrpBuilder/twrpbuilder_tree_generator/wiki)
* [TWRP tree from scratch](https://www.youtube.com/playlist?list=PLRJ9-cX1yE1lnwTD8QP_e5Ohj8Ys-0oO7)
* [Android.mk : a set of tag](https://github.com/TeamWin/android_bootable_recovery/blob/android-12.1/Android.mk)
* [Compile TWRP](https://www.youtube.com/playlist?list=PLRJ9-cX1yE1kzxSkdZSG_h_f-GDNmSmAl)
* [How to compile TWRP touch recovery](https://forum.xda-developers.com/t/dev-how-to-compile-twrp-touch-recovery.1943625/#post-32965365)

##### LineageOS

* [How To Port CyanogenMod/LineageOS Android To Your Own Device](https://fat-tire.github.io/porting-intro.html)
* [How to adapt a LineageOS device tree for AOSP](https://theautomatedparts.com/apblog/?p=12)
* [How-to Build LineageOS​](https://forum.xda-developers.com/t/guide-build-lineageos-how-to-use-github.3551484/)

##### ArrowOS

* [ArrowOS Compilation guide](https://blog.arrowos.net/android/arrowos/guides/compilation-guide/)

##### OmniROM

* [OmniROM - Porting Omni to your device](https://github.com/omnirom/Docs/blob/master/Porting_Omni_To_Your_Device.md)

##### Other

* [Building Alternative Recoveries](https://www.youtube.com/playlist?list=PLRJ9-cX1yE1nQ2HgCoeJS3j_bpTIXh_Fe)

### Tools

#### Bash & shell

*There is also an awesome list with more resources : [awesome-shell](https://github.com/alebcay/awesome-shell#readme)*.

* [Bash Commands and Tips for Beginners to Experts](https://dev.to/awwsmm/101-bash-commands-and-tips-for-beginners-to-experts-30je)
* [Linux](https://www.youtube.com/playlist?list=PLRJ9-cX1yE1m0G44PfLl8eK_gt_dXd8Ay)

#### Git, Gerrit & merging

*There is also awesome lists with more resources : [awesome-git](https://github.com/dictcp/awesome-git#readme), [Git and Git Flow Cheat Sheet](https://github.com/arslanbilal/git-cheat-sheet#readme) and [git-tips](https://github.com/git-tips/tips#readme).*

* [How AOSP Security Patches are merged into Android Custom ROMs?](https://adityatelange.in/blog/aosp/merge-security-patches-aosp/)
* [How-To Cherry-Pick Features for your ROM (both Github and Gerrit)](https://forum.xda-developers.com/t/guide-how-to-cherry-pick-features-for-your-rom-both-github-and-gerrit.2763236/)
* [Oh Shit, Git!?!](https://ohshitgit.com/)
* [Git Immersion](https://gitimmersion.com/)
* [Become a git guru](https://www.atlassian.com/git/tutorials)
* [Git For Newbies](https://baalajimaestro.me/posts/git-for-newbies/)
* [Using Gerrit code review](https://forum.xda-developers.com/t/guide-using-gerrit-code-review.3720802/)
* [Working with git bisect](https://nathanchance.dev/posts/working-with-git-bisect/) - To allows you to find out specifically which change or commit caused a particular issue.
* [git-cherry-pick documentation](https://git-scm.com/docs/git-cherry-pick)
* [GitHub and GitLab](https://www.youtube.com/playlist?list=PLRJ9-cX1yE1mm6avXq9ZxehWsb4gYuRb9)

#### GNU Make

*There is also an awesome list with more resources : [awesome-make](https://github.com/adelarsq/awesome-make#readme)*

* [GNU Autotools: a tutorial](https://bootlin.com/pub/conferences/2016/elc/petazzoni-autotools-tutorial/petazzoni-autotools-tutorial.pdf)

#### Soong

* [Soong readme](https://android.googlesource.com/platform/build/soong/+/refs/heads/master/README.md) - Official documentation from Google.

#### Ninja build

* [The Ninja build system](https://ninja-build.org/manual.html)

### Formation

* [Android Internals (not free)](http://technologeeks.com/course.jl?course=AIRE)
* [bootlin training (not free)](https://bootlin.com/training/)
* [Opersys training (not free)](https://www.opersys.com/training/)

### Documentation

* [Android Open Source Project](https://source.android.com/) - Official documentation for Android AOSP
* [Android Code Search](https://cs.android.com/android)
* [LineageOS wiki](https://wiki.lineageos.org/)
* [XDA Forum : Android Development and Hacking](https://forum.xda-developers.com/c/android-development-and-hacking.564/)
* [XDA Forum : XDA-University](https://forum.xda-developers.com/f/xda-university.2060/)
* [XDA Forum : Android Software Development](https://forum.xda-developers.com/f/android-software-development.524/)
* [XDA : All guides at one place](https://forum.xda-developers.com/t/guides-all-guides-at-one-place.2073370/)
* [Archlinux : How build Android](https://wiki.archlinux.org/title/Android#Building) - Steps for building Android on Archlinux (and maybe other distributions).
* [Projekt ScriBt wiki](https://scribt.github.io/index.html) ([XDA thread](https://forum.xda-developers.com/t/guide-tool-linux-projekt-scribt-v2-2-1-build-a-rom-newbie-friendly.3503018/) & [sources](https://github.com/ScriBt/ScriBt.github.io))
* [bootlin documentation](https://bootlin.com/docs/)
* [Halium](https://docs.halium.org/en/latest/index.html)

#### Qualcomm

* [Qualcomm Android Source Realease](https://wiki.codelinaro.org/en/clo/la/release)

#### Sony

* [Guides and Resources for Sony Xperia™ & AOSP](https://sx.ix5.org/info/)
* [Open Devices : Guides & Resources (Sony devices)](https://opendevices.ix5.org/resources/)

### Official Android Documentation

*All this pages are from source.android.com. You can with this list view its content more easily.*

* [Android Compatibility Definition Document (CDD)](https://source.android.com/docs/compatibility/cdd)
* [AIDL for HALs](https://source.android.com/docs/core/architecture/aidl/aidl-hals)
* [Building Kernels](https://source.android.com/docs/setup/build/building-kernels)
* [Implementing dm-verity](https://source.android.com/docs/security/features/verifiedboot/dm-verity)
* [Linux-stable Merges](https://source.android.com/docs/core/architecture/kernel/linux-stable-merges)
* [Verified Boot](https://source.android.com/docs/security/features/verifiedboot)
* [Android.mk](https://developer.android.com/ndk/guides/android_mk)
* [Vendor Native Development Kit (VNDK) overview](https://source.android.com/docs/core/architecture/vndk)
* [Downloading the Source](https://source.android.com/docs/setup/download/downloading)
* [Optimizing Boot Times](https://source.android.com/docs/core/perf/boot-times)
* [Capture a system trace on the command line](https://developer.android.com/topic/performance/tracing/command-line)
* [Capture a system trace on a device](https://developer.android.com/topic/performance/tracing/on-device)
* [The Android Profiler](https://developer.android.com/studio/profile/android-profiler)
* [Environment variables](https://developer.android.com/studio/command-line/variables)
* [Debugging Native Android Platform Code](https://source.android.com/docs/core/tests/debug)
* [Using Strace](https://source.android.com/docs/core/tests/debug/strace)
* [Understanding Systrace](https://source.android.com/docs/core/tests/debug/systrace)
* [Evaluating Performance](https://source.android.com/docs/core/tests/debug/eval_perf)
* [Diagnosing Native Crashes](https://source.android.com/docs/core/tests/debug/native-crash)
* [Inspect CPU activity with CPU Profiler](https://developer.android.com/studio/profile/cpu-profiler)
* [Using Debuggers](https://source.android.com/docs/core/tests/debug/gdb)
* [Encryption](https://source.android.com/docs/security/features/encryption)
* [File-Based Encryption](https://source.android.com/docs/security/features/encryption/file-based)
* [Full-Disk Encryption](https://source.android.com/docs/security/features/encryption/full-disk)
* [Android HAL Reference (legacy)](https://source.android.com/reference/hal)
* [Customizing SELinux](https://source.android.com/docs/security/features/selinux/customize)
* [Writing SELinux Policy](https://source.android.com/docs/security/features/selinux/device-policy)
* [Downloading the Source](https://source.android.com/docs/setup/build/downloading)
* [Android Common Kernels](https://source.android.com/docs/core/architecture/kernel/android-common)
* [Analyze with Profile GPU Rendering](https://developer.android.com/topic/performance/rendering/profile-gpu)
* [Inspect GPU rendering speed and overdraw](https://developer.android.com/topic/performance/rendering/inspect-gpu-rendering)
* [Soong Build System](https://source.android.com/docs/setup/build)

### Video Channel

* [AlaskaLinuxUser AKLU](https://www.youtube.com/c/AlaskaLinuxUserAKLU)
* [Android & Linux Development (@remainder30000)](https://www.youtube.com/@remainder30000)
* [Dimple S](https://www.youtube.com/@dimples_android_geek)
* [Haikal Luthfianino Balukia](https://www.youtube.com/@haikalluthfianinobalukia2423/videos)
* [OSP »» Android OS »» ROM »» Android Development](https://www.youtube.com/@aosp_android_tollcafe/videos)

## Information

### Devices databases

* [Device Info HW Database](https://deviceinfohw.ru/devices/)
* [J's Android Device Database](http://newandroidbook.com/ddb/)
* [Kimovil](https://www.kimovil.com/en/compare-smartphones)
* [PHONEDB](https://phonedb.net/)
* [PHONEDB - Processor](https://phonedb.net/index.php?m=processor&s=headlines)

## Tools

*Tools for helping development of Android Rom*

### General

* [Android MADkitchen (careful!)](https://androidforums.com/threads/introducing-android-mad-kitchen.1294651/) [(virustotal)](https://www.virustotal.com/gui/file-analysis/ODAwNWVlNjc4MTc0OTI3ODhiMDM2ZmVmODJmN2FhYmY6MTY3NzA2MzAxNw==) - Fork of the ASSAYYED KITCHEN for Windows (be careful).
* [aosp-merger](https://github.com/LineageOS/scripts/tree/master/aosp-merger)
* [ASSAYYED KITCHEN](https://forum.xda-developers.com/t/best-android-roms-apks-file_systems-editor-assayyed_kitchen.3410545/) [(direct link)](https://mega.nz/#!fAIkBZKQ!aS-9yNL9GKgVzgJd9C5DWJtjD_fNM6bHTiz-1KnsydA) - A set of tool for cooking Android on Windows.
* [mAid](https://maid.binbash.rocks/index.html) ([sources](https://code.binbash.rocks:8443/mAid)) - An easy and ready-to-use Linux distribution for developing Android.
* [Projekt Scribt](https://github.com/ScriBt/ScriBt) ([XDA thread](https://forum.xda-developers.com/t/guide-tool-linux-projekt-scribt-v2-2-1-build-a-rom-newbie-friendly.3503018/)) - ROM envsetup, sync and build script for learning developers.
* [Building from source Any ROM](https://forum.xda-developers.com/t/guide-building-from-source-any-rom.2200926/)

### Generator

* [TwrpBuilder](https://github.com/TwrpBuilder/twrpbuilder_tree_generator) - Generate twrp device tree just using recovery.img and build.prop.
* [twrpdtgen](https://github.com/twrpdtgen/twrpdtgen) [(doc)](https://github.com/twrpdtgen/twrpdtgen/wiki) - Create a TWRP device tree only from an Android recovery stock image ROM.

### Extractor

* [abootimg](https://github.com/ggrandou/abootimg) - Manipulate Android boot images.
* [Android Deodexer](https://github.com/Akianonymus/Android_deodexer) - For deodex odexed android firmwares.
* [Android Image Kitchen](https://forum.xda-developers.com/t/tool-android-image-kitchen-unpack-repack-kernel-ramdisk-win-android-linux-mac.2073775/) - Unpack/repack kernel and recovery images, and edit the ramdisk.
* [bootimgtool](https://github.com/vianney/bootimgtool) - Unpack/pack Android boot.img.
* [dextra](http://newandroidbook.com/tools/dextra.html) - An alternative to dexdump for displaying information about .dex files.
* [Firmware Extraction](https://github.com/Akianonymus/Firmware_Extraction) - Regroupment of available firmware extractors.
* [imjtool](http://newandroidbook.com/tools/imjtool.html) - A quick extractor of Android images.
* [ROME](https://code.binbash.rocks:8443/mAid/android_rome) - [ROM] [E]xtractor, a simple GUI for extracting custom and stock ROMs containing.

### Kernel

* [best-caf-kernel.py](https://github.com/LineageOS/scripts/blob/master/best-caf-kernel/best-caf-kernel.py) - Finding the best CAF tag for a vendor kernel.
* [Kernel Rebaser Script](https://github.com/Sushrut1101/android-kernel-rebaser) - Rebase an OEM kernel to Android Common Kernel base.
* [Toolchain build scripts](https://github.com/ClangBuiltLinux/tc-build) - A set of script for building kernel with LLCM, clang.
* [bldgcc](https://github.com/nathanchance/android-tools/blob/main/scripts/bldgcc) - Builds GCC and binutils for exclusively building kernels.

### Blob & vendor

* [Android-Blob-Utility](https://forum.xda-developers.com/t/blob-utility-for-aosp-based-roms.2794413/) [(sources)](https://github.com/JackpotClavin/Android-Blob-Utility) - Easily find which proprietary blobs is needed.
* [aosp-missing-blobs](https://github.com/joshuous/AospMissingBlobs) - Identify required blobs that are missing from AOSP ROM builds with dependencies.
* [DumprX](https://github.com/DumprX/DumprX) - Firmware extractor based on dumpyara.
* [dumpyara](https://github.com/AndroidDumps/dumpyara) - Dumping vendor and Android content of a device.
* [dumpyara (Python)](https://github.com/sebaubuntu-python/dumpyara) - Like dumpyara but code in Python.
* [ldcheck](https://github.com/that1/ldcheck) - Check dependencies and missing for a blob file.

### Conversion

* [hidl2aidl](https://source.android.com/docs/core/architecture/aidl/aidl-hals#converting-to-aidl) - For Converting an existing HAL from HIDL to AIDL.

### Informations

* [Device Info HW (playstore](https://play.google.com/store/apps/details?id=ru.andr7e.deviceinfohw&pli=1)/[paid version)](https://play.google.com/store/apps/details?id=ru.andr7e.deviceinfohw.pro) - A hardware and software information app for Android devices.
* [TrustDevice-Android](https://github.com/trustdecision/trustdevice-android) [(izzyondroid)](https://apt.izzysoft.de/fdroid/index/apk/com.trustdevice.android)- Get informations about security and other.
* [Codec Info](https://github.com/Parseus/codecinfo) ([playstore](https://play.google.com/store/apps/details?id=com.parseus.codecinfo)/[izzyondroid](https://apt.izzysoft.de/fdroid/index/apk/com.parseus.codecinfo)) - Detailed listing of multimedia codecs on your Android device.
* [TrebleInfo](https://gitlab.com/TrebleInfo/TrebleInfo) ([playstore](https://play.google.com/store/apps/details?id=tk.hack5.treblecheck)/[f-droid](https://f-droid.org/packages/tk.hack5.treblecheck/)/[izzyondroid](https://apt.izzysoft.de/fdroid/index/apk/tk.hack5.treblecheck)) -  Check the Treble GSI requirements and determine the correct GSI type for your device.
* [Kaltura Device Info](https://bitbucket.org/oF2pks/kaltura-device-info-android/src/master/) ([playstore](https://play.google.com/store/apps/details?id=com.kaltura.kalturadeviceinfo)/[f-droid](https://f-droid.org/fr/packages/com.oF2pks.kalturadeviceinfos/))
* [Devstat](https://ianfield.com/DevStat/) ([source](https://github.com/IanField90/DevStat)/[izzyondroid](https://apt.izzysoft.de/fdroid/index/apk/uk.co.ianfield.devstat)) - Help you debug a number device issues like identifying various features you request in your AndroidManifest.xml.
* [SysInfo](https://github.com/kl3jvi/sysinfo_app) ([izzyondroid](https://apt.izzysoft.de/fdroid/index/apk/com.kl3jvi.sysinfo)) - Simple and powerful application that gives you complete information about your mobile device.

### Debugging

* [Alogview](https://github.com/flimberger/alogview) - A coloured log viewer for ADB logcat.
* [bdsm](http://newandroidbook.com/tools/bdsm.html) - Debbuging Android's Binder.
* [Binder Explorer](https://github.com/opersys/binder-explorer-web) - Represente Binder relations.
* [bindump](http://newandroidbook.com/tools/bindump.html) - Map which PIDs communicate over Binder.
* [dmtracedump](https://developer.android.com/studio/command-line/dmtracedump) - Generates graphical call-stack diagrams from trace log files.
* [dumpsys](https://developer.android.com/studio/command-line/dumpsys) - Get information about Android system services.
* [file-explorer web](https://github.com/opersys/file-explorer-web) & [file-explorer app](https://github.com/opersys/file-explorer-app) - Exploring Android files with your computer.
* [jtrace](http://newandroidbook.com/tools/jtrace.html) - An augmented, Linux/Android aware strace with plugin architecture.
* [Logcat](https://developer.android.com/studio/command-line/logcat) - A command-line tool that dumps a log of system messages.
* [memento](http://newandroidbook.com/tools/memento.html) - A simple but highly useful memory inspection tool.
* [PID Cat](https://github.com/JakeWharton/pidcat) - Only display log messages coming from a specific application.
* [Process Explorer](http://newandroidbook.com/tools/procexp.html) - Show current process like the "top" application.
* [Process Explorer web](https://github.com/opersys/process-explorer-web) & [Process Explorer app](https://github.com/opersys/process-explorer-app) - Show current process graphicaly.
* [Simpleperf](https://android.googlesource.com/platform/system/extras/+/master/simpleperf/doc/README.md) - A native CPU profiling tool for Android (include in Android Studio).
* [Simple-ADB](https://forum.xda-developers.com/t/win-mac-linx-simple-adb.3417155/) ([sources](https://github.com/mhashim6/Simple-ADB)) - ADB/Fastboot with a Graphical User Interface.
* [strace](https://forum.xda-developers.com/t/utility-strace-4-8-ultimate-debugging-utility-now-ported-to-android.2516002/) - A debugging utility to monitor a program system calls or signals it receives. 

### Partitions, storage & data

* [iozone](https://fossies.org/linux/iozone/src/current/Android_Readme.md) - IO benchmark tool for Android.
* [JPT](http://newandroidbook.com/tools/jpt.html) - A "quick & dirty" GPT partition editor.

### Vendor specific

#### Nexus

* [anestisb/android-prepare-vendor (Github)](https://github.com/anestisb/android-prepare-vendor) - A collection of utilities for Nexus devices.

#### LG

* [LGLAF](https://github.com/Lekensteyn/lglaf) or [here](https://gitlab.com/runningnak3d/lglaf) or [here](https://github.com/steadfasterX/lglaf) - Utility for communication with LG devices in Download Mode.
* [SALT](https://forum.xda-developers.com/t/tool-locked-unlocked-salt-the-lg-up-revolution-begins.3717864/) [sources](https://github.com/steadfasterX/SALT) - Utility able to communicate with your device while in download mode.

#### MediaTek

* [SP Flash Tool](https://spflashtool.com/) - An application which mainly helps you to flash Stock ROM, Custom recovery and fixing in some extreme cases.

#### Samsung

* [Heimdall](https://github.com/Benjamin-Dobell/Heimdall) and [website](https://glassechidna.com.au/heimdall/) - A cross-platform open-source tool suite used to flash firmware onto Samsung devices.

#### Sony

* [Flashtool](https://github.com/Androxyde/Flashtool) and [website](https://flashtool.net/download.html) - An Xperia device flashing tool.
* [UnSIN ~ SIN v3/v4/v5 Unpacker](https://forum.xda-developers.com/t/tool-unsin-sin-v3-v4-v5-unpacker-v1-13.3128106/) - An unpacker for Sony devices images.

### Users scripts

*You can use them as inspiration to create your own or find solutions*

* [akhilnarang/scripts (Github)](https://github.com/akhilnarang/scripts) - Some script useful for ROM development.
* [Build scripts](https://github.com/JarlPenguin/releases)
* [LineageOS scripts](https://github.com/LineageOS/scripts)
* [ShivamKumarJha/android_tools (Github)](https://github.com/ShivamKumarJha/android_tools) - Collection of scripts to help with Android ROM stuff.
* [android_helpful](https://github.com/hpnightowl/android_helpful)
* [Android Build Environment Scripts](https://github.com/CyberJalagam/android_rom_building_scripts)

## Books

* Android Firmware Customization *by Arvind Choudhary* ([amazon](https://www.amazon.com/Android-Firmware-Customization-Arvind-Choudhary/dp/9385020293))
* Android Internals series *by Jonathan Levin* ([website](http://newandroidbook.com/)/[summary](http://newandroidbook.com/TOC.html))
  * Android Internals::Power User's View - *volume 1* ([amazon](https://www.amazon.com/gp/product/0991055586/ref=as_li_tl?ie=UTF8&camp=1789&creative=9325&creativeASIN=0991055586&linkCode=as2&tag=newosxbookcom-20&linkId=dee63bd17b404113dd16f234b5b904eb)/[free 2015 edition](http://newandroidbook.com/AIvI-M-RL1.pdf)/[wikileaks](https://wikileaks.org/ciav7p1/cms/files/AIvI-M-RL1.pdf))
  * Android Internals::Developer's View - *volume 2* ([amazon](https://www.amazon.com/dp/0991055543?&_encoding=UTF8&tag=newosxbookcom-20&linkCode=ur2&linkId=bb5d8363ae5c9a2be1dceb1745a229b8&camp=1789&creative=9325))
  * Android Internals::Security - *volume 3* (being written)
  * Android Internals::The Implementer's View - *volume 4* (being written)
* Android Security Internals: An In-Depth Guide to Android's Security Architecture *by  Nikolay Elenkov* ([amazon](https://www.amazon.com/Android-Security-Internals-Depth-Architecture/dp/1593275811))
* Embedded Android: Porting, Extending, and Customizing *by Karim Yaghmour* ([oreilly](https://www.oreilly.com/library/view/embedded-android/9781449327958/)/[amazon](https://www.amazon.com/_/dp/1449308295))
* Embedded Programming with Android: Bringing Up an Android System from Scratch *by Roger Ye* ([oreilly](https://www.oreilly.com/library/view/embedded-programming-with/9780134030920/)/[amazon](https://www.amazon.com/Embedded-Programming-Android-Bringing-Scratch/dp/0134030001))

## Online groupes

### Telegram channel

*Telegram is often used for asking help and share informations.*

* [AndroidRom_developers](https://t.me/bestandroiddevs)
* [Android Building Help](https://t.me/AndroidBuildersHelp) - Group for help compiling Android AOSP ROMs.
* [Android ROM Development](https://t.me/androidromdev) - Discussion about Android ROM development and testing.
* [AOSP Tracker](https://t.me/aosptracker) - Tracking Android source tags and branches.
* [Bringup/FW chat](https://t.me/androidbringup) - Chat for device bringup/debugging and firmware.
* [Codeaurora Releases](https://t.me/s/CAFReleases) - Tracking CAF new releases.
* [Linux Kernel Brickers](https://t.me/LinuxKernelNewbies)
* [TWRP Building Support Group](https://t.me/build_twrp) - Support group for building TWRP touch recovery.
* [RomDevelopment](https://t.me/alaskalinuxuser_romdevelopment)
* [XDA-Hub](https://t.me/xdadevelopershub) - Hub for finding specific XDA Telegram group.

### Forum

* [androidforums](https://androidforums.com/)
* [android-porting (Google Groups)](https://groups.google.com/g/android-porting)
* [phonandroid (french)](https://www.phonandroid.com/forum/forums/developpement.13/) - French forum for ROM development.
* [XDA Forum](https://forum.xda-developers.com/)

## News

* [Android Champ blog](https://medium.com/android-knowledge-store)
* [LineageOS engineering blog](https://lineageos.org/engineering/)
* [XDA Developers news](https://www.xda-developers.com/)
  * [Development](https://www.xda-developers.com/tag/development/)
  * [LineageOS](https://www.xda-developers.com/tag/lineageos/)
  * [TWRP](https://www.xda-developers.com/tag/twrp/)
  * [XDA MODS](https://www.xda-developers.com/category/developments/)

## Vendors sources

*Where you can download open source software of your device, like the Linux kernel sources.*

* [Alcatel](https://www.alcatelmobile.com/)
  * [Open source](https://sourceforge.net/projects/alcatel/files/)
* [Archos](https://www.archos.com/)
  * todo
* [Asus](https://www.asus.com/mobile/phones/all-series/)
  * Open source : search for each devices at [support](https://www.asus.com/support/) > Driver & Utility > Source Code (example : [Zenfone 9](https://www.asus.com/mobile/phones/zenfone/zenfone-9/helpdesk_download/?model2Name=Zenfone-9))
* [BlackBerry](https://www.blackberry.com/us/en/support/devices)
  * [Github](https://github.com/blackberry)
* [BQ](https://educacion.bq.com/)
  * [Open source](http://opensource.bq.com/)
  * [Github](https://github.com/bq)
* [Fairphone](https://www.fairphone.com/)
  * [Open source](https://code.fairphone.com/)
* [Google](https://developers.google.com/android/images)
* [Honor](https://consumer.huawei.com/en/phones/)
  * [Open source (1)](https://consumer.huawei.com/en/opensource/)
  * [Open source (2)](https://www.hihonor.com/global/opensource/)
* [HTC](https://www.htc.com/us/)
  * [Open source](https://www.htcdev.com/devcenter/downloads)
* [Huawei](https://consumer.huawei.com/en/phones/)
  * [Open source](https://consumer.huawei.com/en/opensource/)
* [Infinix](https://www.infinixmobility.com)
  * [Github](https://github.com/OpenSource-Infinix)
* LeBest (LeEco/LeTV)
  * [Open source](http://opensource.le.com/)
* [Lenvovo](https://www.lenovo.com/us/en/tablets)
  * Open source : search device on [support](https://support.lenovo.com/us/en) (example : [IdeaTab S2109](https://support.lenovo.com/us/en/downloads/ds00306-open-source-code-kernel-ideatab-s2109-tablet-ideatab-s2109a-tablet))
* [LG](https://www.lg.com/us/cell-phones)
  * [Open source](https://opensource.lge.com/index)
  * [Inquiry sources](https://opensource.lge.com/inquiry)
* [MediaTek](https://www.mediatek.com/) - No open source repositories available directly.
  * [Github](https://github.com/MediaTek-Labs)
* [Meizu](https://www.meizu.com/)
  * [Open source](https://github.com/meizuosc)
* [Nokia / HMD Global](https://www.nokia.com/)
  * No sources
* [Motorola](https://www.motorola.com/us/)
  * [Open source](https://www.motorola.com/us/developer)
  * [Github repositories](https://github.com/MotorolaMobilityLLC)
* [Nothing Phone](https://nothing.tech/)
  * [Github](https://github.com/NothingOSS)
* Nubia
  * todo
* [OnePlus](https://www.oneplus.com/)
  * [Github](https://github.com/OnePlusOSS)
* [Oppo](https://www.oppo.com/my/)
  * [Open source notice](https://www.oppo.com/my/store/contents/legal/open-source-software-notice/)
  * [Github](https://github.com/oppo-source)
* [Qualcomm](https://www.qualcomm.com/home)
  * [Code Aurora](https://www.codeaurora.org/)
  * [Repositories sources](https://source.codeaurora.org/)
  * [Proprietary binaries sources (account needed)](https://chipcode.qti.qualcomm.com/)
* [Realme](https://www.realme.com/global/)
  * [Github](https://github.com/realme-kernel-opensource)
* [Samsung](https://www.samsung.com/us/mobile/)
  * [Open source](https://opensource.samsung.com/main)
  * [Inquiry sources](https://opensource.samsung.com/requestInquiry)
* [Sony](https://electronics.sony.com/c/mobile)
  * [Open source](https://developer.sony.com/develop/open-source/)
  * [Build instructions](https://developer.sony.com/develop/open-devices/guides/aosp-build-instructions/)
* [Vivo](https://www.vivo.com/)
  * [Open source](https://opensource.vivo.com/Project)
* [Wiko](https://wikomobile.com/)
  * [Open source](https://www.wikogeek.com/)
  * [Inquiry sources](https://de.wikomobile.com/promo.php?d=2919)
* [Xiaomi](www.xiaomi.cn)
  * [Github repositories](https://github.com/MiCode?type=source)
* [ZTE](https://ztedevices.com/)
  * [Open source](https://opensource.ztedevices.com/)

## Blob

***Binary Large OBject** are often private libaries that you have to get from vendor systems.*

* [Android Dumps](https://dumps.tadiphone.dev/dumps) - Get complete files dumps of specific devices.
* The Muppets ([Gitlab](https://gitlab.com/the-muppets)/[Github](https://github.com/TheMuppets?type=source)) - A regroupment of different vendor files.

## ROMs

*Biggest ROMs projects. You can check her Gerrit instance for study how to port ROMs.*

* [Android AOSP](https://source.android.com/)
  * [Android Review Gerrit](https://android-review.googlesource.com/q/status:open+-is:wip)
* [LineageOS]()
  * [Github](https://github.com/LineageOS)
  * [Gerrit](https://review.lineageos.org/q/status:open+-is:wip)
* [TWRP](https://twrp.me/)
  * [Github](https://github.com/TeamWin)
  * [Gerrit](https://gerrit.twrp.me/q/status:open+-is:wip)
  * [Community chat](https://twrp.zulipchat.com/join/zumqdy6spjszarpubcag4y33/)

## Sources example

*Source code for some project related to Android AOSP.*

* [Android AOSP mirror Github](https://github.com/aosp-mirror/platform_development)
* [Android dummy trees](https://github.com/AndroidBlobs/) - Device & kernel repositories as reference for many devices.
* [android-linux-stable (archive)](https://github.com/android-linux-stable)
* [Minimal manifest for TWRP](https://github.com/minimal-manifest-twrp)
* [Linux kernel](https://git.kernel.org/pub/scm/linux/kernel/git/stable/linux.git/)

### Device project

*Some device project source which you can inspect to study how to port devices.*

* [Project Elixir • [Devices]](https://github.com/ProjectElixir-Devices) - Offer a minimal UI enhancement & close to Stock Android ROM with great performance, security and stability.
* [Raspberry Vanilla](https://github.com/raspberry-vanilla) - AOSP for Raspberry Pi 4.

## Related awesome

* [android-security-awesome](https://github.com/ashishb/android-security-awesome#readme) - A collection of android security related resources.
* [awesome-android](https://github.com/JStumpp/awesome-android#readme) - For Android application development.
* [awesome-android-ui](https://github.com/wasabeef/awesome-android-ui#readme) - List of Android UI/UX Libraries
* [awesome-c](https://github.com/inputsh/awesome-c) - A curated list of C good stuff.
* [awesome-git](https://github.com/dictcp/awesome-git#readme) - Ressources for learning how to use Git.
* [awesome-linux](https://github.com/inputsh/awesome-linux#readme) - Collections of Linux & GNU\Linux resources.
* [awesome-make](https://github.com/adelarsq/awesome-make#readme) - Collections of Make resources.
* [awesome-shell](https://github.com/alebcay/awesome-shell#readme) - A curated list of awesome command-line frameworks, toolkits, guides and gizmos.
* [Git and Git Flow Cheat Sheet](https://github.com/arslanbilal/git-cheat-sheet#readme) - Collection of git commands with descriptions.
* [git-tips](https://github.com/git-tips/tips#readme) - Collection of git-tips.

## Todo
* <https://github.com/davisRoman/aosp-research>

## Contributing

Contributions welcome! Read the [contribution guidelines](contributing.md) first.
