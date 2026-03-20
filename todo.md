---

> **🗂 Temp — move to separate pages**
>
> ### Play Store & Alternative App Stores
> The crDroid and LineageOS ROMs provide a customizable Android experience with MicroG, a free alternative to Google Play Services, allowing users to access essential functionalities without proprietary software. They also include Aurora Store, which lets users download apps from the Google Play Store without a Google account, and F-Droid, a repository of free and open-source applications. Together, these tools offer a complete and privacy-focused alternative to GApps.
>
> ### Common Issues & Fixes
>
> **1. Black Screen After Booting Custom Recovery**
> - **Cause:** The ROM uses `vendor_boot`, which can cause issues with custom recoveries.
> - **Solution:**
>   1. Use a ROM that supports non-`vendor_boot` recoveries.
>   2. Ensure you flash both the `boot` and `vendor_boot` images correctly.
>
> **2. Screen Hangs in Custom Recovery**
> - **Cause:** The recovery may not support encryption, or the data partition may be corrupted.
> - **Action 1:** Disable your screen lock for better compatibility.
> - **Action 2:** If the issue persists, perform a factory reset or switch to a recovery that supports decryption.
>
> **3. Touchscreen/Sideloading Not Working in Recovery**
> - **Cause:** An outdated ROM or firmware may have loaded old vendor firmware.
> - **Solution:** Flash the latest ROM to update the vendor partition.

## 🏪 Play Store & Alternative App Stores

### 9. Aurora Store / MicroG / MindTheGapps / Play Store Support

1. **Default App Stores by ROM:**
   - **CrDroid:** Aurora Store / FDroid / MicroG
   - **LineageOS:** Aurora Store / FDroid / MicroG
   - **E/OS:** Aurora Store, App Lounge, MicroG
   - **LMODroid:** Aurora Store

2. **MindTheGapps Support:**
   - Please note that GApps support is not included by default. However, in most cases, you can rely on MicroG as an alternative.

3. **MindTheGapps Installation:**
   - Download for **CrDroid/LineageOS**: [ARM64](https://mindthegapps.com/#MindTheGapps-for-Android-15-LineageOS-22)
   - Download for **E/OS & LMODroid**: [ARM64](https://mindthegapps.com/#MindTheGapps-for-Android-14-LineageOS-21)
   - Flash the .zip files using the recovery mode.

---

## ⚠️ Common Issues & Fixes

### 1. Black Screen After Booting Custom Recovery
- **Cause:** The ROM uses `vendor_boot`, which can cause issues with custom recoveries.
- **Solution:** 
  1. Use a ROM that supports non-`vendor_boot` recoveries.
  2. Ensure you flash both the `boot` and `vendor_boot` images correctly.

### 2. Screen Hangs in Custom Recovery
- **Cause:** The recovery may not support encryption, or the data partition may be corrupted.

#### Action 1: Disable Screen Lock
- **Solution:** Disable your screen lock for better compatibility.

#### Action 2: Perform Factory Reset or Use a Compatible Recovery
- **Solution:** If the issue persists, perform a factory reset or switch to a recovery that supports decryption.

### 3. Touchscreen/Sideloading Not Working in Recovery
- **Cause:** An outdated ROM or firmware may have loaded old vendor firmware.
- **Solution:** Flash the latest ROM to update the vendor partition.

---

✅ **You're all set!** Enjoy your new custom ROM!


---

## 4.📝 Notes
1. Always use the latest firmware before flashing custom ROMs.
2. Follow the exact steps to avoid boot loops or bricked devices.
3. Utilize **ADB** and **Fastboot** tools for a seamless flashing experience.
4. A custom recovery and Magisk must be flashed after each update, as they are overwritten by the updating process.
5. Updates will be released monthly or quarterly, and unpopular ROMs with fewer than 10 users may be dropped eventually.
6. We welcome your opinions or corrections if they can help improve our work.
    
---
