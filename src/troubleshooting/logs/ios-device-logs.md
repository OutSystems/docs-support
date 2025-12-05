---
summary: Discover methods to retrieve iOS device logs with Apple Configurator 2, Xcode, iTools, and iOSLogInfo in OutSystems 11 (O11).
tags: ios development, log retrieval, debugging, troubleshooting, cross-platform tools
locale: en-us
guid: c05d23c9-e912-469a-ab6b-7fe6a9d97da8
app_type: mobile apps
platform-version: o11
figma:
audience:
  - mobile developers
outsystems-tools:
  - none
coverage-type:
  - unblock
---

# Get iOS Device Logs

To get iOS device logs using **Apple Configurator 2**, follow these steps:

1. First, install Apple Configurator 2 from App Store and launch the application.
1. Connect your iOS device to the Mac through USB. On the device screen, you will be asked if you trust the computer. Tap Trust.
1. By default, all the connected devices will appear on the home screen. Double click on the device you wish to get the logs from.
1. Click on Console from the menu on the top left corner of the new window. You can see the log activities on the screen.
1. Click **Clear** to clear the screen and perform the necessary actions (for example, an app crash) you wish to.
1. Click **Save** button to save the logs.

To get iOS device logs using **Xcode**, follow these steps:

1. Install Xcode on your mac machine. Next, launch Xcode.
1. Connect your iOS device to the Mac through USB.
1. Launch Xcode. Go to **Windows > Devices and Simulators**.
1. Reproduce the problem you encountered.
1. Choose your device from the devices section on the left side of the screen.
1. Click on the up-triangle on the bottom of the screen to view device logs.
1. Click on the down arrow on the bottom right of the screen to save the device logs as a file.
1. Select View Device Logs button under the Device Information section on the right-hand panel to view crash logs.
1. Under Process column on the left, identify and select your app and click **Crash Log** to see the contents.
1. Right click the corresponding app entry on the Process Column and click **Export Log** to save the crash log.

To get iOS device logs using **iTools in Windows**, follow these steps:

1. Install iTools on your Windows machine.
1. Launch iTools. Connect your iOS device to the Windows machine through USB.
1. Click Toolbox.
1. When you are ready to reproduce the issue, click **Real-time log** under **Advanced Features**.
You can see the logging happening in real-time.

Click on Save to save the log activities.

To get iOS device logs using **iOSLogInfo in Windows**, follow these steps:

You must have iTunes installed on your Windows machine before you start using iOSLogInfo.

1. Install iOSLogInfo on your device.
1. Extract the contents of the folder to the local hard drive.
1. Connect your iOS device to the Windows machine through a cable.
1. Open a new command prompt and make sure that you run as administrator.
1. On your command prompt, use the following command to navigate to the location where you have extracted the files. For example, if I have extracted the files to my C drive, the command would be as follows: `cd C:\iOSLogInfo`.
1. Type in the following command to start capturing the device log to a file. Give a suitable name for the file.
`sdsiosloginfo.exe -d C:\iOSLogInfo\logfile.txt`.
1. Reproduce the action causing the issue.
1. Click **CTRL+C** to stop logging.

A new text file(logfile.txt) will be created in the iOSLogInfo folder.
