# OpenOC

Open Android distribution built for **Xiaomi Redmi Note 4X (mido)**.

Base: AOSP 15 / LineageOS 22.2 core + MiThorium device stack (unified msm8953, kernel 4.19).

## Sync

```bash
mkdir -p ~/openoc && cd ~/openoc
repo init -u https://github.com/dimasokolov110315-lang/openoc_manifest.git -b main
repo sync -c -j8
```

## Build

```bash
source build/envsetup.sh
lunch openoc_mido-userdebug
mka bacon
```

## Structure

- `default.xml` — verbatim LineageOS 22.2 base manifest (upgrade-friendly)
- `openoc.xml` — the OpenOC device layer: mido device tree (our fork), MiThorium common, kernel 4.19, Qualcomm CAF HALs
- `snippets/` — upstream snippets

OpenOC is not affiliated with Google, Xiaomi or LineageOS. Apache 2.0 where applicable.
