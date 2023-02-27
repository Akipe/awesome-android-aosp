# Awesome Android AOSP [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A collection of Android AOSP system (Android Open Source Project) and ROM development related resources.

This collection does not concern the development of application, there is a awesome list concerning this case at [JStumpp/awesome-android](https://github.com/JStumpp/awesome-android#readme).

Inspired by many awesome list like [sindresorhus/awesome](https://github.com/sindresorhus/awesome).

**This project is in work in progress !!! Some links may be not valid or not so useful.**

Contributions are welcome! I am looking for any kind of information that can help in the development of Android ROM. Don't hesitate to participate to make pull requests and or to exchange in the issues. You can read the [contribution guidelines](contributing.md) to know how to help me.

*English is not my primary language, there might be some language mistakes (feel free to correct them!).*

There is also a list of all pages for the official AOSP Android documentation here : [summary_official_documentation.md](summary_official_documentation.md)

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
    - [Storage](#storage)
    - [Trebble](#trebble)
    - [Android Framework](#android-framework)
    - [Kernel](#kernel)
      - [Reverse engineering](#reverse-engineering)
      - [Qualcomm](#qualcomm)
      - [MediaTek](#mediatek)
      - [Sony](#sony)
      - [Other vendors](#other-vendors)
    - [Blob and dump](#blob-and-dump)
      - [Reverse Engineering](#reverse-engineering-1)
    - [Feature](#feature)
      - [Telephony](#telephony)
      - [Encryption](#encryption)
      - [Bluetooth](#bluetooth)
      - [Graphics](#graphics)
      - [Audio](#audio)
      - [Time](#time)
      - [Customization](#customization)
    - [Security](#security)
      - [SELinux](#selinux)
      - [Audio](#audio-1)
    - [App integration](#app-integration)
    - [Optimization](#optimization)
    - [Android CTS/VTS \& test](#android-ctsvts--test)
    - [Treble GSI](#treble-gsi)
    - [Debugging](#debugging)
    - [Magisk](#magisk)
    - [Vendor specific](#vendor-specific)
      - [Qualcomm](#qualcomm-1)
      - [MediaTek](#mediatek-1)
      - [Raspberry Pi](#raspberry-pi)
      - [Samsung](#samsung)
      - [Google](#google)
      - [Motorola](#motorola)
      - [Other vendors](#other-vendors-1)
    - [Rom specific](#rom-specific)
      - [TWRP](#twrp)
      - [LineageOS](#lineageos)
      - [ArrowOS](#arrowos)
      - [OmniROM](#omnirom)
      - [Other](#other)
  - [Tools](#tools)
    - [C language](#c-language)
    - [Bash \& shell](#bash--shell)
    - [Git, Gerrit \& merging](#git-gerrit--merging)
    - [GNU Make](#gnu-make)
    - [Soong](#soong)
    - [Other](#other-1)
    - [Ninja build](#ninja-build)
    - [Reverse Engeenering](#reverse-engeenering)
      - [IDA](#ida)
      - [ghidra](#ghidra)
  - [Formation](#formation)
  - [Documentation](#documentation)
    - [Qualcomm](#qualcomm-2)
    - [Sony](#sony-1)
  - [Video Channel](#video-channel)
- [Information](#information)
  - [Devices databases](#devices-databases)
- [Tools](#tools-1)
  - [General](#general-1)
  - [Generator](#generator)
  - [Extractor/Repack/Patcher](#extractorrepackpatcher)
  - [Kernel](#kernel-1)
  - [Blob \& vendor](#blob--vendor)
  - [Conversion](#conversion)
  - [Informations](#informations)
  - [Debugging](#debugging-1)
  - [Partitions, storage \& data](#partitions-storage--data)
  - [Magisk](#magisk-1)
  - [Drivers](#drivers)
  - [Other](#other-2)
  - [Vendor specific](#vendor-specific-1)
    - [Nexus](#nexus)
    - [LG](#lg)
    - [MediaTek](#mediatek-2)
    - [Qualcomm](#qualcomm-3)
    - [Samsung](#samsung-1)
    - [Sony](#sony-2)
    - [Huawei (and Honor)](#huawei-and-honor)
    - [Xiaomi](#xiaomi)
    - [Motorola](#motorola-1)
  - [Users scripts](#users-scripts)
- [Books](#books)
- [Online groupes](#online-groupes)
  - [Telegram channel](#telegram-channel)
  - [Forum](#forum)
- [News](#news)
- [Vendors sources](#vendors-sources)
- [Blob](#blob)
- [GAPPS](#gapps)
- [ROMs](#roms)
- [Sources example](#sources-example)
  - [Device project](#device-project)
- [Related awesome](#related-awesome)
- [Todo](#todo)
- [Contributing](#contributing)

## Learning

### Where to start (complete guide)

It is recommended to start with the official documentation available at <https://source.android.com/> & <https://developer.android.com/>.

There is a summary available in this project for navigate more easily and find more quickly what you search : [summary_official_documentation.md](./summary_official_documentation.md)

* [Android Porting Guidebook](https://github.com/eyedeekay/android_porting_guidebook) (2015/unfinished) - An (incomplete) guide book for porting Android ROM.
* [Android OS Internals / AOSP Mobile ROM Development](https://www.udemy.com/course/android-os-internals-aosp-mobile-development-2020-edition/) (udemy/not free) - Mobile Development.
* [Android OS Internals / AOSP Automotive ROM Development](https://www.udemy.com/course/android-os-internals-aosp-automotive-development/) (udemy/not free) - Android Automotive.
* [Android OS Internals / AOSP in Depth](https://www.udemy.com/course/android-os-internals-aosp-in-depth/) (udemy/not free) - Deep OS Analysis, Android Startup, AMS, WMS, System UI and more.
* [Android ROM Development From Source To End](https://forum.xda-developers.com/t/guide-complete-android-rom-development-from-source-to-end.2814763/) (2022) - The ultimate guide for ROM development starting from source to end.
* [How to build Android.... Where do I start?](https://www.youtube.com/watch?v=yNVe3mjCI1k) (2019/video) - Where newcomers should start.
* [Linux Device Driver Programming Using Beaglebone Black](https://www.udemy.com/course/linux-device-driver-programming-using-beaglebone-black/) (kernel/udemy/not free) - Foundation course on practical Linux device driver programming
* [AOSP - Android OS Internals Series](https://www.youtube.com/playlist?app=desktop&list=PLAlSOSt8vS8Ss3uEshNXQe3cbx9qtl8m4) (recent/video playlist) - Explore Android 12 from an AOSP point of view.

### Specific point

*You may find also information and solution to the official documentation at [summary_official_documentation.md](summary_official_documentation.md)*

#### Introduction

* [Android Getting Started Guide](https://boundarydevices.com/android-getting-started-guide/) (2015)
* [Beginners Guide to Android ROM Development](https://forum.xda-developers.com/t/how-to-beginners-guide-to-android-rom-development.1272270/) (2013)
* [Introduction to AOSP](https://blog.realogs.in/getting-started-with-aosp/) (2022)
* [AOSP Introduction : AOSP Source Code Analysis Lecture 1](https://www.youtube.com/watch?v=MsUhQMz30J4) (2022/video)
* [Getting Started | AOSP Rom Development](https://adityatelange.in/blog/aosp/aosp-getting-started/) (2020)
* [Android rom building made easy - a beginers Guide part 1](https://www.youtube.com/watch?v=LPXK2Lv0nmk) [part 2](https://www.youtube.com/watch?v=Zr7esDS-QrI) (2017/video)
* [Android: What is...](https://www.youtube.com/playlist?list=PLRJ9-cX1yE1nbaEuyRi60ZWVP8_gGQb0J) (video playlist)
* [Android device configuration for AOSP](https://stackoverflow.com/questions/11352709/android-device-configuration-for-aosp/11353248#11353248)
* [How To Setup And Use Fastboot](https://forum.xda-developers.com/t/guide-how-to-setup-and-use-fastboot.2277112/)

#### General

* [Android Tools (Github)](https://github.com/nathanchance/Android-Tools/) (2021) - Contains public guides and scripts tailored for custom Android Development.
* [AOSP Part 3: Developing Efficiently](https://blog.udinic.com/2014/07/24/aosp-part-3-developing-efficiently/) (2014)
* [AOSP: Advanced Development Tricks ](https://www.inovex.de/de/blog/aosp-advanced-development-tricks/) (2021)
* [How to build Custom ROMs and Kernels![10,P,O,N,M,L]](https://forum.xda-developers.com/t/guide-video-tutorial-how-to-build-custom-roms-and-kernels-10-p-o-n-m-l.3814251/) (2019)
* [Intermediate to Advanced Custom Rom and Kernel Building](https://forum.xda-developers.com/t/guide-video-tutorial-intermediate-to-advanced-custom-rom-and-kernel-building.3823927/) (2019)
* [Building AOSP, fastbooting on device](https://scribe.rip/@sohambhattacharya/building-aosp-fastbooting-on-device-eae05938cef8) (2018)
* [Some problems that can occur while rom compilation and their solutions(especially for lettuce)](https://github.com/hpnightowl/android_helpful/blob/master/errors.txt) (2019)
* [Embedded Android](https://www.opersys.com/downloads/cc-slides/embedded-android/embedded-android-141125.pdf) (old/pdf)
* [AOSP Build References](https://www.youtube.com/playlist?list=PLeiDFxcsdhUq6Ch-9AAtiVU7Lw0tTSnKb) (2022/video playlist)
* [Building My Product on Android Open Source Project](https://elinux.org/images/2/29/Customizing_AOSP_for_my_Device.pdf) (2015/pdf)
* [Android System Development](https://bootlin.com/pub/conferences/2012/captronic/android/android-captronic.pdf) (old/pdf)
* [Android System Development](https://bootlin.com/doc/legacy/android/) (2019/pdf)
* [Android Hacks, Variants, Tricks and Resources](https://www.slideshare.net/opersys/android-variants-hacks-tricks-and-resources-presented-at-andevconii) (old/pdf)
* [Android Cookbook: AOSP Custom ROM Building 201](https://tomwwolf.wordpress.com/android/android-cookbook-custom-aosp-rom-building-201/) (2013)
* [Android Cookbook: AOSP ROM Building 102](https://tomwwolf.wordpress.com/android/android-cookbook-aosp-rom-building-101/) (2013)
* [Complete Android ROM development and essential tutorials](https://forum.xda-developers.com/t/guide-complete-android-rom-development-and-essential-tutorials-by-nero-young.1661770/) (2013)
* [How To Port ROMS to Your Device [AOSP]](https://forum.xda-developers.com/t/guide-how-to-port-roms-to-your-device-aosp.2483143/) (2013)
* [Create your Own Custom ROM an easy way](https://forum.xda-developers.com/t/guide-how-to-create-your-own-custom-rom-an-easy-way.2195858/) (2016)
* [Create own ROM (for any Android device)](https://forum.xda-developers.com/t/guide-how-to-create-own-rom-for-any-android-device-for-n00b-easiest-methods.1801690/) (2013)
* [All you need to know to build Android from scratch!](https://forum.xda-developers.com/t/guide-2018-all-you-need-to-know-to-build-android-from-scratch.3862893/) (2018)
* [AOSP Build Guide](https://www.youtube.com/watch?app=desktop&v=-OePyL55rvs) (2018/video)
* [Building AOSP](https://github.com/nathanchance/android-tools/blob/main/guides/building_aosp.txt) (2021)
* [Android Build System Ultimate Guide](https://aabdelfattah.me/2013/04/08/android-build-system-ultimate-guide/) (2013)
* [A practical approach to the AOSP build system](https://blog.jayway.com/2012/10/24/a-practical-approach-to-the-aosp-build-system/) (2012)
* [AOSP Build System](https://budhdisharma.medium.com/aosp-build-system-767deeb535fa) (2019)
* [AOSP System Image](https://scribe.privacydev.net/android-news/aosp-system-image-b80e44ddf4) (2019)
* [Android internals](https://www.youtube.com/playlist?list=PLEq1q16moI5uvGNEdu0eODGiSJAk3VXfy) (old/video playlists)
* [android internals](https://www.youtube.com/playlist?list=PL07D15CEBAC16A98B) (2012/video playlist)
* [How to port roms in Windows​](https://forum.xda-developers.com/t/guide-how-to-port-roms-snapdragon-windows-linux.3801391/) (2019)
* [Android Internals](https://vimeo.com/18017921) (2010/video)
* [Porting to custom hardware](https://elinux.org/images/7/71/03-android-inside.pdf) (2010/pdf)
* [Porting Android to New Hardware](https://www.pudn.com/detail/2374139) (2011/pdf)
* [AN11690 - NXP NCI Android Porting Guidelines](https://www.nxp.com/docs/en/application-note/AN11690.pdf) (2020/pdf)
* [Industrialize your ROM cooking: good practices](https://elinux.org/images/d/d3/ROM_cooking_and_good_practices--vagnet.pdf) (old/pdf)
* [Make your first custom Rom- easiest way](https://forum.xda-developers.com/t/guide-make-your-first-custom-rom-easiest-way.1821695/)
* [How to port roms to your Device](https://forum.xda-developers.com/t/guide-how-to-port-roms-to-your-device.1957219/)
* [How To Port Different Roms to Your Device - For CM, AOSP & AOKP](https://forum.xda-developers.com/t/guide-how-to-port-different-roms-to-your-device-for-cm-aosp-aokp.2545618/)
* [[Development] [Source] [Noob] [Friendly]](https://forum.xda-developers.com/t/rom-development-source-noob-friendly.3848394/)
* [Porting Roms between two similar devices](https://forum.xda-developers.com/t/guide-porting-roms-between-two-similar-devices.2675345/)
* [How To Port a Custom Rom](https://forum.xda-developers.com/t/guide-how-to-port-a-custom-rom-noob-friendly.3157127/)
* [How to port ROMS](https://forum.xda-developers.com/t/guide-how-to-port-roms.1941239/)
* [Install a Linux OS alongside almost any Android device](https://forum.xda-developers.com/t/guide-root-install-a-linux-os-alongside-almost-any-android-device-december-2017.3726844/)
* [Complete Shell Script Flashable Zip Replacement + Signing](https://forum.xda-developers.com/t/dev-template-complete-shell-script-flashable-zip-replacement-signing-script.2934449/)
* [Android system init process startup and init.rc full analysis](https://dev.to/larsonzhong/android-system-init-process-startup-and-init-rc-full-analysis-22hi)
* [Android Gpio use cases by controlling LED](https://dev.to/larsonzhong/android-gpio-use-cases-by-controlling-led-298d)
* [What is inside the init.rc and what is it used for.](https://community.nxp.com/t5/i-MX-Processors-Knowledge-Base/What-is-inside-the-init-rc-and-what-is-it-used-for/ta-p/1106360)
* [The init process and init.rc (archive)](https://web.archive.org/web/20160309042832/http://www.androidenea.com/2009/08/init-process-and-initrc.html)
* [Collection of 'em all - build.prop; init.d; etc.](https://forum.xda-developers.com/t/tweaks-scripts-collection-of-em-all-build-prop-init-d-etc.1227269/)
* [How to modify app preferences with adb](https://forum.xda-developers.com/t/guide-how-to-modify-app-preferences-with-adb-and-set-configuration-for-the-simple-calendar-widget.4447255/)
* [How to Compile AOSPA from Source : + Support and Maintenance](https://forum.xda-developers.com/t/guide-aospa-v3-how-to-compile-aospa-from-source-support-and-maintenance.1863547/)
* [How to build an unsupported rom using sources from other roms](https://forum.xda-developers.com/t/guide-how-to-build-an-unsupported-rom-using-sources-from-other-roms.3844972/)
* [A Simple Way to (kind of) Dual Boot an Android](https://forum.xda-developers.com/t/a-simple-way-to-kind-of-dual-boot-an-android.4176415/)
* [Keep apps running in background via crond](https://forum.xda-developers.com/t/keep-apps-running-in-background-via-crond.4303475/)
* [Hands-On Exercises for Embedded Android](https://www.opersys.com/downloads/cc-slides/embedded-android/exercises-201103.pdf) [2020]
* [Android 3rd Party Recordings opersys](https://www.youtube.com/watch?v=oea7CWdZrsQ&list=PL7OsLr7k6qp39gjnjYE-QysSI4JUwfX2q) [2015] [playlist]

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
* [Android Build System](https://elinux.org/Android_Build_System)
* [Building Custom Roms](https://www.youtube.com/playlist?list=PLRJ9-cX1yE1m8k9gztsQnnXDg1G4X1f6z)
* [VirtualBox](https://www.youtube.com/playlist?list=PLRJ9-cX1yE1ltYDIzCsSMCOpxXJSjrZd5)
* [How to build Android from source (2020 edition)](https://forum.xda-developers.com/t/guide-how-to-build-android-from-source-2020-edition.4171993/)
* [how to make a flashable package (update.zip)](https://forum.xda-developers.com/t/guide-how-to-make-a-flashable-package-update-zip.732957/)
* [Compiling ROMs from Compressed Sources](https://forum.xda-developers.com/t/guide-compiling-roms-from-compressed-sources.3426480/)
* [Set up ADB and Fastboot on a Mac easily](https://forum.xda-developers.com/t/guide-set-up-adb-and-fastboot-on-a-mac-easily-with-screenshots.1917237/)
* [How to build Android 11 with low ram](https://forum.xda-developers.com/t/guide-how-to-build-android-11-with-low-ram.4298483/)
* [Noobs guide to decompile/recompile android application](https://forum.xda-developers.com/t/how-to-noobs-guide-to-decompile-recompile-android-application.1860115/)
* [Create your own UPDATE.ZIP](https://forum.xda-developers.com/t/tutorial-create-your-own-update-zip.1610121/)
* [Set Up A Build Environment On Android](https://forum.xda-developers.com/t/tools-zips-scripts-osm0sis-odds-and-ends-multiple-devices-platforms.2239421/page-11#post-51230135)
* [Cygwin-Linux Cross-Compiler](https://forum.xda-developers.com/t/tools-zips-scripts-osm0sis-odds-and-ends-multiple-devices-platforms.2239421/page-12#post-51726566)
* [nano Android static build instructions](https://forum.xda-developers.com/t/tools-zips-scripts-osm0sis-odds-and-ends-multiple-devices-platforms.2239421/page-34#post-66486572)
* [Build Custom ROM in windows 10 (WSL2)](https://forum.xda-developers.com/t/noob-guide-blind-copy-guide-android-11-build-custom-rom-in-windows-10-wsl2.4392711/)
* [How to build Android on Windows](https://forum.xda-developers.com/t/guide-how-to-build-android-on-windows.3750175/)
* [How To Compile Rom From Source full guide step by step](https://forum.xda-developers.com/t/how-to-compile-rom-from-source-full-guide-step-by-step-by-jai-sharma.3499666/)
* [Compile make_ext4fs, simg2img and img2simg using mingw](https://forum.xda-developers.com/t/guide-windows-compile-make_ext4fs-simg2img-and-img2simg-using-mingw-by-jamflux.4055375/)
* [Compile busybox on Linux](https://forum.xda-developers.com/t/guide-bin-compile-busybox-on-linux.2857650/)
* [Compile busybox (Magisk) for Android with ndk](https://blog.mx17.net/2021/11/22/compile-busybox-magisk-for-android-with-ndk/)
* [Cross compile fstrim for Android on Ubuntu 18.10](https://blog.mx17.net/2019/01/10/cross-compile-fstrim-for-android-on-ubuntu-18-10/)
* [How to compile rsync for Android in Ubuntu](https://blog.mx17.net/2014/06/10/compile-rsync-android-ubuntu/)

##### Automation

* [Use Github Action to compile Recovery](https://github.com/CaptainThrowback/Action-Recovery-Builder)

#### Device tree

* [Device Tree Reference](https://elinux.org/Device_Tree_Reference)
* [How to adapt your Device Tree to aosp and compile AOSP-11 from source Full Guide](https://www.youtube.com/watch?v=evw3QkAE1Jw)
* [how to compile AOSP-10 from source and adapt device tree to pure aosp full guide](https://www.youtube.com/watch?v=KV0IkuRgZpA)
* [Android Framework - Device Tree in Android](https://www.youtube.com/watch?v=KA4TKFKyCMc)
* [Creating a device tree from scratch](https://www.youtube.com/playlist?list=PLRJ9-cX1yE1nnhWBrZtuVz5YC2OPfQVVp)
* [How to make a device-tree for your phone](https://forum.xda-developers.com/t/guide-how-to-make-a-device-tree-for-your-phone.3698419/)
* [AOSP Folder Description](https://budhdisharma.medium.com/aosp-folder-description-ac1d55aa8bb2)
* [Android Device Tree Bringup](https://blog.realogs.in/android-device-tree-bringup/)
* [The method of independently compiling the device tree multi-file multi-dts dependency (translate)](https://blog-csdn-net.translate.goog/vesamount/article/details/83350300?_x_tr_sl=zh-CN&_x_tr_tl=en&_x_tr_hl=en&_x_tr_pto=sc) [(original link)](https://blog.csdn.net/vesamount/article/details/83350300)
* [How to create Device tree for Android Rom building](https://forum.xda-developers.com/t/how-to-create-device-tree-for-android-rom-building.3498355/)

#### Storage

* [Universal guide for making your partitions inside super read-writable again.](https://forum.xda-developers.com/t/guide-universal-guide-for-making-your-partitions-inside-super-read-writable-again.4483933/)
* [SuperPatcherGSI Automated Script for patching the super partition](https://forum.xda-developers.com/t/superpatchergsi-automated-script-for-patching-the-super-partition-super-img.4528589/)
* [Allow SDCard write access & switch SDCard Path](https://forum.xda-developers.com/t/guide-app-6-x-x-7-x-x-allow-sdcard-write-access-switch-sdcard-path.3593021/)

#### Trebble

* [How to make GSIs overlay file for your phone](https://forum.xda-developers.com/t/guide-how-to-make-gsis-overlay-file-for-your-phone.3878974/)
* [GSI Porting Tools for Android](https://forum.xda-developers.com/t/gsi-porting-tools-for-android-auto-script-a-to-a-b-wip.4089193/)
* [Guide For Flashing GSIs for all Android devices (2021)](https://forum.xda-developers.com/t/discoveryandroid-guide-for-flashing-gsis-for-all-android-devices-2021.4348851/)
* [How to port A system image to AB (system-as-root)](https://forum.xda-developers.com/t/guide-how-to-port-a-system-image-to-ab-system-as-root.3829885/)
* [How to build a Project Treble GSI ROM from source?](https://forum.xda-developers.com/t/guide-how-to-build-a-project-treble-gsi-rom-from-source-31-08.3801803/)

#### Android Framework

* [Fundamental of Android Framework](https://budhdisharma.medium.com/fundamental-of-android-framework-761e6da812b8)
* [Android Binder Framework](https://scribe.froth.zone/android-news/android-binder-framework-8a28fb38699a)
* [AndroidManifest.xml](https://scribe.esmailelbob.xyz/android-news/androidmanifest-xml-4d5a3e821f91)
* [Android's HIDL: Treble in the HAL](https://fr.slideshare.net/opersys/androids-hidl-treble-in-the-hal)
* [Connecting a native HIDL (Project Treble) to a Custom System Service](https://scribe.nixnet.services/@gilzhaiek/connecting-a-native-hidl-project-treble-to-a-custom-system-service-2194c9ed7e91)
* [What is HIDL ?](https://news.ycombinator.com/item?id=17770251)
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
* [Captronic Porting Linux on an ARM board](https://bootlin.com/pub/conferences/2015/captronic/captronic-porting-linux-on-arm.pdf) (pdf)
* [Android Kernel Configs](https://android.googlesource.com/kernel/configs/+/refs/heads/master/README.md)
* [Build Your Own Android Kernel](https://forum.xda-developers.com/t/guide-build-your-own-android-kernel-easiest-and-fastest-way-using-the-ndk.2152819/)
* [Kernel Post Compilation Guide; how to turn kernel into img](https://forum.xda-developers.com/t/tutorial-kernel-post-compilation-guide-how-to-turn-kernel-into-img.3604083/)
* [Kernel Building - Essentials | Build a Kernel Easily](https://forum.xda-developers.com/t/tool-dev-1-0-official-kernel-building-essentials-build-a-kernel-easily.3814023/)
* [Compile your own android kernel from source](https://forum.xda-developers.com/t/ultimate-guide-noob-friendly-compile-your-own-android-kernel-from-source.2871276/)
* [Compile an Android kernel module outside the kernel source tree.](https://hex.ro/wp/blog/compile-an-android-kernel-module-outside-the-kernel-source-tree/)
* [Compile our own Android Kernel in 5 Simple Steps](https://www.geeksforgeeks.org/compile-our-own-android-kernel-in-5-simple-steps/)
* [Building the android kernel (Mac OS)](https://forum.xda-developers.com/t/tutorial-reference-building-the-android-kernel-mac-os.3856676/)
* [Automated Linux Kernel CVE Patcher](https://forum.xda-developers.com/t/tool-automated-linux-kernel-cve-patcher.4249547/)
* [How Do Linux Kernel Drivers Work?](https://www.youtube.com/watch?v=juGNPLdjLH4)

##### Reverse engineering

* [Reverse engineer kernel](https://forum.xda-developers.com/t/how-to-reverse-engineer-kernel.3137384/)

##### Qualcomm

* [Codeaurora how to git merge release tag onto kernel/msm-4.4?](https://stackoverflow.com/questions/47505063/codeaurora-how-to-git-merge-release-tag-onto-kernel-msm-4-4)
* [Merge Latest CAF Tags in Your Custom Kernel](https://www.youtube.com/watch?v=8WcVfTnToCI)
* [Merge latest CAF Tag in Kernel](https://forum.xda-developers.com/t/reference-merge-latest-caf-tag-in-kernel.3787564/)
* [How to merge a newer CAF tag in an android kernel](https://gist.github.com/JackLI9/741e47f26ff062a450a94476e3fa7580)
* [How to merge a newer CAF tag in an android kernel](https://gist.github.com/DD3Boh/6c51fd3c5f91b1042e956771483714de)
* [Porting Kernel Source to Snapdragon Device](https://forum.xda-developers.com/t/guide-porting-kernel-source-to-snapdragon-device.4042829/)
* [brcmfmac wifi driver & qcwcn libs for MSM8974-based devices like Sony Shinano](https://forum.xda-developers.com/t/dev-wip-brcmfmac-wifi-driver-qcwcn-libs-for-msm8974-based-devices-like-sony-shinano.4199257/)

##### MediaTek

* [A Noob Guide On Building Your Own Custom Kernel (ARM & ARM64 & MTK)](https://forum.xda-developers.com/t/guide-a-noob-guide-on-building-your-own-custom-kernel-arm-arm64-mtk.3581057/)
* [A Noob Guide On Building Your Own Custom Kernel on WIN10](https://forum.xda-developers.com/t/guide-a-noob-guide-on-building-your-own-custom-kernel-on-win10-arm-arm64-mtk.3775494/)

##### Sony

* [How to Build AOSP Pie Custom ROM for Xperia Devices](https://forum.xda-developers.com/t/guide-how-to-build-aosp-pie-custom-rom-for-xperia-devices.3921641/)

##### Other vendors

* [Compile a custom android kernel for Asus ROG Phone 2 using clang 10](https://www.youtube.com/watch?v=b8-eOfWviU0)
* [How to port a newer kernel to android-x86?](https://groups.google.com/g/android-x86/c/corNvvbjjSo)
* [Custom Kernel on 96boards Hikey LeMaker](https://suchakra.wordpress.com/2016/04/15/custom-kernel-on-96boards-hikey/)

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
* [How to Decompile APKs with ODEX files](https://forum.xda-developers.com/t/guide-how-to-decompile-apks-with-odex-files-noob-friendly.3325340/)
* [How to easily edit/modify .apk files](https://forum.xda-developers.com/t/guide-how-to-easily-edit-modify-apk-files-simple-noob-friendly.2058850/)
* [Working with proprietary blobs](https://wiki.lineageos.org/proprietary_blobs.html)
* [Android definition-tool (vndk-lib-extra-list)](https://android.googlesource.com/platform/development/+/master/vndk/tools/definition-tool/datasets)
* [Android Backup and Restore Tools](https://forum.xda-developers.com/t/tools-zips-scripts-android-backup-and-restore-tools-multiple-devices-platforms.4016617/)
* [How to Unpack and Repack .CPB firmware/stock Rom](https://www.youtube.com/watch?v=KFtWQSFEdw4) [video]
* [How to unpack and repack boot.img](https://forum.xda-developers.com/t/how-to-unpack-and-repack-boot-img-full-guide-by-jai-sharma.3500773/)
* [Camera2 API, SHIM, and HAL 3.2 in Android 5.1](https://www.slideshare.net/ferriskychen/camera2-api-shim-and-hal-32-in-android-51)
* [An In-Depth Capitulation of Why MSM8974 Devices Are Excluded from Nougat](https://www.xda-developers.com/in-depth-capitulation-of-why-msm8974-devices-are-excluded-from-nougat/)
* [Android's HIDL: Treble in the HAL](https://www.youtube.com/watch?app=desktop&v=UFaWqdxBW4E) [2018] [video]
* [Android Framework - Creating custom HIDL in Android](https://www.youtube.com/watch?v=j1v5yTOfo-4) [2022] [video]
* [Android Treble: Blessing or Trouble?](https://www.youtube.com/watch?v=2XJAdK9XKcQ) [2018] [video]

##### Reverse Engineering

* [Reverse Engineering for Beginners](https://repository.root-me.org/Reverse%20Engineering/EN%20-%20Reverse%20Engineering%20for%20Beginners%20-%20Dennis%20Yurichev.pdf)
  * [Old version](https://ia601305.us.archive.org/22/items/ReverseEngineeringForBeginnersEnLite/Reverse_Engineering_for_Beginners-en-lite.pdf)
* [Patching your own init and sepolicy](https://forum.xda-developers.com/t/guide-arm32-patching-your-own-init-and-sepolicy.3558124/)
* [Discovering, reverse-engineering and using vendor HALs](https://forum.xda-developers.com/t/development-discovering-reverse-engineering-and-using-vendor-hals.3733410/)
* [On Device Debug! IDA+GDB trace automagic.apk](https://forum.xda-developers.com/t/on-device-debug-ida-gdb-trace-automagic-apk-in-s1-success.2050393/)
* [Cameras in Custom ROMs: How Developers Make Hardware Work without Source Code](https://www.xda-developers.com/cameras-custom-roms-developers-make-hardware-work-without-source-code/)
* [Example commit : add camera params shim](https://review.lineageos.org/c/LineageOS/android_device_samsung_universal8890-common/+/296858/6)
* [patch adbd to run as root](https://blog.mx17.net/2021/11/17/tolino-shine-3-patch-adbd-to-run-as-root/)
* [Getting ADB root access on a Tolino](https://cweiske.de/tagebuch/android-root-adb.htm)
* [Patching the adb daemon to run as root](https://harrisonsand.com/posts/patching-adb-root/)
* [Intro to Android App Reverse Engineering workshop](https://www.ragingrock.com/AndroidAppRE/)
  * [Github](https://github.com/maddiestone/AndroidAppRE)
* Android Attributes
  * [Value](https://www.temblast.com/ref/attrvalue.htmh)
  * [Name](ttps://www.temblast.com/ref/attrname.htm)
* Android Keycodes
  * [Code](https://www.temblast.com/ref/akeyscode.htm)
  * [Name](https://www.temblast.com/ref/akeysname.htm)
  * [API](https://www.temblast.com/ref/akeysapi.htm)
* [Android Versions](https://www.temblast.com/ref/aversions.htm)

#### Feature

##### Telephony

* [Enable VoLTE trhough modem mod (NV Items) ](https://www.reddit.com/r/GooglePixel/comments/7n8pes/enable_volte_trhough_modem_mod_nv_items/)
* [Android Telephony Basics](https://lineageos.org/engineering/Telephony/)
* [Remove HD ICON (IMS)](https://gist.github.com/Akianonymus/b7bbee7bdb3fe7dc2349fd0431279e41)
* [How to ENABLE VOLTE in any ONEPLUS device in Philippines](https://forum.xda-developers.com/t/how-to-enable-volte-in-any-oneplus-device-in-philippines.4349277/)

##### Encryption

* [Revisiting Android disk encryption](https://nelenkov.blogspot.com/2014/10/revisiting-android-disk-encryption.html?m=1)
* [Analysis of Android cryptfs](https://jsteward.moe/analysis-of-android-cryptfs.html)

##### Bluetooth

* [Improve Bluetooth audio quality on headphones without aptX or LDAC](https://forum.xda-developers.com/t/improve-bluetooth-audio-quality-on-headphones-without-aptx-or-ldac.3832615/)

##### Graphics

* [KCAL - Advanced color control for Qualcomm MDSS 8x10/8x26/8974/8084/8939](https://forum.xda-developers.com/t/dev-patch-kcal-advanced-color-control-for-qualcomm-mdss-8x10-8x26-8974-8084-8939.3032080/)
* [Adreno idler, an idling algorithm for devfreq-based Adreno devices](https://forum.xda-developers.com/t/adreno-idler-an-idling-algorithm-for-devfreq-based-adreno-devices.3134872/)

##### Audio

* [Omni SoundPacks](https://forum.xda-developers.com/t/rom-aosp-nightly-release-carbonrom-kitkat-maguro.2635637/page-27#post-52443494)
* [Enable HI-RES (24bits and over 48kHz sampling) on Xiaomi Redmi Note 9's family](https://forum.xda-developers.com/t/mod-guide-root-enable-hi-res-24bits-and-over-48khz-sampling-on-xiaomi-redmi-note-9s-family.4265823/)

##### Time

* [Update time zone data / tzdata / zoneinfo](https://forum.xda-developers.com/t/how-to-update-time-zone-data-tzdata-zoneinfo-day-saving-time-changes.1324935/)

##### Customization

* [OnePlus FingerPrint Material Icons ](https://forum.xda-developers.com/oneplus-6t/themes/app-theme-opfpcontrol-custom-t3899522/post78940274)
* [How to Change Boot Logo (Splash Screen) for Snapdragon Devices](https://forum.xda-developers.com/t/guide-how-to-change-boot-logo-splash-screen-for-snapdragon-devices-splash-img.3470473/)
* [Change Boot Logo for Exynos Samsung devices](https://forum.xda-developers.com/t/twrp-change-boot-logo-for-exynos-samsung-devices.4249909/)
* [How to change the official samsung splash/boot screen/logo](https://forum.xda-developers.com/t/how-to-change-the-official-samsung-splash-boot-screen-logo-samsung.3374170/)

#### Security

* [Building and flashing a secured AOSP build with verified boot and separate lockscreen password for the Nexus 5X](https://www.howtoforge.com/tutorial/building-and-flashing-a-secured-aosp-build-with-verified-boot-and-separate-lockscreen-password-for-the-nexus-5x/)
* [Signing Builds](https://wiki.lineageos.org/signing_builds)
* [Passing SafetyNet Hardware Attestation on Stock (OEM) ROMs](https://forum.xda-developers.com/t/dev-guide-proof-of-concept-passing-safetynet-hardware-attestation-on-stock-oem-roms.4228005/)
* [avbtool-arm](https://forum.xda-developers.com/t/beta-2017-10-01-supersu-v2-82-sr5.2868133/page-572#post-74498246)
* [Keeping SafetyNet Passing With Incremental Google OTA on Virtual A/B Devices](https://forum.xda-developers.com/t/tools-zips-scripts-osm0sis-odds-and-ends-multiple-devices-platforms.2239421/page-149#post-84764713)
* [Signing boot images for Android Verified Boot (AVB)](https://forum.xda-developers.com/t/signing-boot-images-for-android-verified-boot-avb-v8.3600606/)
* [Reflections on Trusting TrustZone](https://www.blackhat.com/docs/us-14/materials/us-14-Rosenberg-Reflections-on-Trusting-TrustZone.pdf) [pdf]

##### SELinux

* [How to examine Android SELinux policy](https://www.whitewinterwolf.com/posts/2016/08/15/examine-android-selinux-policy/)
* [Working with SELinux on Android](https://lineageos.org/engineering/HowTo-SELinux/)
* [SELinux for Android 8.0](https://source.android.com/static/docs/security/features/selinux/images/SELinux_Treble.pdf)
* [Netflix broken DRM workaround instructions (Nexus 7 2013)](https://forum.xda-developers.com/t/official-lineageos-14-1-nexus-7-2013-nightlies-for-flo.3502494/page-16#post-74374966)

##### Audio

* [Fix Bluetooth Audio A2DP & aptX in any GSI ROM](https://forum.xda-developers.com/t/guide-fix-bluetooth-audio-a2dp-aptx-in-any-gsi-rom.3950938/)
* [Fix Bluetooth Audio & aptX & Bluetooth in call in GSI ROM](https://forum.xda-developers.com/t/guide-fix-bluetooth-audio-aptx-bluetooth-in-call-in-gsi-rom.4455275/)

#### App integration

* [How to Port OEM Apps / Vendor Apps to Your Current ROM](https://forum.xda-developers.com/t/guide-tips-how-to-port-oem-apps-vendor-apps-to-your-current-rom.2476050/)
* [System App In Android](https://scribe.nixnet.services/android-news/system-app-in-android-f003d418b4cc)
* [System App In Android](https://sc.vern.cc/android-news/system-app-in-android-f003d418b4cc)

#### Optimization

* [Speed up your app](https://blog.udinic.com/2015/09/15/speed-up-your-app/)
* [Timing Boot Time Reduction Technique](https://bootlin.com/pub/conferences/2019/elce/opdenacker-timing-boot-time-reduction-techniques/opdenacker-timing-boot-time-reduction-techniques.pdf)
* [Low-RAM Property Patcher for Android](https://forum.xda-developers.com/t/mod-low-ram-property-patcher-for-android.3737373/)

#### Android CTS/VTS & test

* [How to build android cts? And how to add and run your test case?](https://stackoverflow.com/questions/2824015/how-to-build-android-cts-and-how-to-add-and-run-your-test-case)
* [Android VTS](https://budhdisharma.medium.com/android-vts-9e6ff95f075f)
* [Android CTS](https://budhdisharma.medium.com/android-cts-c790df99080)
* [Android System Stability Basics](https://budhdisharma.medium.com/android-system-stability-basics-e3bf63a928ca)
* [Android CTS](https://sc.vern.cc/@budhdisharma/android-cts-c790df99080)

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
* [How to take system logcats, kernel logs, and dmesg on Android](https://www.xda-developers.com/how-to-take-logs-android/)
* [HOW TO USE ADB,DDMS AND TAKE A LOGCAT](https://forum.xda-developers.com/t/win-tutorial-how-to-use-adb-ddms-and-take-a-logcat-pictorial-explanation.2303834/)
* [Using ADB and fastboot](https://wiki.lineageos.org/adb_fastboot_guide.html)
* [How to get useful logs](https://forum.xda-developers.com/t/reference-how-to-get-useful-logs.2185929/)
* [How to get & read a logcat/ Troubleshoot your own issues](https://forum.xda-developers.com/t/universal-logcat-how-to-get-read-a-logcat-troubleshoot-your-own-issues.2274119/)
* [Authorize ADB for a non-booting device](https://gist.github.com/AlvaroBrey/83d90a6a156790e06b8789447d273ace)
* [Most complete ADB command manual](https://dev.to/larsonzhong/most-complete-adb-commands-4pcg)
* [How to enable/disable Android logcat when using a custom kernel](https://blog.mx17.net/2015/01/13/enabledisable-android-logcat-using-custom-kernel/)
* [Debugging IO on Android](https://blog.mx17.net/2013/05/16/debugging-io-on-android/)
* [How to find Android deprecated API](https://blog.mx17.net/2012/09/11/how-to-find-android-deprecated-api/)

#### Magisk

* [How to patch classes.dex (SMALI) with a Magisk Module](https://forum.xda-developers.com/t/guide-how-to-patch-classes-dex-smali-with-a-magisk-module.4291935/)

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
* [Little Kernel Boot Loader Overview](https://developer.qualcomm.com/download/db410c/little-kernel-boot-loader-overview.pdf) (pdf)
* [Qualcomm® Snapdragon™ 410 processor, sensors Porting Guide](https://developer.qualcomm.com/qfile/28820/lm80-p0436-9_sensors_porting_guide.pdf) (2015/pdf)
* [Qualcomm® Snapdragon™ 410 processor, Interfacing Grove Digital Light I2C Sensor, Application Note](https://developer.qualcomm.com/download/db410c/interfacing-grove-digital-light-i2c-sensor-application-note.pdf) (2016/pdf)
* [Qualcomm® Snapdragon™ 410 processor, Software Build and Installation Guide, Linux Android](https://developer.qualcomm.com/download/db410c/linux-android-software-build-and-installation-guide.pdf) (2016/pdf)
* [Trying to use freedreno/turnip on Adreno 616](https://gitlab.freedesktop.org/mesa/mesa/-/issues/6802)
* [Qualcomm Audio/Usb DAC Optimization, Spl monitor, Biquad Helper](https://forum.xda-developers.com/t/qualcomm-audio-usb-dac-optimization-spl-monitor-biquad-helper.3253957/)
* [Unbricking and QPST - All Snapdragon / Qualcomm devices](https://forum.xda-developers.com/t/unbricking-and-qpst-all-snapdragon-qualcomm-devices.3451815/)
* [Ultimate Qualcomm Snapdragon Unbrick Guide, Snapdragon’s are UNBRICKABLE](https://www.androidbrick.com/ultimate-qualcomm-snapdragon-unbrick-guide-snapdragons-are-unbrickable-qhsusb_dload_qpst_qfil_edl/)
* [How to Use Qualcomm Flash Image Loader (QFIL)](https://consumingtech.com/use-qualcomm-flash-image-loader-qfil/)
* [Unbrick Qualcomm via QFIL: Using rawprogram0.xml, patch0.xml, MBN](https://www.droidwin.com/unbrick-qualcomm-via-qfil-using-rawprogram0-xml-patch0-xml-and-mbn-file/)
* [How to use QFIL to flash Qualcomm (QLM) firmware](https://www.youtube.com/watch?v=W9Cz4LwAzLg)
* [How to return to Stock/Flash Images with QFIL](https://forum.xda-developers.com/t/guide-how-to-return-to-stock-flash-images-with-qfil.3901510/)
* [How to use Qualcomm Flash Image Loader (QFIL)](https://xiaomitools.com/how-to-use-qualcomm-flash-image-loader-tool-qfil/)
* [How To Unbrick Qualcomm Android Devices](https://www.leakite.com/revised-how-to-unbrick-qualcomm-android/)
* [Unbrick via external sdcard (no QFIL!)](https://forum.xda-developers.com/t/guide-9008-edl-qdl-qualcomm-only-unbrick-via-external-sdcard-no-qfil.3748946/)
* [Unbrick Qualcomm Mobiles with Step-by-step Guide](https://www.droidsavvy.com/2021/03/unbrick-qualcomm-mobiles-with-step-by-step-guide.html)
* [How to fix bugs in custom rom (Qualcomm)](https://forum.xda-developers.com/t/how-to-fix-bugs-in-custom-rom-qualcomm.3894807/)
* [Optimize GPU 60FPS and CPU processors Qualcomm snapdragon](https://forum.xda-developers.com/t/tut-optimize-gpu-60fps-and-cpu-processors-qualcomm-snapdragon.3703430/)
* [Analysis of Qualcomm Secure Boot Chains](https://blog.quarkslab.com/analysis-of-qualcomm-secure-boot-chains.html)
* Exploiting Qualcomm EDL Programmers:
  1. [Gaining Access & PBL Internals](https://alephsecurity.com/2018/01/22/qualcomm-edl-1/)
  1. [Storage-based Attacks & Rooting](https://alephsecurity.com/2018/01/22/qualcomm-edl-2/)
  1. [Memory-based Attacks & PBL Extraction](https://alephsecurity.com/2018/01/22/qualcomm-edl-3/)
  1. [Runtime Debugger](https://alephsecurity.com/2018/01/22/qualcomm-edl-4/)
  1. [Breaking Nokia 6's Secure Boot](https://alephsecurity.com/2018/01/22/qualcomm-edl-5/)
* [Secure boot and image authentication in mobile tech (Qualcomm)](https://www.qualcomm.com/news/onq/2017/01/secure-boot-and-image-authentication-mobile-tech)
* [Secure Boot and Image Authentication (Technical Overview)](https://www.qualcomm.com/content/dam/qcomm-martech/dm-assets/documents/secure-boot-image-authentication_11.30.16.pdf) [pdf]
* [](https://www.androidbrick.com/unbrick-all-qualcomm-snapdragons-from-qualcomm-hs-usb-qdloader-9008-if-you-have-the-right-kind-of-rom-qhsusb_dload_edl/)
* [Notes about Qualcomm Secure Boot and Motorola High Assurance Boot](http://vm1.duckdns.org/Public/Qualcomm-Secure-Boot/Qualcomm-Secure-Boot.htm)
* [How to reboot to EDL from fastboot](https://forum.xda-developers.com/t/guide-how-to-reboot-to-edl-from-fastboot.3394292/)
* [NO Recovery mode, No download mode, after OTA on rooted LG G2 (& other devices)](https://forum.xda-developers.com/t/fix-no-recovery-mode-no-download-mode-after-ota-on-rooted-lg-g2.2582142/)
* [How to port twrp to qualcomm devices.](https://forum.xda-developers.com/t/guide-how-to-port-twrp-to-qualcomm-devices.3420013/)
* [MSM8909 Service Rom From Source / QPST Root + Unlock + Unbrick](https://forum.xda-developers.com/t/wip-rom-msm8909-service-rom-from-source-qpst-root-unlock-unbrick.3544178/)
* [Building Qualcomm modem from sources (msm8626)](https://forum.xda-developers.com/t/dev-guide-building-qualcomm-modem-from-sources-msm8626.3489833/)

##### MediaTek

* [How To Port TWRP For MediaTek Android Devices](https://techsbyte.com/how-to-port-twrp-for-mediatek-android-devices/)
* [How To Port TWRP To A/B Partitioned Devices (MediaTek)](https://techsbyte.com/how-to-port-twrp-to-a-b-partitioned-devices-mediatek/)
* [How to Decode LCM for Mediatek Devices](https://forum.xda-developers.com/t/guide-arm-how-to-decode-lcm-for-mediatek-devices.3599923/)
* [How To Port & Modify Roms For Mediatek](https://forum.xda-developers.com/t/guide-how-to-port-modify-roms-for-mediatek-everything.2707438/)
* [So what’s all this talk about Mediatek Secure Boot and DA files?](https://www.hovatek.com/blog/so-whats-all-this-talk-about-meditek-secure-boot-and-da-files/)
* [How to bypass authentication and flash in EDL with NO auth for FREE](https://forum.xda-developers.com/t/guide-how-to-bypass-authentication-and-flash-in-edl-with-no-auth-for-free.4229683/)
* [Dissecting a MediaTek BootROM exploit](https://tinyhack.com/2021/01/31/dissecting-a-mediatek-bootrom-exploit/)
* [How to port TWRP Recovery to Mediatek Devices](https://forum.xda-developers.com/t/guide-how-to-port-twrp-recovery-to-mediatek-devices-i-can-port-also.4027321/)
* [MTK ADB, Use ADB directly on your device](https://forum.xda-developers.com/t/app-mtk-adb-use-adb-directly-on-your-device.3313315/)
* [Make Custom ROM + Add ROOT for Unbranded Chinese Tablet](https://forum.xda-developers.com/t/make-custom-rom-add-root-for-unbranded-chinese-tablet-hw-mt6582-model-t906.3877701/)
* [Port/Make Custom Recovery For Any Spreadtrum OR Mediatek Devices](https://forum.xda-developers.com/t/guide-port-make-custom-recovery-for-any-spreadtrum-or-mediatek-devices.3506775/)
* [It's now easy to bypass MediaTek's SP Flash Tool authentication](https://www.xda-developers.com/bypass-mediatek-sp-flash-tool-authentication-requirement/)
* [How to use MTK Bypass to backup or flash secure boot MTK](https://www.hovatek.com/forum/thread-37957.html)
* [How to bypass authentication and flash in EDL with NO auth](https://forum.xda-developers.com/t/guide-how-to-bypass-authentication-and-flash-in-edl-with-no-auth-for-free.4229683/)
* [Minimal Porting Guide For MTK 64BIT Devices](https://forum.xda-developers.com/t/guide-minimal-porting-guide-for-mtk-64bit-devices.3772641/)
* [Manually splitting an MTK firmware (dump)](https://www.youtube.com/watch?app=desktop&v=w-LiHX_fHrg) [video]
* [MTK based tools to customize/split firmware](https://forum.xda-developers.com/t/mtk-guide-mtk-based-tools-to-customize-split-firmware-info.3902286/)
* [Create Scatter File and Dump Full ROM ](https://forum.xda-developers.com/t/guide-util-mt65xx-create-scatter-file-and-dump-full-rom.2540400/) [MT65xx]
* [Amazing Temp Root for MediaTek ARMv8](https://forum.xda-developers.com/t/amazing-temp-root-for-mediatek-armv8-2020-08-24.3922213/)

##### Raspberry Pi

* [Android On Raspberry Pi](https://budhdisharma.medium.com/android-on-raspberry-pi-7795e4914dc0)

##### Samsung

* [How To Build CyanogenMod For Samsung Galaxy Note 4 International ("trltexx")](https://fat-tire.github.io/build-los-trltexx.html)
* [How To Build CyanogenMod For Samsung Galaxy Note 4 T-Mobile ("trltetmo")](https://fat-tire.github.io/build-los-trltetmo.html)
* [Remove FRP Lock on Samsung with Combination File (Odin)](https://technastic.com/remove-frp-samsung-combination-file/amp/#Removing_FRP_on_Samsung_with_Combination_File)
* [how to build/modify roms for samsung devices](https://forum.xda-developers.com/t/guide-how-to-build-modify-roms-for-samsung-devices-7-0-6-0-1-maybe-more.3616040/)
* [How to make a System Dump from Odin-packages](https://forum.xda-developers.com/t/guide-tut-how-to-make-a-system-dump-from-odin-packages.3206327/)
* [Exploiting Android S-Boot: Getting Arbitrary Code Exec in the Samsung Bootloader](https://hexdetective.blogspot.com/2017/02/exploiting-android-s-boot-getting.html?m=1)
* [Restore stock firmware on the Galaxy A7 (2018) using Linux (and heimdall)](https://blog.mx17.net/2021/11/19/restore-stock-firmware-on-the-galaxy-a7-2018-using-linux/)

##### Google

* [Android Cookbook: Nexus Device Hacking 101](https://tomwwolf.wordpress.com/android/android-cookbook-hacking101-nexus/)
* [Connect USB peripherals to your Nexus One](https://sven.killig.de/android/N1/2.2/usb_host/)

##### Motorola

* [Downgrade Motorola Devices](http://www.droidrzr.com/topic/54902-how-to-downgrade-motorola-devices/)
* [Motorola Flashing Utilities and Firmware (Unbrick Your Moto)](https://forum.xda-developers.com/t/index-motorola-flashing-utilities-and-firmware-unbrick-your-moto.3042687/)
* [Motorola Stock Firmware](https://forum.xda-developers.com/t/index-motorola-stock-firmware.4222605/)
* [Using Fastboot.exe with Motorola devices](https://forum.xda-developers.com/t/guide-using-fastboot-exe-with-motorola-devices.4042039/)
* [How to Firmware Restore your Motorola Device on Windows 10 without RSDlite](https://www.youtube.com/watch?v=njXQYn53SPc)
* [Un/locking Motorola Bootloader](https://forum.xda-developers.com/t/guide-un-locking-motorola-bootloader.4079111/)
* [Emergency Download Mode](https://forum.xda-developers.com/t/index-motorola-flashing-utilities-and-firmware-unbrick-your-moto.3042687/page-6#post-80035788)
* [Recovering from a hard brick](https://forum.xda-developers.com/t/guide-recovering-from-a-hard-brick.3989753/)
* [Motorola Firmware XML to Bat Converter Tool for Windows](https://www.youtube.com/watch?v=dqAGWVPYmNo)
* [P2K Tools](https://firmware.center/software/Motorola/)
* [How download latest fastboot firmware with Lenovo Moto Smart Assistant](https://forum.xda-developers.com/t/guide-stock-how-download-latest-fastboot-firmware-with-lenovo-moto-smart-assistant.3916778/)

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
* [Getting Freedreno Turnip (Mesa Vulkan Driver) on a Poco F3](https://forum.xda-developers.com/t/getting-freedreno-turnip-mesa-vulkan-driver-on-a-poco-f3.4323871/)
* [All about Spreadtrum](https://forum.xda-developers.com/t/ultimate-guide-sc6820-sc8810-all-about-spreadtrum.2998862/)
* [Bootloader Unlocking on older Qualcomm ZTE Devices](https://forum.xda-developers.com/t/bootloader-unlocking-on-older-qualcomm-zte-devices-devinfo-partition-modification.4100897/)
* [Unbrick Tutorial For The OnePlus 3T](https://forum.xda-developers.com/t/unbrick-unbrick-tutorial-for-the-oneplus-3t-by-haris-k.3515306/)
* [Unbrick Oneplus One](https://forum.xda-developers.com/t/guide-unbrick-unbrick-oneplus-one.3013732/)
* [OnePlus One / Two / 3 / 3T / 5 Mega UNBRICK Guide + TWRP Flashing](https://www.androidbrick.com/unbrick-oneplus-one-two-3-3t-qualcomm-hs-usb-qdloader-9008/)
* [Modding the Redmi Note 8 Pro — An Adventure](https://medium.com/swlh/modding-the-redmi-note-8-pro-an-adventure-e473e84d4d14)
* [FM Radio app by HTC: Reverse Engineer](https://forum.xda-developers.com/t/success-fm-radio-app-by-htc-reverse-engineer-please-help.971303/)

#### Rom specific

##### TWRP

* [How to create twrp device tree from scratch](https://www.youtube.com/playlist?list=PLsljP0DCGt1EBN4X-NR3-oS6f1NYxLLQA)
* [How to DIY Port TWRP for Android](https://appuals.com/how-to-diy-port-twrp-for-android/)
* [How to compile TWRP from source step by step](https://forum.xda-developers.com/t/guide-noob-friendly-how-to-compile-twrp-from-source-step-by-step.3404024/)
* [Compile LineageOS TWRP: Setting up minimal LineageOS TWRP](https://www.youtube.com/watch?v=7xdIxiiHLlc)
* [TWRP Flags for BoardConfig.mk](https://forum.xda-developers.com/t/twrp-flags-for-boardconfig-mk.3333970/)
* [How to compile TWRP touch recovery](https://forum.xda-developers.com/t/dev-how-to-compile-twrp-touch-recovery.1943625/)
* [TWRP standard device files for Qualcomm SoCs decryption](https://github.com/TeamWin/android_device_qcom_twrp-common)
* [How generate TWRP with TwrpBuilder](https://github.com/TwrpBuilder/twrpbuilder_tree_generator/wiki)
* [TWRP tree from scratch](https://www.youtube.com/playlist?list=PLRJ9-cX1yE1lnwTD8QP_e5Ohj8Ys-0oO7)
* [Android.mk : a set of tag](https://github.com/TeamWin/android_bootable_recovery/blob/android-12.1/Android.mk)
* [Compile TWRP](https://www.youtube.com/playlist?list=PLRJ9-cX1yE1kzxSkdZSG_h_f-GDNmSmAl)
* [How to compile TWRP touch recovery](https://forum.xda-developers.com/t/dev-how-to-compile-twrp-touch-recovery.1943625/#post-32965365)
* [TWRP 3.0.X for Mediatek Devices.](https://forum.xda-developers.com/t/guide-port-twrp-3-0-x-for-mediatek-devices.3379681/)

##### LineageOS

* [How To Port CyanogenMod/LineageOS Android To Your Own Device](https://fat-tire.github.io/porting-intro.html)
* [How to adapt a LineageOS device tree for AOSP](https://theautomatedparts.com/apblog/?p=12)
* [How-to Build LineageOS​](https://forum.xda-developers.com/t/guide-build-lineageos-how-to-use-github.3551484/)
* [How To Port CyanogenMod Android To Your Own Device (archive wiki)](https://web.archive.org/web/20161224192644/https://wiki.cyanogenmod.org/w/Doc:_porting_intro)
* [How to port SONY Small Apps to Any Device Cm Based Roms](https://forum.xda-developers.com/t/guide-how-to-port-sony-small-apps-to-any-device-cm-based-roms.2228969/)

##### ArrowOS

* [ArrowOS Compilation guide](https://blog.arrowos.net/android/arrowos/guides/compilation-guide/)

##### OmniROM

* [OmniROM - Porting Omni to your device](https://github.com/omnirom/Docs/blob/master/Porting_Omni_To_Your_Device.md)

##### Other

* [Building Alternative Recoveries](https://www.youtube.com/playlist?list=PLRJ9-cX1yE1nQ2HgCoeJS3j_bpTIXh_Fe)
* [Definitive FAQ for newest miui](https://forum.xda-developers.com/t/guide-ics-jb-common-definitive-faq-for-newest-miui-porting.1777999/)
* [Build or Port MIUI ROM to Any Device](https://forum.xda-developers.com/t/guide-complete-build-or-port-miui-rom-to-any-device.3250984/)
* [How to port manufacturer ROM (Sense/Touchwizz...)](https://forum.xda-developers.com/t/guide-how-to-port-manufacturer-rom-sense-touchwizz-updated-for-kitkat.2245786/)
* [How to Build OrangeFox Recovery on a fox_6.0](https://forum.xda-developers.com/t/guide-how-to-build-orangefox-recovery-on-a-fox_6-0-android-6-0-build-system-recovery-manifest.4315785/)

### Tools

#### C language

* [The C Beginner's Handbook: Learn C Programming Language basics in just a few hours](https://www.freecodecamp.org/news/the-c-beginners-handbook/)

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
* [How to make your own repos to send us](https://telegra.ph/HOW-TO-MAKE-YOUR-OWN-REPOS-TO-SEND-US-04-20)
* [How to use Github](https://forum.xda-developers.com/t/guide-how-to-use-github.1877040/)

#### GNU Make

*There is also an awesome list with more resources : [awesome-make](https://github.com/adelarsq/awesome-make#readme)*

* [GNU Autotools: a tutorial](https://bootlin.com/pub/conferences/2016/elc/petazzoni-autotools-tutorial/petazzoni-autotools-tutorial.pdf)

#### Soong

* [Soong readme](https://android.googlesource.com/platform/build/soong/+/refs/heads/master/README.md) - Official documentation from Google.

#### Other

* [Odin on Linux](https://forum.xda-developers.com/t/guide-odin-on-linux.4548601/)

#### Ninja build

* [The Ninja build system](https://ninja-build.org/manual.html)

#### Reverse Engeenering

* [EVERYONE in Cyber Security Should Understand Reversing (its EASY)](https://www.youtube.com/watch?v=gh2RXE9BIN8) [2023] [video]
* [Simple Tools and Techniques for Reversing a binary](https://www.youtube.com/watch?v=3NTXFUxcKPc) [2016] [video]
* [Reverse Engineering #0 - Comment bien débuter et gagner du temps](https://www.youtube.com/watch?v=ur0iyh40HK0) [2021] [french]
* [Introduction to Firmware Reversing](https://www.youtube.com/watch?v=GIU4yJn2-2A) [video]
* [Patching Binaries (with vim, Binary Ninja, Ghidra and radare2)](https://www.youtube.com/watch?v=LyNyf3UM9Yc)
* [In-depth: ELF - The Extensible & Linkable Format](https://www.youtube.com/watch?v=nC1U1LJQL8o) [video]
* [android-scripts](https://github.com/strazzere/android-scripts) - Collection of Android reverse engineering scripts that makes life easier.
* [Frida Operation Manual - Android Environment Preparation](https://bbs-kanxue-com.translate.goog/thread-248293.htm?_x_tr_sl=auto&_x_tr_tl=en&_x_tr_hl=fr&_x_tr_pto=wapp) [[orginal language](https://bbs.kanxue.com/thread-248293.htm)]
* [Preliminary Exploration of Android Ransomware Virus](https://paper-seebug-org.translate.goog/1085/?_x_tr_sl=auto&_x_tr_tl=en&_x_tr_hl=fr&_x_tr_pto=wapp) [[original link](https://paper.seebug.org/1085/)]

##### IDA

* [Debugging Dalvik programs with IDA](https://www.hex-rays.com/wp-content/uploads/2019/12/debugging_dalvik.pdf) [pdf]
* [IDA – Remote debugging d’un process sous Android/Arm (Part1)](https://blog.overgen.com/messi89/reverse-engineering/ida-remote-debugging-android/) [french]

##### ghidra

* [How to reverse engineer JNI in Android with Ghidra](https://www.youtube.com/watch?app=desktop&v=wZC7Pzm3jRA)
* [ghidra-jni](https://github.com/extremecoders-re/ghidra-jni)
* [Reverse engineering with #Ghidra: Breaking an embedded firmware encryption scheme](https://www.youtube.com/watch?v=4urMITJKQQs)
* [Reverse engineering with ghidra](https://www.youtube.com/watch?v=d4Pgi5XML8E&list=PLIfB3Ur76mFghKTtY5v7y94Fn8m1qoNV-) [playlist]
* [Ghidra quickstart & tutorial: Solving a simple crackme](https://www.youtube.com/watch?v=fTGTnrgjuGA)

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
* newandroidbook.com
  * [HTC : Analyzing the WeakSauce Exploit](http://www.newandroidbook.com/Articles/HTC.html)
  * [HTCt : Analyzing the WeakSauce Exploit](http://www.newandroidbook.com/Articles/HTCt.html)
  * [KindleFS : Reconstructing the FireOS file system](http://www.newandroidbook.com/Articles/KindleFS.html)
  * [Nexus9 : Notes from a Nexus 9](http://www.newandroidbook.com/Articles/Nexus9.html)
  * [Sboot : DisARMing the Samsung S6E boot loader](http://www.newandroidbook.com/Articles/Sboot.html)
  * [aboot : Reverse Engineering Android's Aboot](http://www.newandroidbook.com/Articles/aboot.html)
* [arm Developer documentation](https://developer.arm.com/documentation/)
* [Linux kernel Backport wiki](https://backports.wiki.kernel.org/index.php/Main_Page)
* [Linux kernel Wireless wiki](https://wireless.wiki.kernel.org/welcome)

#### Qualcomm

* [Qualcomm Android Source Realease](https://wiki.codelinaro.org/en/clo/la/release)

#### Sony

* [Guides and Resources for Sony Xperia™ & AOSP](https://sx.ix5.org/info/)
* [Open Devices : Guides & Resources (Sony devices)](https://opendevices.ix5.org/resources/)


### Video Channel

* [AlaskaLinuxUser AKLU](https://www.youtube.com/c/AlaskaLinuxUserAKLU)
* [Android & Linux Development (@remainder30000)](https://www.youtube.com/@remainder30000)
* [Dimple S](https://www.youtube.com/@dimples_android_geek)
* [Haikal Luthfianino Balukia](https://www.youtube.com/@haikalluthfianinobalukia2423/videos)
* [OSP »» Android OS »» ROM »» Android Development](https://www.youtube.com/@aosp_android_tollcafe/videos)
* [opersys](https://www.youtube.com/@opersys/streams)

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
* [Easy EDL Flashing Tool](https://forum.xda-developers.com/t/easy-edl-flashing-tool.3958723/)
* [AABox2](https://forum.xda-developers.com/t/frp-unlock-bypass-with-all-tools-online-updated-expoits.3709593/) - Frp Unlock tool.
* [Android Advanced Box](https://forum.xda-developers.com/t/tool-android-advanced-box-samsung-mtk-spd-huawei-sony-lenovo-etc.3289128/) - Frp Unlock tool.
* [Android Script Creator](https://forum.xda-developers.com/t/tool-win-linux-mac-update-script-android-script-creator.2747279/)
* [DroidFlasher](https://github.com/ZorgeR/DroidFlasher)
* [GSD Android Tool](https://forum.xda-developers.com/t/dev-tool-gsd-android-tool-rvsecurity-maker-unlock-all-screen-lock-encryption-data.3690772/)
* [Pack of static Linux binaries for ARM/Android](https://forum.xda-developers.com/t/exe-static-linux-binaries-for-arm-android-cryptsetup-encfs-f2fs-tools-testdisk-photorec.3709380/)
* [TOOL ALL IN ONE](https://forum.xda-developers.com/t/tool-tool-all-in-one-drivers-unlock-twrp-factory-image-stock-recovery.3358711/)
* [f2fs-tools for cygwin](https://forum.xda-developers.com/t/tool-f2fs-tools-for-cygwin.4518521/)
* [Universal A/B-cloner](https://forum.xda-developers.com/t/slot-a-b-devices-universal-a-b-cloner.3973751/)
* [PC/GSI Build Automation Toolkit](https://forum.xda-developers.com/t/android-generic-project-pc-gsi-build-automation-toolkit.4132031/)
* [FRP Destroyer](https://forum.xda-developers.com/t/frp-destroyer-flashable-zip.3920067/)
* [Android Ultimate Toolbox Pro](https://forum.xda-developers.com/t/4-5-2013-util-win-android-ultimate-toolbox-pro-the-ultimate-android-utility.1886562/)
* [ClassyKitchen](https://forum.xda-developers.com/t/tool-windows-gui-classykitchen-for-android-roms-development.3862584/)
* [ROM2box](https://forum.xda-developers.com/t/tool-rom2box-all-in-one-frp-flashing-unlocking-tool.4477349/) [[sources](https://github.com/jeck24India/ROM2boxGUI)] - All in one FRP, Flashing & unlocking tool.
* [firehorse](https://github.com/alephsecurity/firehorse) - Research & Exploitation framework for Qualcomm EDL Firehose programmers
* [edlrooter](https://github.com/alephsecurity/edlrooter) - Root exploit for Google Nexus 6 using a leaked Qualcomm Emergency Download (EDL) Mode programmer.
* [Poison Kitchen IDE](https://forum.xda-developers.com/t/ide-roms-windows-poison-kitchen-ide-dev-preview-2-2-3-8-1.3779833/) - A powerful IDE for android ROM development.
* [ADBTouchScreenControl](https://forum.xda-developers.com/t/tool-windows-control-a-device-with-a-broken-screen-now-with-touchscreen-support.2786395/) [[source](https://github.com/kjanku1/ADBTouchScreenControl)] - Control a device with a broken screen.
* [Android Toolkit](https://forum.xda-developers.com/t/tool-macos-unix-android-toolkit.3804927/) [[sources](https://github.com/lorehaze/Android_Toolkit_MacOS)]
* [BlueStacks MultiTool](https://forum.xda-developers.com/t/tool-root-win-bluestacks-multitool-v1-21r1-auto-rooter-xposed-de-bloater-etc.2565644/)
* [Toybox](https://forum.xda-developers.com/t/tool-bin-official-toybox-for-android.3290884/)
* [ATA GUI](https://forum.xda-developers.com/t/tool-ata-gui-v1-9-6-open-source-app-manager-debloat-tool-and-more-adb-and-fastboot-commands.4249885/) - App manager, debloat tool and more.
* [Fastboot Unbrick Maker (FUM)](https://forum.xda-developers.com/t/fastboot-unbrick-maker-fum.4352353/)
* [Android_Unlocker](https://forum.xda-developers.com/t/official-android_unlocker-for-almost-all-smartphone.4206061/) [[sources](https://github.com/FabioFabRob7/Android_Unlocker)]
* [JURASSIC Universal Android Tool](https://forum.xda-developers.com/t/tool-sharing-jurassic-universal-android-tool-v-5-0-2-universal-win.3282400/)
* [DualBootPatcher](https://forum.xda-developers.com/t/guide-dualbootpatcher-use-build-from-source-using-docker-travis-and-add-new-devices.3663076/)

### Generator

* [TwrpBuilder](https://github.com/TwrpBuilder/twrpbuilder_tree_generator) - Generate twrp device tree just using recovery.img and build.prop.
* [twrpdtgen](https://github.com/twrpdtgen/twrpdtgen) [(doc)](https://github.com/twrpdtgen/twrpdtgen/wiki) - Create a TWRP device tree only from an Android recovery stock image ROM.
* [aospdtgen](https://github.com/sebaubuntu-python/aospdtgen) - Create a LineageOS-compatible device tree from an Android stock ROM dump made with dumpyara.

### Extractor/Repack/Patcher

* [abootimg](https://github.com/ggrandou/abootimg) - Manipulate Android boot images.
* [Android Deodexer](https://github.com/Akianonymus/Android_deodexer) - For deodex odexed android firmwares.
* [Android Image Kitchen](https://forum.xda-developers.com/t/tool-android-image-kitchen-unpack-repack-kernel-ramdisk-win-android-linux-mac.2073775/) - Unpack/repack kernel and recovery images, and edit the ramdisk.
* [bootimgtool](https://github.com/vianney/bootimgtool) - Unpack/pack Android boot.img.
* [dextra](http://newandroidbook.com/tools/dextra.html) - An alternative to dexdump for displaying information about .dex files.
* [Firmware Extraction](https://github.com/Akianonymus/Firmware_Extraction) - Regroupment of available firmware extractors.
* [imjtool](http://newandroidbook.com/tools/imjtool.html) - A quick extractor of Android images.
* [ROME](https://code.binbash.rocks:8443/mAid/android_rome) - [ROM] [E]xtractor, a simple GUI for extracting custom and stock ROMs containing.
* [Universal Deodexer V5](https://forum.xda-developers.com/t/massive-update-software-gui-windows-universal-deodexer-v5-version-5.2213235/)
* [DJBTool](https://forum.xda-developers.com/t/tool-win-2017-09-10-djbtool-v1-05-apk-jar-de-compiling-tools.3455067/)
* [kpack](https://forum.xda-developers.com/t/unpack-repack-kernel-image-partition-ramdisk.4098497/)
* [mmcblk0 Extractor](https://forum.xda-developers.com/t/tool-linux-mmcblk0-extractor-v1-0-1-3-16-16.3306883/)
* [ANDROID_IMG_REPACK_TOOLS](https://forum.xda-developers.com/t/tool-android_img_repack_tools.2600364/)
* [Henry's unpacker - unpack repack system/vendor images](https://forum.xda-developers.com/t/tool-works-with-android-11-henrys-unpacker-unpack-repack-system-vendor-images.4139005/)
* [Multi Image Kitchen](https://forum.xda-developers.com/t/kitchen-windows-multi-image-kitchen-repack-android-partitions.4326387/)
* [Dex Manager](https://forum.xda-developers.com/t/tool-windows-dex-manager-v1-1-designed-to-play-with-classes-dex-updated.2988532/)
* [DexPatcher](https://forum.xda-developers.com/t/tool-dexpatcher-modify-android-applications-at-source-level-in-android-studio.3060854/)
* [TurkDevs İmage Kitchen](https://forum.xda-developers.com/t/tool-turkdevs-image-kitchen-boot-recovery-system-img-dat-ext4-win-up-v2-1.3816395/)
* [unmkbootimg](https://forum.xda-developers.com/t/util-unmkbootimg.1877807/)
* [payload_dumper.py](https://gist.github.com/ius/42bd02a5df2226633a342ab7a9c60f15)
* [update_payload_extractor](https://github.com/gmrt/update_payload_extractor)
* [IMG Patch Tools](https://github.com/erfanoabdi/imgpatchtools)
* [Firmware_extractor](https://github.com/erfanoabdi/Firmware_extractor)
* [apk.sh](https://forum.xda-developers.com/t/apk-sh-makes-reverse-engineering-android-apps-easier.4513735/) [[sources](https://github.com/ax/apk.sh)] - Makes reverse engineering Android apps easier.
* [apktool](https://ibotpeaches.github.io/Apktool/) [[sources](https://github.com/iBotPeaches/Apktool)]
* [IDA](https://hex-rays.com/ida-free/) [[Pro](https://hex-rays.com/ida-pro/)]
* [mkbootimg_tools](https://github.com/xiaolu/mkbootimg_tools) [[help](https://forum.xda-developers.com/t/development-mkbootimg-tools.2895954/)]
* [APK-Patcher](https://forum.xda-developers.com/t/dev-template-apk-patcher-easily-mod-apks-from-recovery-flashable-zip.3298945/) - Flashable Zip Template for Modifying System APKs On-Device from Recovery.
* [Jancox Tool Unpack Repack ROMs](https://forum.xda-developers.com/t/tool-linux-android-windows-jancox-tool-unpack-repack-roms.4068281/) [sources [1](https://github.com/Wahyu6070/Jancox-tool-linux),[2](https://github.com/Wahyu6070/Jancox-tool-linux),[3](https://github.com/Wahyu6070/Jancox-tool-android),[4](https://github.com/Wahyu6070/Jancox-Tool-Windows)/android,linux,windows/[download](https://wahyu6070.github.io/tools/jancox-tool)] - For unpacking and repacking ROMs.
* [GNU Nano editor v2.2.6 for Android](https://forum.xda-developers.com/t/binary-gnu-nano-editor-v2-2-6-for-android.1530519/)
* [LazyFlasher](https://forum.xda-developers.com/t/zip-lazyflasher-the-swiss-army-knife-of-flashing-custom-kernels.3549210/) [[sources](https://github.com/jcadduono/lazyflasher)] - the swiss army knife of flashing custom kernels.
* [AnyKernel3](https://forum.xda-developers.com/t/dev-template-anykernel3-easily-mod-rom-ramdisk-pack-image-gz-flashable-zip.2670512/) [[sources](https://github.com/osm0sis/AnyKernel3/)/[download](https://github.com/osm0sis/AnyKernel3/archive/master.zip)] Flashable Zip Template for Kernel Releases with Ramdisk Modifications.
* [Unpack Repack System.img & System.new.dat](https://forum.xda-developers.com/t/tool-windows-tool-unpack-repack-system-img-system-new-dat-no-cygwin-no-linux.3280740/)
* [simg2img](https://github.com/anestisb/android-simg2img) - Convert Android sparse images to raw images.
* [IMG Patch Tools](https://forum.xda-developers.com/t/dev-linux-osx-img-patch-tools-sdat2img-for-ota-zips.3640308/) - sdat2img for OTA zips.
* [Carliv Image Kitchen](https://forum.xda-developers.com/t/tool-utility-carliv-image-kitchen-for-android-unpack-repack-boot-recovery.3013658/)
* [Android System Extraction and Repack Tool](https://forum.xda-developers.com/t/dev-tool-linux-android-system-extraction-and-repack-tool.3588311/) [[sources](https://github.com/iykex/android_system_extraction_and_repack_tool)/[download](https://github.com/iykex/android_system_extraction_and_repack_tool/releases/tag/v1.5)]

### Kernel

* [best-caf-kernel.py](https://github.com/LineageOS/scripts/blob/master/best-caf-kernel/best-caf-kernel.py) - Finding the best CAF tag for a vendor kernel.
* [Kernel Rebaser Script](https://github.com/Sushrut1101/android-kernel-rebaser) - Rebase an OEM kernel to Android Common Kernel base.
* [Toolchain build scripts](https://github.com/ClangBuiltLinux/tc-build) - A set of script for building kernel with LLCM, clang.
* [bldgcc](https://github.com/nathanchance/android-tools/blob/main/scripts/bldgcc) - Builds GCC and binutils for exclusively building kernels.
* [Automated Linux Kernel CVE Patcher](https://forum.xda-developers.com/t/tool-automated-linux-kernel-cve-patcher.4249547/)
* [Kernel Buildinator](https://forum.xda-developers.com/t/tool-linux-kernel-buildinator-by-siddharth-bharadwaj.4069605/) [[sources](https://github.com/SiddharthBharadwaj/Kernel_Buildinator)] - Automating as much part as possible of Kernel compiling process.

### Blob & vendor

* [Android-Blob-Utility](https://forum.xda-developers.com/t/blob-utility-for-aosp-based-roms.2794413/) [(sources)](https://github.com/JackpotClavin/Android-Blob-Utility) - Easily find which proprietary blobs is needed.
* [aosp-missing-blobs](https://github.com/joshchoo/aosp-missing-blobs) - Identify required blobs that are missing from AOSP ROM builds with dependencies.
* [DumprX](https://github.com/DumprX/DumprX) - Firmware extractor based on dumpyara.
* [dumpyara](https://github.com/AndroidDumps/dumpyara) - Dumping vendor and Android content of a device.
* [dumpyara (Python)](https://github.com/sebaubuntu-python/dumpyara) - Like dumpyara but code in Python.
* [ldcheck](https://github.com/that1/ldcheck) - Check dependencies and missing for a blob file.
* [Apktool](https://forum.xda-developers.com/t/util-nov-24-2022-apktool-tool-for-reverse-engineering-apk-files.1755243/)
* [Automated Device/Vendor Tree Deblobber](https://forum.xda-developers.com/t/tool-automated-device-vendor-tree-deblobber.4249559/)
* [Ghidra](https://ghidra-sre.org/) [[sources](https://github.com/NationalSecurityAgency/ghidra)] - A software reverse .engineering (SRE) framework
* [androguard](https://github.com/androguard/androguard) - Reverse engineering and pentesting for Android applications.
* [Dexcalibur](https://github.com/frenchyeti/dexcalibur) - An Android reverse engineering platform focus on instrumentation automation.
* [androidre](https://github.com/cryptax/androidre) - Reverse engineering Android.
* [gnirehtet](https://github.com/genymobile/gnirehtet) - Provides reverse tethering for Android.
* [Simplify](https://github.com/calebfenton/simplify) - Generic Android Deobfuscator.
* [Bytecode Viewer](https://github.com/konloch/bytecode-viewer) - A lightweight user-friendly Java/Android Bytecode Viewer, Decompiler & More.
* [Dobby](https://github.com/jmpews/Dobby) - A lightweight, multi-platform, multi-architecture hook framework.
* [Uber Apk Signer](https://github.com/patrickfav/uber-apk-signer) - A tool that helps to sign, zip aligning and verifying multiple Android application packages.
* [APKiD](https://github.com/rednaga/apkid) - Gives you information about how an APK was made.
* [APK Studio](https://vaibhavpandey.com/apkstudio/) [[source](https://github.com/vaibhavpandeyvpz/apkstudio)] - IDE for reverse-engineering Android application packages.

### Conversion

* [hidl2aidl](https://source.android.com/docs/core/architecture/aidl/aidl-hals#converting-to-aidl) - For Converting an existing HAL from HIDL to AIDL.
* [OMC Decoder Encoder](https://forum.xda-developers.com/t/decode-or-encode-omc-files-with-omc-decoder-encoder.3791471/)

### Informations

* [Device Info HW (playstore](https://play.google.com/store/apps/details?id=ru.andr7e.deviceinfohw&pli=1)/[paid version)](https://play.google.com/store/apps/details?id=ru.andr7e.deviceinfohw.pro) - A hardware and software information app for Android devices.
* [TrustDevice-Android](https://github.com/trustdecision/trustdevice-android) [(izzyondroid)](https://apt.izzysoft.de/fdroid/index/apk/com.trustdevice.android)- Get informations about security and other.
* [Codec Info](https://github.com/Parseus/codecinfo) ([playstore](https://play.google.com/store/apps/details?id=com.parseus.codecinfo)/[izzyondroid](https://apt.izzysoft.de/fdroid/index/apk/com.parseus.codecinfo)) - Detailed listing of multimedia codecs on your Android device.
* [TrebleInfo](https://gitlab.com/TrebleInfo/TrebleInfo) ([playstore](https://play.google.com/store/apps/details?id=tk.hack5.treblecheck)/[f-droid](https://f-droid.org/packages/tk.hack5.treblecheck/)/[izzyondroid](https://apt.izzysoft.de/fdroid/index/apk/tk.hack5.treblecheck)) -  Check the Treble GSI requirements and determine the correct GSI type for your device.
* [Kaltura Device Info](https://bitbucket.org/oF2pks/kaltura-device-info-android/src/master/) ([playstore](https://play.google.com/store/apps/details?id=com.kaltura.kalturadeviceinfo)/[f-droid](https://f-droid.org/fr/packages/com.oF2pks.kalturadeviceinfos/))
* [Devstat](https://ianfield.com/DevStat/) ([source](https://github.com/IanField90/DevStat)/[izzyondroid](https://apt.izzysoft.de/fdroid/index/apk/uk.co.ianfield.devstat)) - Help you debug a number device issues like identifying various features you request in your AndroidManifest.xml.
* [SysInfo](https://github.com/kl3jvi/sysinfo_app) ([izzyondroid](https://apt.izzysoft.de/fdroid/index/apk/com.kl3jvi.sysinfo)) - Simple and powerful application that gives you complete information about your mobile device.
* [Getevent](https://source.android.com/docs/core/interaction/input/getevent) - Provides information about input devices and a live dump of kernel input events.
* [validatekeymaps](https://source.android.com/docs/core/interaction/input/validate-keymaps) - Validate the syntax of input device configuration files, key layout files, key character maps files and virtual key definition files.
* [LibChecker](https://github.com/LibChecker/LibChecker) ([f-droid](https://f-droid.org/packages/com.absinthe.libchecker/)/[playstore](https://play.google.com/store/apps/details?id=com.absinthe.libchecker)) - View the third-party libraries used by applications in your device.
* [Debugging enabler](https://forum.xda-developers.com/t/tool-universal-deprecated-debugging-enabler.3467434/) [deprecated] - Allow a user to debug their device.
* [Bootimage ADB Unsecure Patcher](https://forum.xda-developers.com/t/mod-bootimage-adb-unsecure-patcher.3618558/) - Modify the ramdisk to set ADB into an unsecure mode in order to debug Android stock ROMs.
* [PhoNetInfo](https://www.patrickfrei.ch/phonetinfo/) [[playstore](https://play.google.com/store/apps/details?id=ch.patrickfrei.phonetinfo.free)/[paid](https://play.google.com/store/apps/details?id=ch.patrickfrei.phonetinfo)]

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
* [logcatTrimmer](https://ronaxdevil.github.io/logcatTrimmer/) [[source](https://github.com/ronaxdevil/logcatTrimmer)] - Logcat Trimmer on Website rather than 'grep'.
* [SysLog](https://github.com/Tortel/SysLog) [[f-droid](https://f-droid.org/packages/com.tortel.syslog/)/[playstore](https://play.google.com/store/apps/details?id=com.tortel.syslog)]
* [ADB Screenshot](https://forum.xda-developers.com/t/tools-zips-scripts-osm0sis-odds-and-ends-multiple-devices-platforms.2239421/) [[download](https://forum.xda-developers.com/attachments/adb-screenshot-v2-0-win32-zip.2786433/)] - Take screenshots while in recovery.
* [ADBsync sdcard Backup](https://forum.xda-developers.com/t/tools-zips-scripts-osm0sis-odds-and-ends-multiple-devices-platforms.2239421/) [[download](https://forum.xda-developers.com/attachments/adbsync-sdcard-backup-v2-1-win32-zip.5164097/)]
* [settingsdump.sh](https://forum.xda-developers.com/t/tools-zips-scripts-osm0sis-odds-and-ends-multiple-devices-platforms.2239421/) [[download](https://forum.xda-developers.com/attachments/settingsdump-sh-txt.1891970/)]
* [getprio](https://forum.xda-developers.com/t/tools-zips-scripts-osm0sis-odds-and-ends-multiple-devices-platforms.2239421/) [[download](https://forum.xda-developers.com/attachments/getprio-txt.2567372/)]
* [SELinux Audit2Allow Script](https://forum.xda-developers.com/t/tools-zips-scripts-osm0sis-odds-and-ends-multiple-devices-platforms.2239421/page-140#post-83309297) - A script snippet for turning SELinux audits in a logcat into allow statements ready for supolicy or magiskpolicy.
* [SELinux Audit2Allow Script](https://forum.xda-developers.com/t/app-2015-01-12-root-gnex-dev-bootunlocker-for-nexus-devices-version-1-6-1.1731993/page-29#post-67147071)
* [SEParser](https://forum.xda-developers.com/t/tool-separser-facilitate-working-with-selinux-sepolicy.3909807/) [[sources](https://github.com/andrwgldmn/SEcontexts_parser)/[download](https://github.com/andrwgldmn/SEcontexts_parser/releases/tag/1.0)] - Facilitate working with SELinux/SEPolicy.
* [εxodus trackers apk static analysis](https://forum.xda-developers.com/t/dexdump-exodus-trackers-apk-static-analysis.3833391/)
* [native-shim](https://github.com/rednaga/native-shim) - A "shim" for loading native jni files for Android active debugging.
* [reverse-hal.sh](https://github.com/phhusson/treble_experimentations/blob/master/vendor-HAL/reverse-hal.sh)
* [drmemory](https://github.com/dynamorio/drmemory) - Memory Debugger for Windows, Linux, Mac, and Android.
* [LiME - Linux Memory Extractor](https://github.com/504ensicslabs/lime) - A Loadable Kernel Module (LKM) which allows for volatile memory acquisition from Linux and Linux-based devices, such as Android.
* [Tinker](https://github.com/tencent/tinker) - A hot-fix solution library for Android, it supports dex, library and resources update without reinstalling apk.
* [binxml](https://www.temblast.com/android.htm) [[download](https://www.temblast.com/download/binxml)/[guide](https://www.temblast.com/ntxhwcfg.htm)] - Dump Android binary XML files (AndroidManifest.xml).
* [setvalues](https://www.temblast.com/android.htm) [[download](https://www.temblast.com/download/setvalues)] - Android settings from the shell.
* [zerostat](https://www.temblast.com/android.htm) [[download](https://www.temblast.com/download/zerostat)] - List partitions and show what percentage they are filled with actual data.
* [dtbview.exe](https://www.temblast.com/android.htm) [[download](https://www.temblast.com/download/dtbview.exe)] - A utility for viewing Device Trees (dtb files).
* [binxml.exe](https://www.temblast.com/android.htm) [[download](https://www.temblast.com/download/binxml.exe)] - A utility for dumping Android binary XML files (AndroidManifest.xml).
* [elfview.exe](https://www.temblast.com/android.htm) [[download](https://www.temblast.com/download/elfview.exe)] - A utility for viewing ELF executable files.
* [ImgUtil](https://www.temblast.com/imgutil.htm) [[download](https://www.temblast.com/download/imgutil.exe)] - ImgUtil is a Win32 utility for modifying Android boot images.
* [AdbSync](https://www.temblast.com/adbsync.htm) [[download](https://www.temblast.com/download/adbsync.exe)] - AdbSync is a Win32 utility for syncing files to and from an Android device.
* [DexDump](https://www.temblast.com/dexdump.htm) [[download](https://www.temblast.com/download/dexdump.exe)] - A simple utility for enumerating the classes in an application (.apk), a framework (.jar) or an extracted dex file.
* [JavaStub](https://www.temblast.com/javastub.htm) [[download](https://www.temblast.com/download/javastub.exe)] - For turning Android Dalvik Smali files into Java "stub" files.
* [MergeSmali](https://www.temblast.com/mergesmali.htm) [[download](https://www.temblast.com/download/mergesmali.exe)]
* [QcomView Utility](https://www.temblast.com/qcomview.htm) [[download](https://www.temblast.com/download/qcomview.exe)] - Itility for analyzing Qualcomm signed executables.
* [SepUtil](https://www.temblast.com/seputil.htm) [[download](https://www.temblast.com/download/seputil.exe)] - For modifying SE Linux sepolicy files.
* [https://www.temblast.com/adbgrab.htm](https://www.temblast.com/adbgrab.htm) [[download](https://www.temblast.com/download/adbgrab.exe)] - AdbGrab is a Win32 utility for grabbing the frame buffer of an Android device.
* [EDL Utility](https://www.temblast.com/edl.htm) [[download](https://www.temblast.com/edl.htm)] - A Win32 utility for accessing the Qualcomm Emergency Download interface on Qualcomm processors.
* [UsbMode](https://www.temblast.com/usbmode.htm)
  * [UsbMode-2.4.apk](https://www.temblast.com/download/UsbMode-2.4.apk)
  * [the usbhostd daemon](https://www.temblast.com/download/usbhostd)
* [WhatIsIt](https://www.temblast.com/whatisit.htm)
  * [Win32](https://www.temblast.com/download/whatisit.exe)
  * [Android](https://www.temblast.com/download/whatisit)
* [Temblast Android Applications](https://www.temblast.com/android.htm)
  * [AudioCtl-1.0.apk](https://www.temblast.com/download/AudioCtl-1.0.apk) – a simple utility for testing audio.
  * [Library-1.14.apk](https://www.temblast.com/download/Library-1.14.apk) – a simple library application.
  * [Lights-1.0.apk](https://www.temblast.com/download/Lights-1.0.apk) – a simple utility to adjust brightness and color of eink screens.
  * [NullKbd-1.2.apk](https://www.temblast.com/download/NullKbd-1.2.apk) – an IME that does nothing.
  * [Recorder-1.2.apk](https://www.temblast.com/download/Recorder-1.2.apk) – an audio recorder that can record 16 or 24 bit audio directly through ALSA.
  * [Touch-1.0.apk](https://www.temblast.com/download/Touch-1.0.apk) – a utility for testing Nook touch screens.

### Partitions, storage & data

* [iozone](https://fossies.org/linux/iozone/src/current/Android_Readme.md) - IO benchmark tool for Android.
* [JPT](http://newandroidbook.com/tools/jpt.html) - A "quick & dirty" GPT partition editor.
* [mtd-utils Installer](https://forum.xda-developers.com/attachments/update-mtd-utils-installer-v2-1-5-signed-zip.5766435/) [[download](https://forum.xda-developers.com/attachments/update-mtd-utils-installer-v2-1-5-signed-zip.5766435/)] - mtd-utils (flash_erase, nanddump, nandwrite).
* [Android File System (Network ADB Extension) for Windows Explorer](https://forum.xda-developers.com/t/tool-android-file-system-network-adb-extension-for-windows-explorer.3519741/)
* [Mount System as read write (Android 10+)](https://forum.xda-developers.com/t/script-linux-mount-system-as-read-write-android-10.4240703/)
* [Universal SystemRW / SuperRW feat. MakeRW / ro2rw](https://forum.xda-developers.com/t/closed-universal-systemrw-superrw-feat-makerw-ro2rw-read-only-2-read-write-super-partition-converter-by-lebigmac.4247311/)
* [Lanchon REPIT](https://forum.xda-developers.com/t/tool-lanchon-repit-the-data-sparing-repartitioning-tool-for-android.3358036/) [[sources](https://github.com/Lanchon/REPIT)] - The Data-Sparing Repartitioning Tool For Android.
* [e2fsck_ANDROID](https://forum.xda-developers.com/t/e2fsck_android.4214533/) [[sources](https://github.com/FabioFabRob7/e2fsck_ANDROID)]

### Magisk

* [TWRP A/B Retention Script Zip Module](https://forum.xda-developers.com/t/tools-zips-scripts-osm0sis-odds-and-ends-multiple-devices-platforms.2239421/page-102#post-77770683) [[source](https://github.com/Magisk-Modules-Repo/twrp-keep)]

### Drivers

* [ADB FASTBOOT AND Flashing Drivers Collection](https://forum.xda-developers.com/t/usb-flashing-drivers-adb-fastboot-and-flashing-drivers-qdloader-mtk-spd-samsung-and-others-collection.4370985/)
  * [LG Mobile Driver](https://forum.xda-developers.com/attachments/lg-mobile-driver-v4-8-0-zip.5475017/?hash=a2246ade1de8a4670e50229daf27342d)
  * [MTK USB All](https://forum.xda-developers.com/attachments/mtk_usb_all_v1-0-8-zip.5475019/?hash=a2246ade1de8a4670e50229daf27342d)
  * [Nokia USB Driver](http://nokia_usb_driver_v1.4.0/)
  * [QDLoader HS-USB Driver](https://forum.xda-developers.com/attachments/qdloader-hs-usb-driver_32_64bit_setup-zip.5475023/?hash=a2246ade1de8a4670e50229daf27342d)
  * [SAMSUNG USB Driver](https://forum.xda-developers.com/attachments/samsung_usb_driver_for_mobile_phones-zip.5475025/?hash=a2246ade1de8a4670e50229daf27342d)
  * [Sony Xperia Drivers](https://forum.xda-developers.com/attachments/sony-xperia-drivers-zip.5475027/?hash=a2246ade1de8a4670e50229daf27342d)
  * [SPD Driver](https://forum.xda-developers.com/attachments/spd_driver_r4-20-4201-zip.5475029/?hash=a2246ade1de8a4670e50229daf27342d) & [SPRD NPI USB Driver](https://forum.xda-developers.com/attachments/sprd_npi_usb_driver_v1-4-zip.5475031/?hash=a2246ade1de8a4670e50229daf27342d)
  * [Motorola Mobile Drivers](https://forum.xda-developers.com/attachments/motorola_mobile_drivers_v6-4-0-zip.5475037/?hash=a2246ade1de8a4670e50229daf27342d)
* [Yet Another Universal ADB Driver Package and adbupdater](https://forum.xda-developers.com/t/yet-another-universal-adb-driver-package-and-adbupdater-for-windows.3595277/)

### Other

* [Zip Builder v4.5.2 - Build and Sign ANY script based installer](https://forum.xda-developers.com/t/tool-windows-zip-builder-v4-5-2-build-and-sign-any-script-based-installer.3739556/)
* [Obfuscated apk decompile/recompile tool​](https://forum.xda-developers.com/t/obfuscated-apk-decompile-recompile-tool.4299213/)

### Vendor specific

#### Nexus

* [anestisb/android-prepare-vendor (Github)](https://github.com/anestisb/android-prepare-vendor) - A collection of utilities for Nexus devices.

#### LG

* [LGLAF](https://forum.xda-developers.com/t/tool-docs-lg-download-mode-laf.3285946/) [source [1](https://github.com/Lekensteyn/lglaf),[2](https://gitlab.com/runningnak3d/lglaf),[3](https://github.com/steadfasterX/lglaf)] - Utility for communication with LG devices in Download Mode.
* [SALT](https://forum.xda-developers.com/t/tool-locked-unlocked-salt-the-lg-up-revolution-begins.3717864/) [sources](https://github.com/steadfasterX/SALT) - Utility able to communicate with your device while in download mode.
* [LG-KDZ-dll-Tool/LGUP_UI-fixer/LG-Kdz-downloader](https://forum.xda-developers.com/t/lg-tools-lg-kdz-dll-tool-lgup_ui-fixer-lg-kdz-downloader.3916444/) [[sources](https://github.com/ehem/kdztools)]
  * LG-KDZ-dll-Tool - for extracting that dll from a kdz package.
  * LGUP_UI-fixer - Yet another little add-on for LGUP to do the same.
  * LG-Kdz-downloader - A small batch tool to download kdz files from LG servers.

#### MediaTek

* [SP Flash Tool](https://spflashtools.com/category/windows) [other source](https://spflashtool.com/)  - An application which mainly helps you to flash Stock ROM, Custom recovery and fixing in some extreme cases.
* [SP MDT Tool](https://spmdttool.com/) [potential virus!]
* [SoftwareDownload Tool](https://www.hovatek.com/forum/thread-23709.html)
* [MediaTek / MTK - Auth Bypass (SLA/DAA)](https://forum.xda-developers.com/t/mod-dev-mediatek-mtk-auth-bypass-sla-daa-utility.4232377/) [[website](https://m929.ru/_pages/mtk_bypass.html#)] - bypass Serial Link Authentication and Download Agent Authentication on supported devices.
  * [Bypass utility](https://github.com/MTK-bypass/bypass_utility)
  * [exploits_collection](https://github.com/MTK-bypass/exploits_collection)
* [MTK Droid Root & Tools](https://forum.xda-developers.com/t/util-win-mt65xx-mtk-droid-root-tools-mediatek-android-smartphone.2160490/)
* [MTK Scatter Studio for Windows](https://forum.xda-developers.com/t/tool-mtk-scatter-studio-for-windows.3656506/)
* [MTKClient](https://github.com/bkerler/mtkclient) [[download](https://github.com/bkerler/mtkclient/releases)] - MTK reverse engineering and flash tool.
  * [Guide](https://forum.xda-developers.com/t/guide-mtk-how-to-use-mtkclient-and-set-it-up.4509245/)

#### Qualcomm

* [QFIL Tool](https://qfiltool.com/) [potential virus!]
* [QPST Tool](https://qpsttool.com/) [potential virus!]
* [Qualcomm USB driver](https://androiddatahost.com/nbyn6) [potential virus!]
* [tzexec](https://github.com/eti1/tzexec) - Disable baseband firmware signature on Sony Xperia SP & Samsung s7275r.
* [pymdt](https://github.com/eti1/pymdt) - Python library for mdt firmware manipulation.

#### Samsung

* [Heimdall](https://github.com/Benjamin-Dobell/Heimdall) and [website](https://glassechidna.com.au/heimdall/) - A cross-platform open-source tool suite used to flash firmware onto Samsung devices.
* [Akhil99's Samsung Firmware Extractor](https://forum.xda-developers.com/t/tool-script-linux-win10-akhil99s-samsung-firmware-extractor-beta.4162333/)
* [frija](https://forum.xda-developers.com/t/tool-frija-samsung-firmware-downloader-checker.3910594/) [sources](https://github.com/SlackingVeteran/frija) - Download latest firmware for a Samsung device.
* [Bifrost](https://github.com/zacharee/SamloaderKotlin) - Yet another firmware downloader for Samsung devices.
* [FRP Removal Tool](https://forum.xda-developers.com/t/tool-samsung-your-frp-frp-removal-tool-updated-5-5-2020.4439497/)
* [Odin](https://forum.xda-developers.com/t/patched-odin-3-13-1.3762572/)
* [Freya](https://forum.xda-developers.com/t/tool-freya-v1-0-2-0-samsung-open-source-flash-tool.4518091/) [[source](https://github.com/Alephgsm/Freya)]
* [Thor](https://forum.xda-developers.com/t/abandoned-thor-open-source-samsung-flash-tool-with-additinal-features.4453437/) [[source](https://github.com/Samsung-Loki/thor)/[download](https://nightly.link/Samsung-Loki/Thor/workflows/build/main)[documentation](https://samsung-loki.github.io/samsung-docs/)] - An alternative to well-known Heimdall.
* [Multi CSC/OMC Auto-Maker [OMC/OPTICS/PRISM]](https://forum.xda-developers.com/t/tool-samsung-multi-csc-omc-auto-maker-omc-optics-prism.4222825/)

#### Sony

* [Flashtool](https://forum.xda-developers.com/t/tool-update-04-09-2015-flashtool-version-0-9-19-10-windows-linux-mac.920746/) [[sources](https://github.com/Androxyde/Flashtool)/[website](https://flashtool.net/index.html)/[download](https://flashtool.net/download.html)] - An Xperia device flashing tool.
* [UnSIN ~ SIN v3/v4/v5 Unpacker](https://forum.xda-developers.com/t/tool-unsin-sin-v3-v4-v5-unpacker-v1-13.3128106/) - An unpacker for Sony devices images.
* [XperiFirm](https://forum.xda-developers.com/t/tool-xperifirm-xperia-firmware-downloader-v5-6-5.2834142/) - Download the current firmware for all Sony Xperia-line smartphones, tablets and accessories.
* [anyxperia_dumper](https://forum.xda-developers.com/t/tool-windows-linux-android-apple-unpack-any-sony-firmware-file.3530077/) [[source](https://github.com/munjeni/anyxperia_dumper)] - Tool for dump any Sony Xperia image.
* [Xflasher](https://forum.xda-developers.com/t/tool-xflasher-xperia-command-line-flasher-for-pre-2017-devices.2986634/) [[sources](https://github.com/munjeni/xflasher)] - For flashing old xperia devices.

#### Huawei (and Honor)

* [PotatoNV](https://github.com/mashed-potatoes/PotatoNV) - Unlock bootloader for Huawei & Honor devices on Kirin SoC.

#### Xiaomi

* MiFlash
* [XiaoMiTool V2](https://www.xiaomitool.com/V2/)
* [Mi Flash Pro](https://miflashpro.com/)
* [Xiaomi Flash Tool](https://xiaomiflashtool.com/)
* [Xiaomi Flashable Firmware Creator](https://forum.xda-developers.com/t/tool-win-linux-mac-xiaomi-flashable-firmware-creator-v2-gui-cli.3871311/)
* [Xiaomi Firmware Updater](https://forum.xda-developers.com/t/all-devices-xiaomi-firmware-updater-v5-auto-updated-daily.3741446/) [[sources](https://github.com/XiaomiFirmwareUpdater/mi-firmware-updater)]
* [Xiaomi Sideload](https://forum.xda-developers.com/t/tool-xiaomi-sideload-read-flash-on-locked-bootloader.4512223/) - A Partition Management app for Xiaomi smartphone running on MIUI 13 & Newer.

#### Motorola

* [RSD Lite](http://www.droidrzr.com/topic/57858-motorola-tools-rsd-lite-usb-driver/) [[other source](https://rsdlitetool.com/) potential virus!/[other source](https://androidmtk.com/download-rsd-lite-tool) potential virus!]
* [House of Moto](http://www.droidrzr.com/topic/61124-house-of-moto-43/)
* [Fastboot Flasher](http://www.droidrzr.com/topic/35863-fastboot-flasher-prototype/)
* [RSD Flasher](http://www.droidrzr.com/topic/48904-rsd-flasher-beta-windows-only/)
* [Motorola OTA Link Generator Tool](https://forum.xda-developers.com/t/tool-motorola-ota-link-generator-tool.3537039/) [[sources](https://github.com/erfanoabdi/Motorola-OTA-Link-Generator-Tool)/[instance](https://motoota.lolinet.com/)]
* [LMSA: Lenovo's Motorola Smart Assistant ](https://support.lenovo.com/us/en/downloads/ds101291) [[help](https://forum.xda-developers.com/t/rescue-and-smart-assistant-lmsa-motorola-lenovo-only.3951714/)] - Is an official tool installs on PC.

### Users scripts

*You can use them as inspiration to create your own or find solutions*

* [akhilnarang/scripts (Github)](https://github.com/akhilnarang/scripts) - Some script useful for ROM development.
* [Build scripts](https://github.com/JarlPenguin/releases)
* [LineageOS scripts](https://github.com/LineageOS/scripts)
* [ShivamKumarJha/android_tools (Github)](https://github.com/ShivamKumarJha/android_tools) - Collection of scripts to help with Android ROM stuff.
* [android_helpful](https://github.com/hpnightowl/android_helpful)
* [Android Build Environment Scripts](https://github.com/CyberJalagam/android_rom_building_scripts)
* [XSans0/my-script](https://github.com/XSans0/my-script)

## Books

* Android Firmware Customization *by Arvind Choudhary* ([amazon](https://www.amazon.com/Android-Firmware-Customization-Arvind-Choudhary/dp/9385020293))
* Android Internals series *by Jonathan Levin* ([website](http://newandroidbook.com/)/[summary](http://newandroidbook.com/TOC.html))
  * Android Internals::Power User's View - *volume 1* ([amazon](https://www.amazon.com/gp/product/0991055586/ref=as_li_tl?ie=UTF8&camp=1789&creative=9325&creativeASIN=0991055586&linkCode=as2&tag=newosxbookcom-20&linkId=dee63bd17b404113dd16f234b5b904eb)/[free 2015 edition](http://newandroidbook.com/AIvI-M-RL1.pdf)/[wikileaks](https://wikileaks.org/ciav7p1/cms/files/AIvI-M-RL1.pdf))
  * Android Internals::Developer's View - *volume 2* ([amazon](https://www.amazon.com/dp/0991055543?&_encoding=UTF8&tag=newosxbookcom-20&linkCode=ur2&linkId=bb5d8363ae5c9a2be1dceb1745a229b8&camp=1789&creative=9325))
  * Android Internals::Security - *volume 3* (being written)
  * Android Internals::The Implementer's View - *volume 4* (being written)
* Android System Programming: Porting, customizing, and debugging Android HAL *by Roger Ye* ([amazon](https://www.amazon.com/Android-System-Programming-customizing-debugging/dp/178712536X))
* Android Security Internals: An In-Depth Guide to Android's Security Architecture *by  Nikolay Elenkov* ([amazon](https://www.amazon.com/Android-Security-Internals-Depth-Architecture/dp/1593275811))
* Embedded Android: Porting, Extending, and Customizing *by Karim Yaghmour* ([oreilly](https://www.oreilly.com/library/view/embedded-android/9781449327958/)/[amazon](https://www.amazon.com/_/dp/1449308295))
* Embedded Programming with Android: Bringing Up an Android System from Scratch *by Roger Ye* ([oreilly](https://www.oreilly.com/library/view/embedded-programming-with/9780134030920/)/[amazon](https://www.amazon.com/Embedded-Programming-Android-Bringing-Scratch/dp/0134030001))

## Online groupes

* [Reddit Android](https://www.reddit.com/r/Android/)
* [Reddit LineageOS](https://www.reddit.com/r/LineageOS/)

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
* [Android dumps](https://t.me/android_dumps)

### Forum

* [androidforums](https://androidforums.com/)
* [android-porting (Google Groups)](https://groups.google.com/g/android-porting)
* [droidrzr.com](http://www.droidrzr.com/index)
* [phonandroid (french)](https://www.phonandroid.com/forum/forums/developpement.13/) - French forum for ROM development.
* [XDA Forum](https://forum.xda-developers.com/)

## News

* [Android Champ blog](https://medium.com/android-knowledge-store)
* [LineageOS engineering blog](https://lineageos.org/engineering/)
* [LineageOS blog](https://lineageos.org/blog/)
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
* [NPX](https://www.nxp.com/)
  * [Github](https://github.com/NXPNFCLinux)
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
* Samsung firmware - *there are tools availables to directly download firmware, look at tools chapter*
  * [sammobile](https://www.sammobile.com/firmwares/)
  * [Galaxy Firmware](https://galaxyfirmware.com/)
  * [SamFw](https://samfw.com/)
  * [samfrew](https://samfrew.com/)
* Motorola firmware
  * [easy-firmware](https://easy-firmware.com/index.php?a=downloads&b=folder&id=12733)
* Xiaomi
  * [Official website download](https://new.c.mi.com/global/miuidownload/index)
  * [Xiaomi Firmware Updater](https://xiaomifirmwareupdater.com/)
  * [MiROM](https://mirom.ezbox.idv.tw/en/phone/)
* Google Nexus & Pixel
  * [Factory images](https://developers.google.com/android/images)
  * [Full OTA images](https://developers.google.com/android/ota)
  * [Vendor images](https://developers.google.com/android/drivers)
* Lenovo
  * [mirrors.lolinet.com](https://mirrors.lolinet.com/firmware/lenovo/)
* Motorola
  * [mirrors.lolinet.com](https://mirrors.lolinet.com/firmware/motorola/)
* [firmware.mobi](https://desktop.firmware.mobi/)
* [OnePlus](https://service.oneplus.com/fr/search/search-detail?id=2096330&articleIndex=1)

## GAPPS

* [BiTGApps](https://bitgapps.github.io/)
  * [Github](https://github.com/BiTGApps/BiTGApps)
  * [Documentation](https://bitgapps.github.io/docs/Home.html)
  * [FAQ](https://bitgapps.github.io/docs/FAQ.html)
  * [Download](https://bitgapps.github.io/latest.html)
* [FlameGApps](https://flamegapps.github.io/)
  * [Github](https://github.com/flamegapps)
  * [XDA thread](https://forum.xda-developers.com/t/gapps-arm64-flamegapps-for-android-10-0-11-0-12-0-12-1.4020917/)
  * [Download](https://flamegapps.github.io/download#downloads)
* [Fossapps creator](https://un.pixel-fy.com/)
  * [Github](https://github.com/wacko1805/Fossapps-creator)
* [LiteGapps](https://litegapps.site/)
  * [Github](https://github.com/litegapps)
  * [Gitlab](https://gitlab.com/litegapps)
  * [XDA thread](https://forum.xda-developers.com/t/litegapps-systemless-custom-gapps.4146013/)
  * [Download](https://sourceforge.net/projects/litegapps/files/)
  * [Documentation](https://litegapps.site/documentation.html)
* [microG](https://microg.org/) - A anti GAPPS, compatibility with Google Play Service apps without Google.
  * [Github](https://github.com/microg/GmsCore)
  * [Wiki](https://github.com/microg/GmsCore/wiki)
  * [LineageOS ROMs with microG](https://lineage.microg.org/)
  * [Download](https://microg.org/download.html)
  * [Alternative NanoDroid installation](https://nanolx.org/nanolx/nanodroid/)
* [NikGApps](https://nikgapps.com/)
  * [XDA thread](https://forum.xda-developers.com/t/android-13-gapps-nikgapps-arm64.3915866/)
  * [Download](https://sourceforge.net/projects/nikgapps/files/)
  * [FAQ](https://nikgapps.com/faqs)
  * [Create own configuration](https://github.com/nikgapps/config)
* [MindTheGapps](https://wiki.lineageos.org/gapps)
  * [Gitlab](https://gitlab.com/MindTheGapps)
  * [Download](http://downloads.codefi.re/jdcteam/javelinanddart/gapps)
  * [Download (Android TV)](http://downloads.codefi.re/jdcteam/javelinanddart/gapps/ATV)
* [OpenGApps](https://opengapps.org/)
  * [Github](https://github.com/opengapps/opengapps)
  * [Wiki](https://github.com/opengapps/opengapps/wiki)
  * [FAQ](https://github.com/opengapps/opengapps/wiki/FAQ)
  * [XDA thread](https://forum.xda-developers.com/t/gapps-daily-open-gapps-for-android-all-android-versions-devices.3098071/)
  * [XDA thread development](https://forum.xda-developers.com/t/q-a-gapps-2015-06-01-open-gapps-for-android-5-1-5-0-4-4.3124506/)

## ROMs

*Biggest ROMs projects. You can check her Gerrit instance for study how to port ROMs.*

* [Android AOSP](https://source.android.com/)
  * [Android Review Gerrit](https://android-review.googlesource.com/q/status:open+-is:wip)
* [CalyxOS](https://calyxos.org/)
  * [Matrix main channel](https://app.element.io/#/room/#CalyxOS:matrix.org)
  * [Matrix development](https://app.element.io/#/room/#calyxos-dev:matrix.org)
  * [Reddit](https://www.reddit.com/r/CalyxOS/)
  * [Development documentation](https://calyxos.org/docs/development/)
  * [Gitlab](https://gitlab.com/CalyxOS)
  * [Github](https://github.com/CalyxOS)
  * [Issues](https://gitlab.com/CalyxOS/calyxos/-/issues)
  * [Gerrit](https://review.calyxos.org/q/status:open+-is:wip)
* [GrapheneOS](https://grapheneos.org/)
  * [Build documentation](https://grapheneos.org/build)
  * [FAQ](https://grapheneos.org/faq)
  * [Releases](https://grapheneos.org/releases)
  * [Sources link](https://grapheneos.org/source)
  * [Github](https://github.com/GrapheneOS)
* [LineageOS](https://lineageos.org/)
  * [Github](https://github.com/LineageOS)
  * [Gerrit](https://review.lineageos.org/q/status:open+-is:wip)
  * [Issues](https://gitlab.com/LineageOS/issues)
  * [Translation](https://crowdin.com/project/lineageos)
  * [Wiki](https://wiki.lineageos.org/)
  * [IRC](https://kiwiirc.com/nextclient/irc.libera.chat#lineageos)
  * [Discord](https://discord.com/invite/gD6DMtf)
  * [Status infrastructure](https://status.lineageos.org/)
* [LineageOS with microG](https://lineage.microg.org/)
* [paranoidandroid](https://paranoidandroid.co/)
  * [Gerrit](https://gerrit.aospa.co/q/status:open+-is:wip)
* [ProtonAOSP](https://protonaosp.org/)
  * [Developers documentation](https://protonaosp.org/developers/download)
  * [Github](https://github.com/ProtonAOSP)
* [TWRP](https://twrp.me/)
  * [Github](https://github.com/TeamWin)
  * [Gerrit](https://gerrit.twrp.me/q/status:open+-is:wip)
  * [Community chat](https://twrp.zulipchat.com/join/zumqdy6spjszarpubcag4y33/)
* [OrangeFox Recovery](https://orangefox.download/)
  * [Github](https://github.com/OrangeFoxRecovery)
  * [Wiki](https://wiki.orangefox.tech/en/dev)
  * [Build varaibles](https://gitlab.com/OrangeFox/vendor/recovery/-/blob/master/orangefox_build_vars.txt)
  * [Example manifest](https://github.com/OrangeFoxRecovery/fox-6.0_manifest)
* [/e/OS](https://e.foundation/)
  * [Gitlab](https://gitlab.e.foundation/e)
  * [Documentation](https://doc.e.foundation/)
  * [Devices supported](https://doc.e.foundation/devices)

## Sources example

*Source code for some project related to Android AOSP.*

* [Android AOSP mirror Github](https://github.com/aosp-mirror/platform_development)
* [Android dummy trees](https://github.com/AndroidBlobs/) - Device & kernel repositories as reference for many devices.
* [android-linux-stable (archive)](https://github.com/android-linux-stable)
* [Minimal manifest for TWRP](https://github.com/minimal-manifest-twrp)
* [Linux kernel](https://git.kernel.org/pub/scm/linux/kernel/git/stable/linux.git/)
* [Freedreno](https://docs.mesa3d.org/drivers/freedreno.html), an open source GPU driver for Qualcomm SoC
  * [Wiki](https://gitlab.freedesktop.org/freedreno/freedreno/-/wikis/home)
  * [Sources](https://gitlab.freedesktop.org/mesa/mesa/-/tree/main/src/freedreno)
  * [Issues](https://gitlab.freedesktop.org/mesa/mesa/-/issues/?label_name%5B%5D=freedreno)
* [LineageOS Source Device Tree Template](https://github.com/imasaru/android_device_tree_template) - Build device trees and port custom ROMs and recoveries to new devices easily with this template.
* [Example commit to log device startup](https://github.com/aoleary/device_lge_g4-common/commit/073490b8a5056d5d59c2bea04d6648f423db3a35)
* [Magisk](https://github.com/topjohnwu/Magisk)
  * [Download](https://github.com/topjohnwu/Magisk/releases)
  * [Installation instruction](https://topjohnwu.github.io/Magisk/install.html)
  * [Documentation](https://topjohnwu.github.io/Magisk/)

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
* [awesome-reverse-engineering](https://github.com/alphaSeclab/awesome-reverse-engineering/blob/master/Readme_full_en.md)
* [osm0sis' Odds and Ends](https://forum.xda-developers.com/t/tools-zips-scripts-osm0sis-odds-and-ends-multiple-devices-platforms.2239421/)
* [Temblast Android Applications, Tools and Patches](https://www.temblast.com/android.htm)
* [Reverse-Engineering](https://github.com/OshekharO/Reverse-Engineering) - List resources about reverse engineering.
* [awesome-reversing](https://github.com/tylerha97/awesome-reversing)
* [Awesome Java](https://github.com/akullpp/awesome-java)

## Todo
* <https://github.com/davisRoman/aosp-research>
* <https://forum.xda-developers.com/t/lists-guide-ride-from-a-newbie-to-a-dev-get-all-you-need-here.2281656/>
* <https://forum.xda-developers.com/t/guide-basic-and-intermediate-development-guides-for-interested-devs-collection.1750733/>
* <https://www.temblast.com/android.htm>
* <https://forum.xda-developers.com/t/wip-rom-msm8909-service-rom-from-source-qpst-root-unlock-unbrick.3544178/>
* <https://forum.xda-developers.com/t/help-interactive-help-forum-tutorials-where-questions-are-encouraged.1605509/>
* <https://github.com/ysh329/android-reverse-engineering>

## Contributing

Contributions welcome! Read the [contribution guidelines](contributing.md) first.
