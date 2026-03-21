---
title: Vendor Restrictions & Bootloader Research
---

This page documents bootloader unlock restrictions imposed by major Android manufacturers. Information is sourced from the community-maintained [bootloader-unlock-wall-of-shame](https://github.com/zenfyrdev/bootloader-unlock-wall-of-shame) project and supplemented with independent community research.

---

- [Samsung](#samsung)
- [Xiaomi / Redmi / POCO](#xiaomi--redmi--poco)

---

## Samsung

**Verdict: 🍅 Terrible!**

> **⚠️ One UI 8 Warning:** Once you update to One UI 8, bootloader unlocking is gone **forever** — and any previously unlocked bootloader will be **automatically re-locked** when you flash One UI 8 firmware through ODIN. There is no way back unless the rollback protection bit is unchanged between One UI 7 and One UI 8. **If you are still on One UI 7 or earlier, do not update.**

### Current Status

Until recently, international Samsung devices (sold in Europe or Asia) could be unlocked. Starting with **One UI 8**, Samsung has completely removed the ability to unlock the bootloader — regardless of model or region. Exynos devices on One UI 7 or earlier can still be unlocked. North American devices on older firmware may be unlockable via a [paid third-party service](https://xdaforums.com/t/android-unsamlock-bootloader-unlock-for-samsung-us-canada-devices.4215101/) at your own risk.

Snapdragon phones prior to the S7/Note7 (2016) can be unlocked regardless of region, provided they are not carrier-locked (e.g. AT&T or Verizon). The Canadian S7 is also unlockable as it ships with an Exynos SoC.

The **Galaxy XR** (Samsung's AR headset) is a notable exception: it [does retain](https://www.ithome.com/0/892/132.htm) an unlockable bootloader despite the broader One UI 8 lockdown.

### Knox Trip — Permanent Consequences

Unlocking a Samsung device **permanently trips Knox**. Once tripped, the following features are broken and cannot be restored:

- Samsung Pay, Samsung Pass, Samsung Flow
- Samsung Health, Secure Folder, Secure Wi-Fi, Smart View

Tripping Knox may also serve as grounds for voiding your voluntary warranty. Under EU law, your statutory two-year warranty cannot be voided without the manufacturer proving the modification caused the specific defect claimed.

### 🔴 MTK Hard Brick Warning — One UI 8

> **🚨 HARD BRICK WARNING**
>
> If your device uses a **MediaTek (MTK) SoC** and your bootloader is **already unlocked**, flashing One UI 8 firmware while the bootloader remains unlocked carries a **~99% chance of permanent hard brick** with no signs of life.
>
> Non-MTK devices are not guaranteed safe either. The recommended procedure before upgrading is:
> 1. Re-flash One UI 7 firmware
> 2. Lock the bootloader
> 3. Verify "CURRENT BINARY:" shows **Official** in Download mode
> 4. Only then flash One UI 8
>
> **Do not selectively flash BL, AP, CP, and CSC files — flash all partitions in a single operation.**
>
> As of December 2025, there is no fix for this issue.

### 🔶 Helio G99 — Modem Crash Every 6 Hours

Devices with the **Helio G99** SoC (e.g. Galaxy A15 4G, A16 4G) develop a recurring modem failure after bootloader unlock and Knox trip:

- The modem crashes every **6 hours**, disabling SIM cards and temporarily showing a NULL IMEI.
- Once crashed, the modem cannot recover without a full device restart.
- This issue **persists even after re-locking the bootloader**.

**Root cause:** A check in `/vendor/lib64/libsec-ril.so` via a function called `DoOemSetwarrantyBit` reads the `ro.vendor.boot.warranty_bit` property. A partial workaround exists via a Magisk module that restarts the `ril-daemon` before the 6-hour crash window — but this is not a fix.

### 🔶 Dimensity 6100+ / 6300 — Permanent 5G Loss

Devices with **Dimensity 6100+** or **Dimensity 6300** (e.g. Galaxy A06 5G, A15 5G, A16 5G, M15 5G) suffer permanent connectivity damage after bootloader unlock:

- **5G connectivity is permanently lost** — unfixable even after re-locking the bootloader.
- The modem crashes when attempting to connect to a 5G network, causing battery drain and overheating.
- The only mitigation is forcing the device into 4G-only mode.

An additional check is baked directly into the modem firmware (`md1img` partition) and is not patchable by third parties. Even porting the entire vendor partition from another Samsung 5G device did not resolve the issue.

### 🔴 Dimensity 6100+ / 6300 — Bootloop After Custom Binary Flash (Early Firmware)

This issue affected early firmware and has been **fixed by updates from the January/April/July 2025 security patches onward**. If your firmware predates those patches, flashing an unsigned binary (custom kernel, Magisk-patched boot image) causes a persistent bootloop state where Android recovery becomes inaccessible and only Download mode remains accessible — even after reverting all changes.

**If your firmware is already updated past the January 2025 patch, this issue does not apply.**

### Camera Issues After Unlock

- As of September 2025, the **Galaxy Z Fold 5** presents a black viewfinder screen after unlocking — confirmed as an intentional "security mechanism" that is reversible by re-locking the bootloader.
- The **Korean Galaxy Fold3** on One UI 5 still had cameras disabled after unlocking as of late 2023; EU and CN variants had resolved the issue earlier.

### SoC-Level Exploits Do Not Apply

Samsung bootloaders check on every boot whether unlocking has been authorised and automatically re-lock if not. SoC-level exploits such as **mtkclient** or **EDLUnlock** therefore do not persist on Samsung devices — Samsung verifies and signs their own bootloaders, making re-flashing a modified version infeasible.

### Partial Mitigations

Some Knox-based features can be partially restored using [KnoxPatch](https://github.com/BlackMesa123/KnoxPatch) (LSPosed) and its companion [KnoxPatch Enhancer](https://github.com/BlackMesa123/KnoxPatch#knoxpatch-enhancer) (Magisk/KernelSU). VoLTE will not work on GSI ROMs due to Samsung's IMS stack being incompatible with AOSP's — a partial [open-source VoLTE service](https://github.com/phhusson/ims) by phh exists but remains incomplete.

### Further Reading

- [One UI 8 bootloader unlock removal — XDA](https://xdaforums.com/t/bootloader-unlocking-option-removed-from-one-ui-8-0.4751904/)
- [Rollback protection bit explained — SamFW](https://samfw.com/blog/what-is-bit-binary-value)
- [Galaxy Z Fold 3 camera fix — XDA](https://www.xda-developers.com/bootloader-unlocking-no-longer-kills-galaxy-z-fold-3-cameras/)
- [Galaxy S22 bootloader unlock camera fix — XDA](https://www.xda-developers.com/samsung-galaxy-s22-bootloader-unlock-camera-working/)

*Samsung research sourced from the [bootloader-unlock-wall-of-shame](https://github.com/zenfyrdev/bootloader-unlock-wall-of-shame) project. Additional contributions by [aries-ts-indo](https://github.com/aries-ts-indo), [ravindu644](https://github.com/ravindu644), and [Ivy / Lost-Entrepreneur439](https://github.com/Lost-Entrepreneur439). Authored by [melontini](https://github.com/melontini).*

---

## Xiaomi / Redmi / POCO

**Verdict: 🟡 Restricted (technically possible, deliberately obstructed)**

> **⚠️ China region devices:** It is currently **impossible** to unlock Xiaomi phones from the China region. Xiaomi has removed the unlocking function from their Community App for this region entirely. This also applies to Chinese devices imported and used outside China.

### Background — MIUI vs HyperOS

Under MIUI 14 and earlier, unlocking required logging a Mi Account on the device, enabling the unlock request in Developer Options, waiting 7 days, then running the official Mi Unlock Tool. Not fast, but doable entirely through official channels.

With the introduction of **HyperOS** (essentially MIUI 15 rebranded), Xiaomi added a mandatory additional step before the Developer Options request even becomes available.

### The HyperOS Unlock Process (Global Region)

The current process requires all of the following to be in place:

1. **Xiaomi Community App** version 5.3.31 or above, installed from Google Play
2. **Mi Account active for more than 30 days**
3. **Phone number linked** to the Mi Account
4. Inside the Community App: navigate to Settings → select Global region → "Unlock Bootloader" → submit a request

Only *after* a successful Community App request can you proceed to the Developer Options step and the 7-day (or longer) waiting period.

**Critically:** there is a global daily cap on how many Community App requests are accepted. This cap fills almost instantly, meaning your only realistic window is attempting the request at the precise moment the daily quota resets.

### Account and Device Limits

As of **January 1st, 2025**, Xiaomi further tightened limits:

- **1 device per year** per account (down from 3)
- **2 devices per SIM card** per 3-month period
- OTA updates are disabled after unlocking
- Warranty is voided (including extended warranties such as Mi Care)

### Unisoc Devices — Never Unlockable

Devices using **Unisoc SoCs** will never be unlockable. This is not Xiaomi's policy but a hardware-level restriction imposed by Unisoc itself, which does not permit bootloader unlocking on its platform.

### Community Bypass Tools

Several bypass tools exist that exploit vulnerabilities in the Community App request step, allowing users to complete the binding process and then proceed with the standard 7-day unlock wait:

- **[MlgmXyysd/Xiaomi-HyperOS-BootLoader-Bypass](https://github.com/MlgmXyysd/Xiaomi-HyperOS-BootLoader-Bypass)** — the original PoC; works on Qualcomm devices running HyperOS 2 and 3. The same developer has also identified a newer vulnerability affecting most HyperOS 2 and 3 Qualcomm devices.
- **HyperSploit** — user-friendly wrapper; patched as of HyperOS 2.0.203.0, works only on older builds.
- **[MiUnlockTool](https://github.com/topminipie/awesome-xiaomi-bootloader-unlock)** — open-source cross-platform alternative to the official Windows-only Mi Unlock Tool.

> ⚠️ **Risk:** Using bypass tools may result in your device or Mi Account being flagged or banned by Xiaomi's "risk control" system. Bypass tools do not skip the 7/14/30-day waiting period — they only address the Community App binding step.

### Consequences of Unlocking

- **OTA updates disabled** — you will not receive official over-the-air updates.
- **Warranty voided** — including extended warranties. Under EU law, the statutory two-year warranty still applies, but Xiaomi must prove a causal link between the unlock and the specific defect claimed.
- **TEE-related features permanently damaged** — similar in effect to Samsung's Knox trip.

### Further Reading

- [Xiaomi HyperOS BootLoader Bypass — GitHub](https://github.com/MlgmXyysd/Xiaomi-HyperOS-BootLoader-Bypass)
- [Awesome Xiaomi Bootloader Unlock — GitHub](https://github.com/topminipie/awesome-xiaomi-bootloader-unlock)
- [Xiaomi bootloader unlock wall-of-shame entry](https://github.com/zenfyrdev/bootloader-unlock-wall-of-shame/blob/main/brands/xiaomi/README.md)

*Xiaomi research sourced from the [bootloader-unlock-wall-of-shame](https://github.com/zenfyrdev/bootloader-unlock-wall-of-shame) project.*

---

*This page is part of Fortress64's ongoing research into manufacturer restrictions on device ownership. See also: [We Are Done Asking Permission to Use Our Own Devices](https://fortress64.github.io/).*
