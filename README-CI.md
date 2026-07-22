# LineageOS 23.2 for Xiaomi mars

This manifest tracks LineageOS 23.2 and includes the Moment, status bar lyric,
custom About phone, and Xiaomi mars changes maintained by LineageOS-Sado.

## Sync

```bash
repo init -u https://github.com/LineageOS-Sado/android-lineage-23.2.git \
    -b lineage-23.2 --git-lfs
repo sync -c --force-sync --no-clone-bundle --no-tags -j"$(nproc)"
```

## Build

```bash
source build/envsetup.sh
lunch lineage_mars-bp4a-userdebug
mka bacon
```

CI runners need enough disk space for Android 16 sources and build output, Git
LFS support, Java and the standard LineageOS build dependencies. Proprietary
Xiaomi repositories are fetched from TheMuppets.
