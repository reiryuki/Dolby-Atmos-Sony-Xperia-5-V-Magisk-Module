# Dolby Atmos Sony Xperia 5 V Magisk Module

## DISCLAIMER
- Sony & Dolby apps and blobs are owned by Sony™ & Dolby™.
- The MIT license specified here is for the Magisk Module only, not for Sony & Dolby apps and blobs.

## Descriptions
- Equalizer sound effect ported from Sony Xperia 5 V (pdx237) and integrated as a Magisk Module for all supported and rooted devices with Magisk
- Global type sound effect
- Conflicted with `vendor.dolby_v3_6.hardware.dms360@2.0-service`, `vendor.dolby_sp.hardware.dmssp@2.0-service`, & `vendor.dolby.hardware.dms@1.0-service`
- I will not porting DSEE Ultimate and Intelligent Wind Filter because they requires Xperia Audio Hal support which only available on Xperia ROM

## Sources
- https://dumps.tadiphone.dev/dumps/sony/pdx237 sssi-user-14-67.1.A.2.229-1-release-keys
- /lib64/soundfx/libswdap.so: https://github.com/XperiaLabs/vendor_sony_extra/tree/UDC/Sagami/audio
- /lib/soundfx/libswdap.so modified by bbn
- libstagefright_foundation.so, libstagefrightdolby.so, libstagefright_soft_ddpdec.so, libstagefright_soft_ac4dec.so, libdeccfg.so, & media_codecs_dolby_audio.xml: https://dumps.tadiphone.dev/dumps/motorola/rhode user-12-S1SR32.38-124-3-a8403-release-keys
- libhidlbase.so: CrDroid ROM Android 13
- libmagiskpolicy.so: Kitsune Mask R6687BB53

## Screenshots
- https://t.me/ryukimodsscreenshots/7

## Requirements
- arm64-v8a architecture
- Android 11 (SDK 30) and up
- Magisk or KernelSU installed (Recommended to use Magisk Delta/Kitsune Mask for systemless early init mount manifest.xml if your ROM is Read-Only https://t.me/androidryukimodsdiscussions/100091)

## WARNING!!!
- Possibility of bootloop or even softbrick or a service failure on Read-Only ROM if you don't use Magisk Delta/Kitsune Mask.

## Installation Guide & Download Link
- Recommended to use Magisk Delta/Kitsune Mask https://t.me/androidryukimodsdiscussions/100091
- Remove any other else Dolby MAGISK MODULE with different name (no need to remove if it's the same name)
- Reboot
- If you have Dolby in-built in your ROM, then you need to activate data.cleanup=1 at the first time install (READ Optionals bellow!)
- Install this module https://www.pling.com/p/2219723/ via Magisk app or KernelSU app or Recovery if Magisk installed
- Install AML Magisk Module https://t.me/ryukinotes/34 only if using any other else audio mod module
- If you are using KernelSU, you need to disable Unmount Modules by Default in KernelSU app settings
- Reboot
- If you are using KernelSU, you need to allow superuser list manually all package name listed in package.txt (and your home launcher app also) (enable show system apps) and reboot afterwards
- If you are using SUList, you need to allow list manually your home launcher app (enable show system apps) and reboot afterwards
- If you have sensors issue (fingerprint, proximity, gyroscope, etc), then READ Optionals bellow!

## Optionals
- https://t.me/ryukinotes/8
- Global: https://t.me/ryukinotes/35
- Stream: https://t.me/androidryukimodsdiscussions/26764

## Troubleshootings
- https://t.me/ryukinotes/10
- https://t.me/ryukinotes/11
- Global: https://t.me/ryukinotes/34

## Support & Bug Report
- https://t.me/androidryukimodsdiscussions/2618
- If you don't do above, issues will be closed immediately

## Credits and Contributors
- @HuskyDG
- https://t.me/viperatmos
- https://t.me/androidryukimodsdiscussions
- @HELLBOY017
- @ahnet_h & bbn
- You can contribute ideas about this Magisk Module here: https://t.me/androidappsportdevelopment

## Sponsors
- https://t.me/ryukinotes/25


