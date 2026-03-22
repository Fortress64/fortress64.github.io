---
title: Troubleshooting
---
🛠 Troubleshooting Boot Loops & Issues

If you experience a boot loop or other issues, follow these steps:

    Capture Logs via ADB:
        Before powering off the device, connect it to your PC.
        Run the following command:

        adb shell logcat *:E

        Allow the device to start and try to replicate the issue.

    Using Matlog (if the device is usable):
        Install Matlog.
        Perform the action that is not working properly.
        Save the log file.

    Sharing the Logs:
        Upload the log contents to Hastebin.
        Inform us on the XDA forum, but do not post logs directly on the forum as they may contain private information and clutter discussions
