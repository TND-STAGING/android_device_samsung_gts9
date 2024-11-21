# Android device tree for samsung SM-X816B (gts9p)

# How-to compile it:

 - twrp-14 manifest
```
    repo init --depth=1 -u https://github.com/MrFluffyOven/platform_manifest_twrp_aosp.git -b twrp-14
```
 - Sync
```
    repo sync
```
 - Clone TheNoobDevs-Staging twrp tree
```
    git clone https://github.com/TND-STAGING/android_device_samsung_gts9p.git -b twrp-14 device/samsung/gts9p
```
 - Prepare
```
    export ALLOW_MISSING_DEPENDENCIES=true; . build/envsetup.sh; lunch twrp_gts9p-eng
```
 - Repopick Patches
```
    repopick -Q "branch:android-14+status:open+-change:7371+-change:7543+-change:7553+-change:7671+-change:7717+-change:7718"
```
 - Run the Build Command
```
    mka recoveryimage
```
## Multidisabler
once in twrp go to advanced, terminal and type "multidisabler" to stop restoration of stock recovery
