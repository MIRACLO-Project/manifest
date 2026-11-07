<div align="center">

# MIRACLO

**A premium Android 17 ROM for the POCO F5 (marble), built from Qualcomm's CLO source.**

`1.0 Aurora` · Android 17 · CLO `LA.QSSI.17.0` · Security patch `2026-08-05`

**First release · under active development**

<!-- SCREENSHOTS: home screen · Quick Settings (ColorOS / iOS / One UI) · Mira Studio · lock screen · Mira Dolby -->

</div>

---

> [!IMPORTANT]
> **1.0 Aurora is MIRACLO's first build.** Everything is still under active development: expect bugs and missing features, and read [Known issues and missing features](#known-issues-and-missing-features) before installing. Keep a backup of your data.

## Overview

MIRACLO pairs a pure CLO system with its own design language, **Mira**. Every MIRACLO feature lives in one place, **Mira Studio**, opened from the card at the top of Settings, and every addition can be turned on or off.

- Designed for both dark and light themes, on every screen.
- Previews show your real lock screen, home screen, tiles and icons, never placeholder images.
- Two variants: **GApps** (Google's own apps) and **Vanilla** (open-source apps, no Google apps).

## At a glance

| | |
| --- | --- |
| Device | POCO F5 / Redmi Note 12 Turbo (`marble`) |
| Base | Qualcomm CLO, `LA.QSSI.17.0` |
| Android | 17, security patch `2026-08-05` |
| Kernel | **aurora**: Google's official `android12-5.10-lts` (5.10.272), built by MIRACLO |
| Firmware | Xiaomi HyperOS `OS3.0.4.0.VMRMIXM`, included in the package |
| Vendor | Xiaomi's stock vendor, odm and vendor_dlkm |
| Signing | MIRACLO's own release keys and verified-boot key |
| Variants | GApps and Vanilla, fastboot and recovery packages with SHA-256 checksums |
| Updates | New builds as fastboot or recovery packages; OTA through Mira Updater starts with a later release |
| Root | Optional zips: KernelSU-Next, KernelSU and SukiSU-Ultra, from their official releases |

## Mira Studio

One home for customisation, with live previews, an inline search over every option, a reset icon on every slider and a **Reset to default** button on every page.

| Page | What you can change |
| --- | --- |
| Status bar | Wi-Fi and signal icon style (ColorOS, iOS, One UI or Android), merged SIMs, no-data mark, network type label, 4G+, VoLTE and Wi-Fi calling icons, clock seconds, visible icons, edge spacing, height |
| Network speed | Live speed, hide when idle, position, style, arrows, size, units |
| Quick Settings | Four styles (Stock, ColorOS, iOS, One UI), round tiles, tile size, edit controls |
| Notification shade | Split pull: notifications on one side, Quick Settings on the other, sides swappable |
| Liquid Glass | Glass with refraction and touch glow, and where it applies (Quick Settings, notifications, island, volume panel, power menu) |
| Dynamic Island | On or off, pill length and height, each activity type, pop-up notifications |
| Volume panel | Mira volume panel or Android's, left or right edge |
| Lock screen | Eight clock faces with weight, size, layout, alignment and font |
| Home screen and icons | Icon packs, shape, size, themed icons, grid, labels, dots, folder blur, page transitions, gestures, hidden apps, layout lock, home search, recents style |
| Wallpaper | MIRACLO wallpapers with blur, dim and vignette |
| Colours and style | Wallpaper colours or any colour, palette style, dark theme, contrast |
| Fonts | Mira Sans (Inter) or other fonts, text size, bold text |
| Animations | Motion style and speed, wavy progress bar |
| Display | Refresh rate (Adaptive, 60, 90, 120 Hz or always highest), refresh-rate counter, colour profile |
| Battery | Battery saver, charging animation |
| Sounds and haptics | Mira sounds, touch, lock and charging sounds, vibration strength |
| App privacy | Privacy dashboard, clipboard alerts, lock-screen notification text, password visibility |
| Software update | Check, download and install MIRACLO updates |

## Quick Settings and notification shade

- **Four styles:** Stock (round tiles), ColorOS, iOS-style Control Center and One UI, every control editable.
- **ColorOS style:** the music card that grows into a full player, tall sliders, the ringer control and paged tiles.
- **Editing:** ColorOS 17-style add sheet (Recommended first, then all tiles) for ColorOS and One UI; in-place editing for iOS.
- **Split shade:** pull from the left for notifications, from the right for Quick Settings (Android 17 Dual Shade).
- **Liquid Glass:** frosted glass with real refraction and an optional soft touch glow.
- **Landscape:** every style on one screen, controls on the left and tiles on the right, notifications in a centred column.
- **Accessibility:** every round control is named and works with TalkBack.

## Status bar, Dynamic Island and lock screen

- Signal and Wi-Fi icons in ColorOS, iOS or One UI style, or Android's.
- Stacked network speed indicator.
- **Dynamic Island** (never on the lock screen or in full-screen apps): media, calls, timers and stopwatch, screen recording, live updates (navigation, rides, deliveries), downloads, charging, earbuds battery, ringer mode and low battery; message pop-ups with Reply and Mark as read; up to three activities at once.
- **Lock screen:** eight Mira clock faces, outline clocks on the always-on display, and a charging ring with level, fast-charging label and time to full.

## Launcher

- Icon packs (ADW, Nova and Lawnchair formats) with separate packs for the home screen and the app drawer, plus Mira system icons and themed icons.
- Icon shape and size, labels, notification dots, folders that blur the wallpaper.
- Grid size, layout lock, hidden apps, page transitions (slide, cube, depth, fade).
- Gestures: double-tap to lock, swipe down, swipe up and pinch, each with its own action.
- Home search: a pill the page dots turn into, or a search bar below the dock, with your choice of search app.
- Recents: default or ColorOS stacked style, with a close-all button.

## System UI

- **Mira volume panel:** a compact edge panel with Liquid Glass.
- **Power menu:** Android's own menu in this build; the Mira power menu returns once it opens as fast as Android's.

## Mira apps

- **Mira Dolby:** the phone's Dolby Atmos engine with profiles (Dynamic, Movie, Music, Game, Voice, Custom), intelligent equalizer, 10-band graphic equalizer, surround virtualiser, stereo width, dialogue enhancer, volume leveller, bass and treble; separate speaker and headphone settings, per-app profiles, saved presets and a Quick Settings tile. Includes the EasyEffects presets by JackHack96.
- **Mira Updater:** background A/B updates with pause and resume, Wi-Fi only and What's new (OTA delivery starts with a later release).
- **Mira Setup:** MIRACLO's own first screens before Google's or Android's setup.
- **Identity:** Mira Sans (Inter), Mira sounds, MIRACLO wallpapers (Planetary is the default) and the MIRACLO boot animation.

## Apps

| Role | GApps | Vanilla |
| --- | --- | --- |
| Phone | Google Phone | Fossify Phone |
| Messages | Google Messages | Fossify Messages |
| Contacts | Google Contacts | Fossify Contacts |
| Calendar | Google Calendar | Fossify Calendar |
| Clock | Google Clock | Fossify Clock |
| Calculator | Google Calculator | Fossify Calculator |
| Files | Files by Google | Fossify File Manager |
| Gallery | Google Photos | Aves |
| Music | YouTube | Gramophone |
| Keyboard | Gboard | HeliBoard |
| Browser | Chrome | Cromite |
| Camera | Xiaomi camera | Xiaomi camera |
| Sound | Mira Dolby | Mira Dolby |

GApps also includes Google's core: Play services, Play Store, the Google app, setup and restore, sync, speech services, TalkBack, Digital Wellbeing, Android Auto and Family Link. Vanilla apps come from each developer's official release, checked against the developer's signing key.

## Performance

- **aurora kernel:** Google's official `android12-5.10-lts`, built with Google's GKI configuration and ThinLTO. All 421 stock Xiaomi drivers are checked against it before every release (24,041 symbol checks). A display fix keeps the panel and the screen-sampling output working together without frame drops.
- **Qualcomm boosts:** touch, scroll, app launch and animation boosts through Qualcomm's performance service.
- **Scheduler:** the foreground app gets a minimum CPU boost and is latency-sensitive; background work is capped.
- **Memory:** zram tuned for phones, PSI-driven low-memory killer, Dalvik heap sized for 8 and 12 GB.
- **Storage:** UFS queue tuned (no I/O stats, no entropy, completions on the requesting CPU).
- **Graphics:** CPU performance hints for SurfaceFlinger and the UI renderer, frame pacing for 120 Hz.
- **Compiling:** System UI, launcher and Settings compiled ahead of time; apps verified on first boot and compiled in the background.

## Installing

MIRACLO installs from a computer with the phone in **fastboot mode** (Power + Volume down), bootloader unlocked.

1. Extract the zip and open a terminal in the extracted folder.
2. Run `bash flash_all.sh` (Linux and macOS) or `flash_all.bat` (Windows).
3. Answer `y` to wipe data on the first install. Later installs can keep data.

`flash_keep_firmware.sh` does the same but keeps the firmware already on the phone. Every file in the package is listed in `SHA256SUMS`.

**Recovery package:** flash the `-recovery.zip` from OrangeFox (Install). It goes to the inactive slot; reboot to system afterwards. Updates over an existing MIRACLO install keep your data.

## Building

```bash
repo init -u https://github.com/MIRACLO-Project/manifest -b aurora --git-lfs
repo sync -c -j16 --force-sync --no-clone-bundle --no-tags
```

Then follow `vendor/miraclo/README.md`: apply the build patches in `vendor/miraclo/patches`, fetch the stock firmware for marble, and run `vendor/miraclo/tools/build-release.sh` (`VARIANT=vanilla` for Vanilla). The aurora kernel builds from Google's official source with `vendor/miraclo/kernel/aurora-lts.sh`.

Release builds are signed with MIRACLO's private keys, which are never stored in any repository; your builds should use your own.

### Bring MIRACLO to your device

Maintainers can build MIRACLO for any Snapdragon device with a working Android 17 tree: add your trees in a local manifest, copy the product file example, and build with `DEVICE=<device>`. The full guide, including the rules for official builds, is in [DEVICES.md](DEVICES.md).

## Known issues and missing features

1.0 Aurora is the first MIRACLO build. It is under active development, and these are known:

**Not in this build yet**
- **Face unlock:** coming in a later update as Mira Face.
- **OTA updates:** Mira Updater is included, but updates are delivered as fastboot packages for now.

**Known issues**
- Apps that require a locked bootloader (some banking and payment apps) may refuse to run.
- Some MIRACLO options and visual effects may still have rough edges on certain screens.
- Battery life and performance tuning for the aurora kernel continues in the next builds.

Found something else? Report it with the steps to reproduce it and, if you can, a log (`adb logcat`). Fixes ship in the next build.

## Changelog

See [CHANGELOG.md](CHANGELOG.md).
