---
subtitle: Xiaomi Redmi Note 10 (sunny/mojito)
title: CrDroid+ — Download
---

![CrDroid Logo](/img/logos/CrDroid.webp)

> **Important:** Please read the installation guide first — it contains crucial information.
> [Xiaomi Firmware, ROM and Recovery Installation Guide](/manuals/xiaomi-installation/)

---

## Release Information

| | |
|---|---|
| **Device** | Xiaomi Redmi Note 10 (sunny / mojito) |
| **ROM** | CrDroid+ |
| **Release date** | October 23, 2025 |

---

## Changelog

*Refer to the [GitHub release page](https://github.com/PTX64/releases_sunny_crdroid/releases/tag/latest) for the full changelog.*

---

## Downloads

All files are required for a fresh installation. For OTA updates, use the built-in Updater app.

| File | Description | Download |
|---|---|---|
| `crDroidAndroid-16.0-20251019-sunny-v12.2.zip` | ROM package | [Download](https://github.com/PTX64/releases_sunny_crdroid/releases/download/latest/crDroidAndroid-16.0-20251019-sunny-v12.2.zip) |
| `boot.img` | Boot image (required for first install) | [Download](https://github.com/PTX64/releases_sunny_crdroid/releases/download/latest/boot.img) |
| `vendor_boot.img` | Vendor boot image (required for first install) | [Download](https://github.com/PTX64/releases_sunny_crdroid/releases/download/latest/vendor_boot.img) |

---

## SHA256 Checksums

Verify your download against the checksums listed on the GitHub release page.

```bash
# Linux
sha256sum filename

# Windows (PowerShell)
Get-FileHash filename -Algorithm SHA256
```

[View checksums on GitHub](https://github.com/PTX64/releases_sunny_crdroid/releases/tag/latest)

---

## Recovery Options

A custom recovery is required for flashing. The following recoveries are supported for this device:

- [TWRP](/devices/sunny/twrp/) — Touch-based recovery with ADB sideloading and NANDroid backup support
- [OrangeFox](/devices/sunny/orangefox/) — TWRP-based recovery with built-in Magisk manager support
- [Pitch Black Recovery Project (PBRP)](/devices/sunny/pbrp/) — Dark-themed recovery with clean UI

---

## Troubleshooting

Having boot issues after flashing? See the [Troubleshooting guide](/manuals/troubleshoot/#bootissues).

---

[← Back to device page](/devices/sunny/)
