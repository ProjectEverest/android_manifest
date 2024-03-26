# This is ProjectEverest [EverestOS]

# Build guide

Prior to building, you will need basic knowledge of [Git](https://www.atlassian.com/git/tutorials/atlassian-git-cheatsheet).

### Requirements
- Around 100G disk space.
- A computer with at least 16GB RAM running Linux (recommended) or MacOS.
- Build environment [setup](https://github.com/akhilnarang/scripts).

# Getting Started

### Initialize local repository

```
repo init -u https://github.com/ProjectEverest/android_manifest -b udc
```

### Sync up 

```
repo sync -c --force-sync --optimized-fetch --no-tags --no-clone-bundle --prune -j$(nproc --all)
```

# Inherit the vendor
```
$(call inherit-product, vendor/everest/config/common_full_phone.mk)
```
# Build Flags
```
# Maintainer name for Everest
EVEREST_MAINTAINER := "XYZ"

# Adding Blur support
TARGET_SUPPORTS_BLUR := true

# For UDFPS devices
EVEREST_UDFPS_ANIMATIONS := true

# Build ViMusic or InnerTune
TARGET_BUILD_VIMUSIC := true 
TARGET_BUILD_INNERTUNE := true

# Build lawnchair
TARGET_USES_LAWNCHAIR := true
```

# Build

```
source build/envsetup.sh
lunch everest_<devicecodename>-user
make bacon -j$(nproc --all)
```

### Compilation Help
To get help with build errors, please visit [**Android Building Help**](https://t.me/AndroidBuildingHelp).

## Credits

 * [**LineageOS**](https://github.com/LineageOS)
 * [**CodeAurora Forum**](https://source.codeaurora.org/quic/la)
 * [**ArrowOS**](https://github.com/ArrowOS)
 * [**SuperiorOS**](https://github.com/superioros)
 * [**Project Awaken**](https://github.com/Project-Awaken)
 * [**ProtonAOSP**](https://github.com/ProtonAOSP)
 * [**PixelExperience**](https://github.com/PixelExperience)
 * [**Syberia Project**](https://github.com/syberia-project)
 * [**Yet another AOSP project**](https://github.com/Yaap)
 * [**Pixel OS**](https://github.com/pixelos-aosp)
 * [**ProjectBlaze**](https://github.com/ProjectBlaze)
