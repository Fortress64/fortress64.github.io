---
layout: page
title: Xiaomi Redmi Note 10 — Releases
subtitle: Xiaomi Redmi Note 10 (sunny/mojito)
hero_height: is-fullwidth
callouts: sunny
---
# Custom ROM and Recovery Releases

This page lists custom Android ROM and Recovery builds maintained for the Xiaomi Redmi Note 10 (codenames: `sunny` / `mojito`). All builds support Magisk for root management and are compatible with TWRP, OrangeFox, and PBRP recovery. Version numbers and download links are listed in the overview above.

> **Disclaimer:** Flashing a custom ROM or recovery carries inherent risks, including data loss, boot loops, or a bricked device. Follow all instructions carefully. By proceeding, you accept full responsibility for any issues that may arise.

## Device Specifications

![Device Specifications](/img/xiaomi/devices/Specs-Sunny.webp)

---

## Table of Contents

1. [ROM Releases](#1-rom-releases)
   - [CrDroid+](#crdroid)
   - [LineageOS+](#lineageos)
   - [e/OS *(Discontinued)*](#eos)
   - [LMODroid *(Discontinued)*](#lmodroid)
2. [Recovery Options](#2-recovery-options)

---

## 1. ROM Releases

<a name="crdroid"></a>
### 1.1 CrDroid+

![CrDroid Logo](/img/logos/CrDroid.webp)

[View XDA Thread](https://xdaforums.com/t/crdroid-v12-2-rom-unofficial-android-16-microg-ota-magisk-twrp-pbrp-orangefox-xiaomi-redmi-note-10-sunny-mojito-23-october-2025.4764091/)

CrDroid is a feature-rich custom ROM based on AOSP, focused on performance, customisation, and stability. This build extends the upstream release with privacy-focused app defaults and a configurable app selection system.

#### Key Features

- **OTA Updates:** Updates are delivered directly from our secure servers, keeping the device current without manual intervention.
- **MicroG Verified Device:** This build has fully passed Google Play Services' SafetyNet attestation via MicroG, ensuring broad app compatibility and a stable security baseline.
- **Custom Patchsets:** Tailored security and privacy patches are applied on top of the base ROM to improve both performance and user protection.
- **Configurable App Selection:** The default set of user and system apps can be customised by editing `Fortress64/fortress64-apk.config.txt`. This file persists across fresh installations for a consistent, reproducible setup. Further details are documented in the file itself.

#### Included Removable Apps

All apps listed below are pre-installed but can be removed at any time.

| App | Description |
|---|---|
| **AdAway** | System-level ad blocker using hosts file modification |
| **AFWall+** | Host-based firewall with fine-grained per-app network control |
| **Aurora Store** | Anonymous Google Play client; no Google account required |
| **DroidFS** | Encrypted virtual filesystem for secure local and cloud file storage |
| **F-Droid Basic** | Minimal F-Droid client for installing open-source Android apps |
| **Fossify File Manager** | Lightweight file manager with no analytics or cloud dependencies |
| **InviZible Pro** | Combined Tor, DNSCrypt, and I2P client for network privacy |
| **Ironfox** | Privacy-hardened web browser based on Firefox |
| **KeePassDX** | Offline password manager with encrypted local storage |
| **Magisk** | Root management framework with systemless modification support |
| **MicroG** | Open-source reimplementation of Google Play Services |
| **Neo Backup** | Open-source app and data backup utility |
| **Organic Maps** | Offline maps application built on OpenStreetMap data |
| **Signal** | End-to-end encrypted messaging and voice calls |
| **Survival Manual** | Offline survival guide based on the U.S. Army Field Manual 21-76 |
| **Termux** | Terminal emulator providing a full Linux userland environment on Android |
| **Thunderbird** | Full-featured open-source email client |
| **WireGuard** | Modern, high-performance VPN using the WireGuard protocol |

#### Screenshots

![CrDroid Screenshots](/img/xiaomi/screenshots/Xiaomi-crDroid.webp)

---

<a name="lineageos"></a>
### 1.2 LineageOS+

![LineageOS Logo](/img/logos/LineageOS.webp)

[View XDA Thread](https://xdaforums.com/t/lineageos-v23-0-rom-unofficial-android-16-microg-ota-magisk-twrp-pbrp-orangefox-xiaomi-redmi-note-10-sunny-mojito-23-october-2025.4764092/)

LineageOS is one of the most widely used custom Android distributions, known for its clean AOSP base, long-term device support, and strong community. This build extends it with the same privacy-focused app defaults and configurable app selection system as CrDroid+.

#### Key Features

- **OTA Updates:** Updates are delivered from our secure servers.
- **MicroG Verified Device:** This build has largely passed SafetyNet attestation via MicroG, providing good app compatibility with standard security guarantees.
- **Custom Patchsets:** Tailored security and privacy patches are applied on top of the base ROM.
- **Configurable App Selection:** The default set of user and system apps can be customised by editing `Fortress64/fortress64-apk.config.txt`. This file persists across fresh installations for a consistent, reproducible setup. Further details are documented in the file itself.

#### Included Removable Apps

Identical to the CrDroid+ app bundle. Refer to the [table above](#included-removable-apps) for descriptions.

#### Screenshots

![LineageOS Screenshots](/img/xiaomi/screenshots/Xiaomi-LineageOS.webp)

---

<a name="eos"></a>
### 1.3 e/OS — **DISCONTINUED**

![e/OS Logo](/img/logos/eOS.webp)

[View XDA Thread](https://xdaforums.com/t/discontinued-e-os-e-2-8-u-rom-unofficial-android-14-ota-magisk-twrp-pbrp-orangefox-xiaomi-redmi-note-10-sunny-mojito-06-feb-2025.4717275/)

> Development on this ROM has been discontinued. No further updates will be released. The XDA thread and downloads remain available for reference.

#### Key Features

- **OTA Updates:** Updates were delivered over-the-air from our secure servers.

#### Included Removable Apps

| App | Description |
|---|---|
| **AdAway** | System-level ad blocker |
| **AFWall** | Host-based firewall |
| **Aurora Store** | Anonymous Google Play client |
| **Iceraven** | Privacy-focused web browser (Firefox fork) |
| **KeePassDX** | Offline password manager |
| **Magisk** | Root management framework |
| **Signal** | End-to-end encrypted messaging |
| **Thunderbird** | Open-source email client |

#### Screenshots

![e/OS Screenshots](/img/xiaomi/screenshots/Xiaomi-e_OS.webp)

---

<a name="lmodroid"></a>
### 1.4 LMODroid — **DISCONTINUED**

![LMODroid Logo](/img/logos/LMODroid.webp)

[View XDA Thread](https://xdaforums.com/t/discontinued-lmodroid-v6-0-rom-unofficial-android-14-ota-magisk-twrp-pbrp-orangefox-xiaomi-redmi-note-10-sunny-mojito-06-feb-2025.4717140/)

> Development on this ROM has been discontinued. No further updates will be released. The XDA thread and downloads remain available for reference.

#### Key Features

- **OTA Updates:** Updates were delivered over-the-air from our secure servers.

#### Included Removable Apps

Identical to the e/OS app bundle. See the [e/OS app table above](#eos) for descriptions.

#### Screenshots

![LMODroid Screenshots](/img/xiaomi/screenshots/Xiaomi-LMODroid.webp)

---

## 2. Recovery Options

[View XDA Thread](https://xdaforums.com/t/multiple-custom-recoveries-unofficial-xiaomi-redmi-note-10-sunny-mojito-twrp-orangefox-pbrp-10-juli-2025.4721961/)

All three recoveries are available as both a bootable `.img` file and an installable `.zip` for flashing from within an existing recovery. Each release bundles the latest version of Magisk available at build time.

> Recoveries can be booted directly via Fastboot without being permanently flashed to the device.

**Magisk installation:** OrangeFox includes built-in Magisk flashing support directly from its UI. For TWRP and PBRP, navigate to `/Magisk/Magisk.zip` within the recovery interface and flash the zip from there.

<a name="twrp"></a>
### TWRP (Team Win Recovery Project)

![TWRP Logo](/img/logos/TWRP.webp)

TWRP is the most widely adopted custom recovery for Android. It provides a touch-based interface with support for ADB sideloading, full NANDroid backups, file management, and terminal access.

#### Screenshot

![TWRP Screenshots](/img/xiaomi/screenshots/Xiaomi-TWRP.webp)

<a name="orangefox"></a>
### OrangeFox (OrangeFox Recovery Project)

![OrangeFox Logo](/img/logos/OrangeFox.webp)

OrangeFox is built on top of TWRP and extends it with a polished Material Design interface, built-in OTA update support, and fully integrated Magisk manager support for streamlined root installation — no sideloading required.

#### Screenshot

![OrangeFox Screenshots](/img/xiaomi/screenshots/Xiaomi-OrangeFox.webp)

<a name="pbrp"></a>
### Pitch Black Recovery Project (PBRP)

![PBRP Logo](/img/logos/PBRP.webp)

PBRP is a dark-themed recovery with a clean, minimal UI. It supports ADB sideloading and includes integrated tools for partition management and backups.

#### Screenshot

![PBRP Screenshots](/img/xiaomi/screenshots/Xiaomi-PitchBlack.webp)
