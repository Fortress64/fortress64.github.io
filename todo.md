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
