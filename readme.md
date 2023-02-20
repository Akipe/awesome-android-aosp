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
  - [Where to start](#where-to-start)
    - [Formation](#formation)
  - [Specific point](#specific-point)
- [Documentation](#documentation)
  - [Video Channel](#video-channel)
- [Tools](#tools)
- [Videos](#videos)
- [Books](#books)
- [Telegram channel](#telegram-channel)
- [News](#news)
- [Vendors open source](#vendors-open-source)
- [Some device project](#some-device-project)
- [Related awesome](#related-awesome)
- [Contributing](#contributing)

## Learning

### Where to start

* [Get started with Android Development (source.android.com)](https://source.android.com/docs/setup) - Official guide to beggining Android AOSP development.
* [eyedeekay/android_porting_guidebook (github)](https://github.com/eyedeekay/android_porting_guidebook) - An (incomplete) guide book for porting Android ROM.
* [Android OS Internals / AOSP Mobile ROM Development (udemy)](https://www.udemy.com/course/android-os-internals-aosp-mobile-development-2020-edition/) - A paid course for learning Android OS development.
* [Android OS Internals / AOSP Automotive ROM Development (udemy)](https://www.udemy.com/course/android-os-internals-aosp-automotive-development/) - A paid course for learning Android OS development.
* [Android OS Internals / AOSP in Depth (udemy)](https://www.udemy.com/course/android-os-internals-aosp-in-depth/) - A paid course for learning Android OS development.
* [Android ROM Development From Source To End (XDA)](https://forum.xda-developers.com/t/guide-complete-android-rom-development-from-source-to-end.2814763/)
* [Android Device Tree Bringup](https://blog.realogs.in/android-device-tree-bringup/)
* [Introduction to AOSP](https://blog.realogs.in/getting-started-with-aosp/)
* [Android Build System](https://elinux.org/Android_Build_System)

#### Formation

* [Android Internals](http://technologeeks.com/course.jl?course=AIRE)

### Specific point

* [Tutorial: Android Internals - Building a Custom ROM, Pt. 1 of 2 (Youtube)](https://www.youtube.com/watch?app=desktop&v=1_H4AlQaNa0)
* [Building The Android Open Source Project (4 parts)](https://littlelostandroid.wordpress.com/2015/11/28/building-the-android-open-source-project/)
* [Android Tools (Github)](https://github.com/nathanchance/Android-Tools/) - Contains public guides and scripts tailored for custom Android Development.
* [How to examine Android SELinux policy](https://www.whitewinterwolf.com/posts/2016/08/15/examine-android-selinux-policy/)
* [Extract vendor from stock firmware (Sony Xperia Z7 Premium)](https://forum.xda-developers.com/t/guide-extract-vendor-from-stock-firmware.4212587/)
* [AOSP Part 1: Get the code using the Manifest and Repo tool](https://blog.udinic.com/2014/05/24/aosp-part-1-get-the-code-using-the-manifest-and-repo/)
* [AOSP Part 2: Build variants](https://blog.udinic.com/2014/06/04/aosp-part-2-build-variants/)
* [AOSP Part 3: Developing Efficiently](https://blog.udinic.com/2014/07/24/aosp-part-3-developing-efficiently/)
* [Speed up your app](https://blog.udinic.com/2015/09/15/speed-up-your-app/)
* [AOSP: Advanced Development Tricks ](https://www.inovex.de/de/blog/aosp-advanced-development-tricks/)
* [How to build Custom ROMs and Kernels![10,P,O,N,M,L]](https://forum.xda-developers.com/t/guide-video-tutorial-how-to-build-custom-roms-and-kernels-10-p-o-n-m-l.3814251/)
* [Intermediate to Advanced Custom Rom and Kernel Building](https://forum.xda-developers.com/t/guide-video-tutorial-intermediate-to-advanced-custom-rom-and-kernel-building.3823927/)
* [How to Port OEM Apps / Vendor Apps to Your Current ROM](https://forum.xda-developers.com/t/guide-tips-how-to-port-oem-apps-vendor-apps-to-your-current-rom.2476050/)
* [Using Gerrit code review](https://forum.xda-developers.com/t/guide-using-gerrit-code-review.3720802/)
* [Making Dump Files Out of Android Device Partitions](https://forum.xda-developers.com/t/guide-making-dump-files-out-of-android-device-partitions.2450045/)
* [How to build android cts? And how to add and run your test case?](https://stackoverflow.com/questions/2824015/how-to-build-android-cts-and-how-to-add-and-run-your-test-case)
* [Building AOSP, fastbooting on device](https://scribe.rip/@sohambhattacharya/building-aosp-fastbooting-on-device-eae05938cef8)
* [Vendor Blob Extraction (v2)](https://baalajimaestro.me/posts/extract-vendor-2/)
* [Working with SELinux on Android](https://lineageos.org/engineering/HowTo-SELinux/)
* [Qualcomm’s Chain of Trust](https://lineageos.org/engineering/Qualcomm-Firmware/)
* [Verified Boot](https://source.android.com/docs/security/features/verifiedboot)
* [Device Tree Reference](https://elinux.org/Device_Tree_Reference)
* [Implementing dm-verity](https://source.android.com/docs/security/features/verifiedboot/dm-verity)
* [Some problems that can occur while rom compilation and their solutions(especially for lettuce)](https://github.com/hpnightowl/android_helpful/blob/master/errors.txt)
* [How To Port TWRP For MediaTek Android Devices](https://techsbyte.com/how-to-port-twrp-for-mediatek-android-devices/)
* [How To Extract Your Stock Firmware from Your Android Device](https://techsbyte.com/how-to-extract-your-stock-firmware-from-your-android-device/)
* [How To Port TWRP To A/B Partitioned Devices (MediaTek)](https://techsbyte.com/how-to-port-twrp-to-a-b-partitioned-devices-mediatek/)
* [How to adapt your Device Tree to aosp and compile AOSP-11 from source Full Guide](https://www.youtube.com/watch?v=evw3QkAE1Jw&t=123s)
* [how to compile AOSP-10 from source and adapt device tree to pure aosp full guide](https://www.youtube.com/watch?v=KV0IkuRgZpA)
* [AOSP Introduction : AOSP Source Code Analysis Lecture 1](https://www.youtube.com/watch?v=MsUhQMz30J4)
* [Android Framework - Device Tree in Android](https://www.youtube.com/watch?v=KA4TKFKyCMc&t=11s)
* [Cara Port Custom ROM AOSP | Android 10](https://www.youtube.com/watch?v=kwnQVY1Wn6s)

## Documentation

* [Android Open Source Project](https://source.android.com/) - Official documentation for Android AOSP
* [Android Code Search](https://cs.android.com/android)
* [LineaOS wiki](https://wiki.lineageos.org/)
* [J's Android Device Database](http://newandroidbook.com/ddb/)
* [XDA Forum](https://forum.xda-developers.com/)
* [XDA Forum : Android Development and Hacking](https://forum.xda-developers.com/c/android-development-and-hacking.564/)
* [XDA Forum : XDA-University](https://forum.xda-developers.com/f/xda-university.2060/)
* [XDA Forum : Android Software Development](https://forum.xda-developers.com/f/android-software-development.524/)
* [Android Dumps](https://dumps.tadiphone.dev/dumps)
* [PHONEDB](https://phonedb.net/)
* [PHONEDB - Processor](https://phonedb.net/index.php?m=processor&s=headlines)
* [Guides and Resources for Sony Xperia™ & AOSP](https://sx.ix5.org/info/)
* [Open Devices : Guides & Resources (Sony devices)](https://opendevices.ix5.org/resources/)
* [XDA : All guides at one place](https://forum.xda-developers.com/t/guides-all-guides-at-one-place.2073370/)

### Video Channel

* [AlaskaLinuxUser AKLU](https://www.youtube.com/c/AlaskaLinuxUserAKLU)
* [Android & Linux Development (@remainder30000)](https://www.youtube.com/@remainder30000)
* [OSP »» Android OS »» ROM »» Android Development](https://www.youtube.com/@aosp_android_tollcafe/videos)
* [Dimple S](https://www.youtube.com/@dimples_android_geek)
* [Haikal Luthfianino Balukia](https://www.youtube.com/@haikalluthfianinobalukia2423/videos)

## Tools

*Tools for helping development of Android Rom*

* [akhilnarang/scripts (Github)](https://github.com/akhilnarang/scripts) - Some script useful for ROM development.
* [ShivamKumarJha/android_tools (Github)](https://github.com/ShivamKumarJha/android_tools) - Collection of scripts to help with Android ROM stuff.
* [dumpyara](https://github.com/AndroidDumps/dumpyara) - For dumping files like vendors or blobs of an Android device.
* [dumpyara (python)](https://github.com/sebaubuntu-python/dumpyara)
* [Binder Explorer](https://github.com/opersys/binder-explorer-web)
* [Process Explorer web](https://github.com/opersys/process-explorer-web) & [Process Explorer app](https://github.com/opersys/process-explorer-app)
* [file-explorer](https://github.com/opersys/file-explorer-web) & [](https://github.com/opersys/file-explorer-app)
* [file-explorer](https://github.com/opersys/file-explorer-web) & [](https://github.com/opersys/file-explorer-app)
* [jtrace](http://newandroidbook.com/tools/jtrace.html)
* [bdsm](http://newandroidbook.com/tools/bdsm.html)
* [imjtool](http://newandroidbook.com/tools/imjtool.html)
* [memento](http://newandroidbook.com/tools/memento.html)
* [Process Explorer](http://newandroidbook.com/tools/procexp.html)
* [dextra](http://newandroidbook.com/tools/dextra.html)
* [bindump](http://newandroidbook.com/tools/bindump.html)
* [JPT](http://newandroidbook.com/tools/jpt.html)
* [anestisb/android-prepare-vendor (Github)](https://github.com/anestisb/android-prepare-vendor)
* [UnSIN ~ SIN v3/v4/v5 Unpacker](https://forum.xda-developers.com/t/tool-unsin-sin-v3-v4-v5-unpacker-v1-13.3128106/)
* [Android Image Kitchen](https://forum.xda-developers.com/t/tool-android-image-kitchen-unpack-repack-kernel-ramdisk-win-android-linux-mac.2073775/) - Unpack/Repack Kernel Ramdisk
* [Android-Blob-Utility](https://github.com/JackpotClavin/Android-Blob-Utility)
* [Alogview](https://github.com/flimberger/alogview)
* [PID Cat](https://github.com/JakeWharton/pidcat)
* [DumprX](https://github.com/DumprX/DumprX)
* [Android Build Environment Scripts](https://github.com/CyberJalagam/android_rom_building_scripts)
* [android_helpful](https://github.com/hpnightowl/android_helpful)

## Videos

* [AOSP - Android OS Internals Series (Youtube playlist)](https://www.youtube.com/playlist?app=desktop&list=PLAlSOSt8vS8Ss3uEshNXQe3cbx9qtl8m4)

## Books

* [Embedded Android: Porting, Extending, and Customizing](https://www.oreilly.com/library/view/embedded-android/9781449327958/) by Karim Yaghmour.
* [Android Internals, A Confectioner's Cookbook, Volume I (first edition)](http://newandroidbook.com/AIvI-M-RL1.pdf) - Free ebook 
* [Android Internals::Developer's View](https://www.amazon.com/Android-Internals-Developers-Jonathan-Levin/dp/0991055543) ([Author website](http://newandroidbook.com/TOC.html))
* [Android Internals::Power User's View](https://www.amazon.com/Android-Internals-Power-Users-View/dp/0991055586) ([Author website](http://newandroidbook.com/TOC.html))
* [Android Telephony Basics](https://lineageos.org/engineering/Telephony/)

## Telegram channel

*Telegram is often used by system maintainers to share informations*

## News

* [LineageOS Engineering Blog](https://lineageos.org/engineering/)

## Vendors open source

* [Fairphone](https://code.fairphone.com/)
* [LG](https://opensource.lge.com/index) and [inquiry](https://opensource.lge.com/inquiry)
* [Motorola](https://www.motorola.com/us/developer) & [Github](https://github.com/MotorolaMobilityLLC)
* [Samsung](https://opensource.samsung.com/main) and [inquiry](https://opensource.samsung.com/requestInquiry)
* [Sony](https://developer.sony.com/develop/open-source/)

## Some device project

* [Raspberry Vanilla](https://github.com/raspberry-vanilla) - AOSP for Raspberry Pi 4

## Related awesome

* [awesome-android](https://github.com/JStumpp/awesome-android#readme) - For Android application development.
* [awesome-android-ui](https://github.com/wasabeef/awesome-android-ui) - List of Android UI/UX Libraries
* [ android-security-awesome](https://github.com/ashishb/android-security-awesome) - A collection of android security related resources.

## Contributing

Contributions welcome! Read the [contribution guidelines](contributing.md) first.
