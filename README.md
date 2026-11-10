# Dolby Atmos Sony Xperia 5 V Magisk Module

## DISCLAIMER
- Sony & Dolby apps and blobs are owned by Sony™ & Dolby™.
- The MIT license specified here is for the Magisk Module only, not for Sony & Dolby apps and blobs.

## Description
- Equalizer global type sound effect ported from Sony Xperia 5 V (pdx237) and integrated as a Magisk Module for all supported and rooted devices with Magisk
- Conflicted with `vendor.dolby_v3_6.hardware.dms360@2.0-service`, `vendor.dolby_sp.hardware.dmssp@2.0-service`, & `vendor.dolby.hardware.dms@1.0-service`
- I will not porting DSEE Ultimate nor Intelligent Wind Filter because they requires Xperia Audio Hal support which only available on Xperia ROM

## Sources
- https://dumps.tadiphone.dev/dumps/sony/pdx237 sssi-user-14-67.1.A.2.229-1-release-keys
- libswdap.so 64 bit: https://github.com/XperiaLabs/vendor_sony_extra/tree/UDC/Sagami/audio
- libswdap.so 32 bit modified by bbn
- libsqlite.so: https://dumps.tadiphone.dev/dumps/zte/p855a01 msmnile-user-11-RKQ1.201221.002-20211215.223102-release-keys
- libstagefright_foundation.so, libstagefrightdolby.so, libstagefright_soft_ddpdec.so, libstagefright_soft_ac4dec.so, libdeccfg.so, & media_codecs_dolby_audio.xml: https://dumps.tadiphone.dev/dumps/motorola/rhode user-12-S1SR32.38-124-3-a8403-release-keys
- libhidlbase.so: CrDroid ROM Android 13
- libutils.so: LineageOS 23 Android 16 BP2A.250605.031.A2 1758630651
- libmagiskpolicy.so: Magisk (debug) 31.0 (31000)

## Screenshots
https://t.me/ryukimodsscreenshots/7

## Requirements
- arm64-v8a architecture
- Android 11 (SDK 30) and up
- HIDL audio service
- Magisk or Kitsune Mask or KernelSU or Apatch installed (Recommended to use Magisk Delta/Kitsune Mask for systemless early init mount manifest.xml if your ROM is Read-Only https://t.me/ryukinotes/49)

## Download Links and Changelog

v2.2 https://move2link.co/5744d6e
- Update libmagiskpolicy.so from Magisk (debug) 31.0 (31000)
- Prepare /storage/emulated/"$UID"/Android/data/$PKG/ directories
- Add a new optional dolby.mod_xml to let users to use any modified/custom dax-default.xml. Please read Optionals below.

v2.1 https://move2link.co/1977e9c
- Fix manifest.xml detection bug in some ROMs
- Fix sepolicy denial

v2.0
- Check functions in mirror /apex files instead of mirror /system if exist
- Remove hardware services conflict restart (Use this instead: https://github.com/reiryuki/Hardware-Services-Restarter-Magisk-Module)
- Fix sepolicy denial

v1.9
- Support NoMount metamodule
- Resets module folders/files permissions at post-fs-data
- Move _uninstall.log to /data/adb/logs/
- Hides in-bulit LunarisDolby.apk
- Removes conflicted weird modules

v1.8
- Update libmagiskpolicy.so from Magisk (stable) 30.7 (30700) (fixes sepolicy denials in KernelSU)
- Does not disable raw playback (You can use Audio Compatibility Patch Reborn Magisk Module instead)

v1.7
- Fix wrong target in latest KernelSU
- Improve detections

v1.6
- Fix wrong manifest.xml location patch target in latest Magisk version

v1.5
- Tidy up aml.sh
- Exclude \*audio\*effects\*haptic\*.xml
- Fix wrong file permissions in some ROMs

v1.4
- Forgot to patch libdlbvol.so & libdlbpreg.so

v1.3
- Fix ZN7android8String16aSEOS0 function not found in some ROMs
- Add libutils.so as system_support
- Abort installation if fail to mount mirror system

## Download Tutorial
https://t.me/ryukinotes/97

## WARNING!!!
Possibility of bootloop or even softbrick or a service failure on Read-Only ROM if you don't use Magisk Delta/Kitsune Mask.

## Installation Guide
- Recommended to use Magisk Delta/Kitsune Mask https://t.me/ryukinotes/49
- Remove any other else Dolby MAGISK MODULE with different name (no need to remove if it's the same name)
- Reboot
- If you are using KernelSU, you need to disable Unmount Modules by Default in KernelSU app settings and install https://github.com/KernelSU-Modules-Repo/meta-overlayfs or https://github.com/KernelSU-Modules-Repo/magic_mount_rs or https://github.com/KernelSU-Modules-Repo/hybrid_mount or https://github.com/maxsteeel/nomount first depending on ROM compatibility
- If you have Dolby in-built in your ROM, then you need to activate data.cleanup=1 at the first time install (READ Optionals below!)
- Install this module via Magisk app or Kitsune Mask app or KernelSU app or Apatch app or Recovery if Magisk or Kitsune Mask installed
- Install AML Magisk Module https://t.me/ryukinotes/34 only if using any other else audio mod module
- Reboot
- If you are using KernelSU, you need to allow superuser list manually all package name listed in package.txt (and your home launcher app also) (enable show system apps) and reboot afterwards
- If you are using SUList, you need to allow list manually your home launcher app (enable show system apps) and reboot afterwards
- If you have vibrator, camera, charging/USB, SIM card/RIL, display, brightness, WiFi, thermal, and sensors issues (fingerprint, proximity, gyroscope, etc.), then install https://github.com/reiryuki/Hardware-Services-Restarter-Magisk-Module also

## Optionals
- https://t.me/ryukinotes/8
- Global: https://t.me/ryukinotes/35
- Stream: https://t.me/ryukinotes/52

## Troubleshootings
- https://t.me/ryukinotes/10
- https://t.me/ryukinotes/11
- Global: https://t.me/ryukinotes/34

## Known Issue
Unsupported in some SDK 30 ROM or maybe it's just unsupported in SDK 30? I don't know.

## Support and Bug Report
- https://t.me/ryukinotes/54
- If you don't do above, issues will be closed immediately

## Credits and Contributors
- @HuskyDG
- https://t.me/viperatmos
- https://t.me/androidryukimodsdiscussions
- @HELLBOY017
- @ahnet_h & bbn
- https://t.me/androidappsportdevelopment

## Sponsors and Donation
https://t.me/ryukinotes/25


