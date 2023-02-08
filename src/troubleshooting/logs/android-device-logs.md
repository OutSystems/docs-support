---
summary:
tags: 
locale: en-us
guid: 36b333c2-1bf0-4e3e-9162-6894bb2c76f7
app_type: mobile apps
platform-version: o11
---
# Android device logs

To get more information to troubleshoot eventual issues, we check the device logs using adb and logcat together. You can accomplish this by following these steps:

1. [Enable Developer Mode](`https://developer.android.com/studio/debug/dev-options#enable`) and USB Debugging on your Android device.
1. Download Android's **platform-tools** from the [Official Android website](`https://developer.android.com/studio/releases/platform-tools.html`) to your computer.
1. Extract platforms-tools to a directory of your choice (we'll refer to it as `<directory_path>` from now on).
1. Open a command line and jump to `<directory_path>`.
1. Connect your Android device to your computer and ensure that USB Debugging is active. You can validate that it's correctly connected using this command:
`adb.exe devices`
If you see no devices on the list that is printed, please validate that USB Debugging is, in fact, enabled. In case it is, we recommend following the steps provided on this more thorough [this article](`https://www.howtogeek.com/125769/how-to-install-and-use-abd-the-android-debug-bridge-utility/`).
1. Run the following command to clear the logs of your device first:
`adb.exe logcat -c`
1. Reproduce the error.
1. Run the following command to extract the logs:
`adb.exe logcat -d > device.log`
1. Wait a couple of seconds and click **CTRL + C** in the command line to stop the process.
1. Send the **device.log** file found in `<directory_path>` to OutSystems Support. 

If none of these steps failed, you should have a file with entries on it. If the file has a size of 0kb (empty), please review all the previous steps.
