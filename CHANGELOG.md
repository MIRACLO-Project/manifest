# Changelog

## 1.1 Aurora (in testing)

**Design**
- Mira design language across the system: continuous corners (cards 28, wells 22), capsule buttons and sliders, Mira Sans with the iOS type scale, iOS system colours, 60 × 28 switches, sliders with a reset button.
- Liquid Glass everywhere it is turned on: Clear or Tinted glass with eight tints, blur strength, smoother glass, and a milky light-theme glass with readable text. Quick Settings, notifications, the Dynamic Island and the volume panel follow the same look.
- Text in Quick Settings and the shade stays readable over any wallpaper.

**Mira Studio**
- New pages: Notifications (card style, spacing, transparency, blur, lock screen Count/Stack/List, group by app, app icon in toasts), Network access, Dual apps, App lock, Bug report, Screenshots & recording, Gestures, Performance, Floating windows, Software update, Call recording.
- Lock screen: widgets, left and right shortcuts, Always-on display (Always, Scheduled, Tap to show) and Edge lighting (Glow, Pulse, Rainbow, Corners).
- Display: Extra dim and per-app refresh rate.
- Quick Settings: columns, rows, labels, brightness and media visibility, colours, transparency and blur.

**Apps**
- Mira Setup: Hello, Make it yours (Light or Dark with the matching Aurora wallpaper), Controls (navigation and Quick Settings style), Liquid Glass.
- Mira Updater: new design, daily background check, automatic download, Wi-Fi only, restart overnight to install.
- Mira Dolby and Mira GameSpace redesigned.
- Call recording from a notification during calls.

**Under the hood**
- CLO `LA.QSSI.17.0.r1-12500-qssi.0`, security patch 2026-11-05.
- Vulkan rendering for apps and SurfaceFlinger; 120 Hz tuning; apps compiled with their profiles at install.

**Not in 1.1**
- 6.x kernel and face unlock (next update). 4K video in the camera and charging limits wait for device checks.

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
