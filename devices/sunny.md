---
layout: page
subtitle: Xiaomi Redmi Note 10 (sunny/mojito)
hero_height: is-fullwidth
callouts: sunny
---
# Custom ROM Releases

This repository provides custom Android ROM builds for the Xiaomi Redmi Note 10 (codenames: `sunny` / `mojito`). All releases are compatible with Magisk and the following custom recoveries: TWRP, PBRP, and OrangeFox.

> **Disclaimer:** Flashing a custom ROM carries inherent risks, including data loss, boot loops, or a bricked device. Follow all instructions carefully. By proceeding, you accept full responsibility for any issues that arise from the flashing process.

![Device Specifications](/img/xiaomi/Specs-Sunny.webp)

---

## Table of Contents

1. [ROM Releases](#1-rom-releases)
   - [CrDroid+ v12.2 — Android 16](#11-crdroid-v122--android-16)
   - [LineageOS+ v23.0 — Android 16](#12-lineageos-v230--android-16)
   - [e/OS e-2.8-u — Android 14 *(Discontinued)*](#13-eos-e-28-u--android-14--discontinued)
   - [LMODroid 6.0 — Android 14 *(Discontinued)*](#14-lmodroid-60--android-14--discontinued)
2. [Recovery Options](#2-recovery-options)

---

## 1. ROM Releases

### 1.1 CrDroid+ v12.2 — Android 16

![CrDroid Logo](/img/logos/Logo_CrDroid.webp)

[View XDA Thread](https://xdaforums.com/t/crdroid-v12-2-rom-unofficial-android-16-microg-ota-magisk-twrp-pbrp-orangefox-xiaomi-redmi-note-10-sunny-mojito-23-october-2025.4764091/)

#### Key Features

- **OTA Updates:** Seamless over-the-air updates are delivered directly from our own secure servers, keeping the device current without manual intervention.
- **MicroG Verified Device:** This build has successfully passed Google Play Services' SafetyNet attestation via MicroG, ensuring broad app compatibility and a stable security baseline.
- **Custom Patchsets:** Tailored security and privacy patches are applied on top of the base ROM to improve both performance and user protection.
- **Configurable App Selection:** Users can modify `Fortress64/fortress64-apk.config.txt` to define which user and system apps are installed by default. This configuration file persists across fresh installations, enabling a reproducible and personalized setup.

#### Included Removable Apps

| App | Description |
|---|---|
| AdAway | System-level ad blocker using hosts file modification |
| AFWall+ | Host-based firewall with fine-grained per-app network control |
| Aurora Store | Anonymous Google Play client; no Google account required |
| DroidFS | Encrypted virtual filesystem for secure local and cloud file storage |
| F-Droid Basic | Minimal F-Droid client for installing open-source Android apps |
| Fossify File Manager | Lightweight file manager with no analytics or cloud dependencies |
| Ironfox | Privacy-hardened web browser |
| InviZible Pro | Combined Tor, DNSCrypt, and I2P client for network privacy |
| KeePassDX | Offline password manager with encrypted local storage |
| Magisk | Root management framework with systemless modification support |
| MicroG | Open-source reimplementation of Google Play Services |
| Neo Backup | Open-source app and data backup utility |
| Organic Maps | Offline maps application built on OpenStreetMap data |
| Signal | End-to-end encrypted messaging and voice calls |
| Survival Manual | Offline survival guide based on the U.S. Army Field Manual 21-76 |
| Termux | Terminal emulator providing a full Linux userland environment on Android |
| Thunderbird | Full-featured open-source email client |
| WireGuard | Modern, high-performance VPN using the WireGuard protocol |

![CrDroid Screenshots](/img/xiaomi/Screenshot-Xiaomi-crDroid.webp)

---

### 1.2 LineageOS+ v23.0 — Android 16

![LineageOS Logo](/img/logos/Logo_LineageOS.webp)

[View XDA Thread](https://xdaforums.com/t/lineageos-v23-0-rom-unofficial-android-16-microg-ota-magisk-twrp-pbrp-orangefox-xiaomi-redmi-note-10-sunny-mojito-23-october-2025.4764092/)

#### Key Features

- **OTA Updates:** Over-the-air updates are delivered from our own secure servers.
- **MicroG Verified Device:** This build has largely passed SafetyNet attestation via MicroG, providing good app compatibility with standard security guarantees.
- **Custom Patchsets:** Tailored security and privacy patches are applied on top of the base ROM.
- **Configurable App Selection:** Users can modify `Fortress64/fortress64-apk.config.txt` to control which apps are present after installation. The file can be reused across reinstalls for a consistent setup.

#### Included Removable Apps

Identical to the CrDroid+ app bundle. Refer to the [table above](#included-removable-apps) for descriptions.

![LineageOS Screenshots](/img/xiaomi/Screenshot-Xiaomi-LineageOS.webp)

---

### 1.3 e/OS e-2.8-u — Android 14 — **DISCONTINUED**

![e/OS Logo](/img/logos/Logo_eOS.webp)

[View XDA Thread](https://xdaforums.com/t/discontinued-e-os-e-2-8-u-rom-unofficial-android-14-ota-magisk-twrp-pbrp-orangefox-xiaomi-redmi-note-10-sunny-mojito-06-feb-2025.4717275/)

> Development on this ROM has been discontinued. No further updates will be released.

#### Key Features

- **OTA Updates:** Updates were delivered over-the-air from our own secure servers.

#### Included Removable Apps

| App | Description |
|---|---|
| Magisk | Root management framework |
| Aurora Store | Anonymous Google Play client |
| AFWall | Host-based firewall |
| AdAway | System-level ad blocker |
| Iceraven | Privacy-focused web browser (Firefox fork) |
| KeePassDX | Offline password manager |
| Signal | End-to-end encrypted messaging |
| Thunderbird | Open-source email client |

![e/OS Screenshots](/img/xiaomi/Screenshot-Xiaomi-e_OS.webp)

---

### 1.4 LMODroid 6.0 — Android 14 — **DISCONTINUED**

![LMODroid Logo](/img/logos/Logo_LMODroid.webp)

[View XDA Thread](https://xdaforums.com/t/discontinued-lmodroid-v6-0-rom-unofficial-android-14-ota-magisk-twrp-pbrp-orangefox-xiaomi-redmi-note-10-sunny-mojito-06-feb-2025.4717140/)

> Development on this ROM has been discontinued. No further updates will be released.

#### Key Features

- **OTA Updates:** Updates were delivered over-the-air from our own secure servers.

#### Included Removable Apps

Identical to e/OS. Refer to the [table above](#included-removable-apps-2) for descriptions.

![LMODroid Screenshots](/img/xiaomi/Screenshot-Xiaomi-LMODroid.webp)

---

## 2. Recovery Options

[View XDA Thread](https://xdaforums.com/t/multiple-custom-recoveries-unofficial-xiaomi-redmi-note-10-sunny-mojito-twrp-orangefox-pbrp-10-juli-2025.4721961/)

All three recoveries are available in two formats: a bootable `.img` file and an installable `.zip` for flashing from within recovery. Each release bundles Magisk v30.1. Recoveries can be booted directly via Fastboot without being permanently flashed to the device.

**Magisk installation:** OrangeFox includes full built-in Magisk manager support. For TWRP and PBRP, navigate to `/Magisk/Magisk.zip` within the recovery interface and flash the zip directly.

### TWRP 3.7.1 (Team Win Recovery Project)

A well-established recovery with broad device support, a touch-based interface, and support for ADB sideloading, full backups (NANDroid), and file system operations.

![TWRP Screenshots](/img/xiaomi/Screenshot-Xiaomi-TWRP.webp)

### OrangeFox 12.1 (OrangeFox Recovery Project)

A feature-rich recovery built on TWRP, with a polished Material Design interface and fully integrated Magisk manager support for streamlined root installation.

![OrangeFox Screenshots](/img/xiaomi/Screenshot-Xiaomi-OrangeFox.webp)

### PBRP 4.0 (Pitch Black Recovery Project)

A dark-themed recovery with a clean UI, support for ADB sideloading, and integrated tools for partition management and backups.

![PBRP Screenshots](/img/xiaomi/Screenshot-Xiaomi-PitchBlack.webp)
