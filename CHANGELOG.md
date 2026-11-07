# Changelog

## Next build (in testing)

- Builds are tagged release-keys.
- Launcher: icon packs and recents style moved to Mira Studio › Home screen & icons; the launcher's Home settings gets **Advanced settings**, which opens that page.
- The stock media player leaves the collapsed shade and the lock screen; the Quick Settings music cards stay.
- Maintainer support: build for other devices with `DEVICE=<device>` (see [DEVICES.md](DEVICES.md)).

## 1.0 Aurora (recovery update, 6 Nov)

- Recovery package (payload OTA zip) that installs from OrangeFox.
- Mira Dolby: None preset, Sound and Tuning pages, aligned labels.
- Power menu: Android's own menu for now.
- Display flicker with the aurora kernel fixed.
- Setup no longer loops back to the first page.

## 1.0 Aurora

Now based on Qualcomm CLO `LA.QSSI.17.0` (Android 17).

First MIRACLO build, under active development. See [Known issues and missing features](README.md#known-issues-and-missing-features).

**System**
- aurora kernel: Google's official android12-5.10-lts (5.10.272), with a display fix for the screen-sampling output.
- Xiaomi HyperOS `OS3.0.4.0.VMRMIXM` firmware included; stock vendor, odm and vendor_dlkm.
- Fastboot packages that flash from the bootloader's fastboot mode with one script (`flash_all`).
- GApps: Google's own apps only. Vanilla: maintained open-source apps.
- Xiaomi camera in both variants.

**Mira Studio**
- One home for every MIRACLO option, with live previews, search and reset to default everywhere.

**Quick Settings and shade**
- Four styles: Stock, ColorOS, iOS and One UI. Split shade, Liquid Glass with refraction, landscape layouts.

**Status bar and lock screen**
- Signal icon styles, network speed, Dynamic Island, eight clock faces, charging ring.

**Launcher**
- Icon packs, themed icons, home search, gestures, page transitions, ColorOS-style recents.

**Mira apps**
- Mira Dolby, Mira Updater, Mira Setup, Mira Sans, Mira sounds, MIRACLO wallpapers and boot animation.

**Performance**
- Qualcomm boosts, scheduler, memory, storage, graphics and compiling tuned for marble.
