<picture>
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/MIRACLO-Project/MIRACLO/main/assets/header_light.png">
  <img alt="MIRACLO: Pure Android 17. Expressive where it counts." src="https://raw.githubusercontent.com/MIRACLO-Project/MIRACLO/main/assets/header_dark.png">
</picture>

# MIRACLO: build setup

How to build **MIRACLO 1.0 Aurora** (Android 17) from scratch. Branch: `aurora`.

MIRACLO is Qualcomm's Android source (CLO) plus five MIRACLO repositories. `miraclo.xml` swaps in
MIRACLO's versions of frameworks/base, Settings and Launcher3 and adds the device and vendor trees.
The three Mira Studio repositories are private: ask for access first
([MIRACLO](https://github.com/MIRACLO-Project/MIRACLO)).

## What you need

- Linux (Ubuntu 22.04 or newer), 64 GB RAM or more, about 500 GB free disk.
- `repo`, `git`, Python 3, and the usual Android build packages.
- GitHub access to the private MIRACLO repositories (a token works as the git password).

## 1. Get the source

```
mkdir -p ~/aurora && cd ~/aurora
repo init -u https://github.com/MIRACLO-Project/manifest -b aurora -m default.xml --depth=1
mkdir -p .repo/local_manifests
curl -o .repo/local_manifests/miraclo.xml https://raw.githubusercontent.com/MIRACLO-Project/manifest/aurora/miraclo.xml
repo sync -c -j8 --no-tags --no-clone-bundle
```

`server_local_manifests/` holds the extra local manifests the reference build machine had (for
reference; check them against `miraclo.xml` before adding any).

## 2. MIRACLO's changes to other Android repos

```
vendor/miraclo/patches/apply.sh
```

This applies `build_soong.patch` (lets the camera's MIUI stand-in classes into the framework, plus
build fixes) and any other patches listed in `vendor/miraclo/patches/OTHER_REPOS.txt`.

## 3. Your signing keys

Builds are signed with your own keys in `vendor/miraclo-keys/` (never put keys in git). Make them
once with Android's `development/tools/make_key` for `releasekey`, `platform`, `shared`, `media`,
`networkstack`, `sdk_sandbox` and `bluetooth`, and keep a backup: a phone can only take updates
signed with the same keys it was installed with.

## 4. Stock firmware and Google apps

```
source build/envsetup.sh
lunch miraclo_marble-cp2a-userdebug
m ota_extractor fsck.erofs aapt2 simg2img
device/xiaomi/marble/fetch-stock.sh                 # Xiaomi's vendor images and firmware (not in git)
vendor/miraclo/gapps/extract-gapps.sh <Pixel 7 Android 17 factory image>   # skip with WITH_GMS=false
```

## 5. Build

```
m                                   # images: out/target/product/marble/
m target-files-package              # target files
ota_from_target_files -k vendor/miraclo-keys/releasekey \
  out/target/product/marble/obj/PACKAGING/target_files_intermediates/miraclo_marble-target_files.zip \
  out/target/product/marble/MIRACLO-ota.zip
```

`vendor/miraclo/tools/` has the full release flow: `build-release.sh` (stock firmware, Google
apps, build, preflight checks, release package with flash scripts) and `ota-step.sh` (the update
zip). Android 17 has no `otapackage` target; `ota-step.sh` makes the zip from the target files.

## 6. Install

- **First install** (from HyperOS or another ROM): the release package's `flash_all.sh` in
  fastboot, answering **y** to wipe data.
- **Update** (MIRACLO to MIRACLO, same keys): recovery › Apply update from ADB, then
  `adb sideload MIRACLO-ota.zip`. Data stays.

## Things that will bite you

| Symptom | Cause and fix |
|---|---|
| `ninja: unknown target 'otapackage'` | Android 17 builds without it. Use `ota-step.sh` or the commands in step 5. |
| `check boot jar packages ... miui.hardware.display` | Run `vendor/miraclo/patches/apply.sh` (adds the `miui.*` packages to the boot jar allow list). |
| Bootloop, `privileged permissions not in privileged permission allowlist` | A system app asked for a new privileged permission. Add it to that app's file in `frameworks/base/data/etc/` (System UI: `com.android.systemui.xml`). |
| New Settings or launcher features missing on the phone | An older copy installed with `adb install` hides the system one: `adb shell pm uninstall-system-updates com.android.settings` (or `com.android.launcher3`). |
| `m: command not found` in a script | Run it after `source build/envsetup.sh` and `lunch`. |
| Recovery refuses an update | The phone was installed with other keys. Updates need the same keys; otherwise flash with fastboot and wipe. |
