# OrangeFox Recovery device tree for Samsung S8 aka dreamlte.

## Kernel source 
Available at https://github.com/corsicanu/android_kernel_samsung_universal8895

## How to build
This was tested and it's fully compatible with [minimal manifest twrp](https://github.com/minimal-manifest-twrp/platform_manifest_twrp_omni).
1. Set up the build environment following instructions from [here](https://wiki.orangefox.tech/en/dev/building)
2. In the root folder of cloned repo you need to clone the device tree:
```bash
git clone https://github.com/ksant0s/android_device_samsung_dreamlte.git -b fox-9.0_R11.1 device/samsung/dreamlte
```
3. To build:
```bash
. build/envsetup.sh && export ALLOW_MISSING_DEPENDENCIES=true && export FOX_USE_TWRP_RECOVERY_IMAGE_BUILDER=1 && export LC_ALL="C" && lunch omni_dreamlte-eng && mka recoveryimage -j128
```

