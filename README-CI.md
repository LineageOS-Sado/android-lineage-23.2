# LineageOS 23.2 for Xiaomi mars, fuxi and ishtar

This manifest tracks LineageOS 23.2 and includes the Moment, status bar lyric,
custom About phone, Extra face authentication, and Xiaomi device changes
maintained by LineageOS-Sado.

## Sync

```bash
repo init -u https://github.com/LineageOS-Sado/android-lineage-23.2.git \
    -b lineage-23.2 --git-lfs
repo sync -c --force-sync --no-clone-bundle --no-tags -j"$(nproc)"
```

## Build

```bash
source build/envsetup.sh
lunch lineage_fuxi-bp4a-userdebug
mka bacon
```

Replace `fuxi` with `ishtar` or `mars` to build another supported device.

CI runners need enough disk space for Android 16 sources and build output, Git
LFS support, Java and the standard LineageOS build dependencies. `--git-lfs`
is required because the MiuiCamera and proprietary repositories contain LFS
objects. Device proprietary repositories are fetched from TheMuppets and
LineageOS-Sado.
