---
summary:
tags: 
locale: en-us
guid: c05d23c9-e912-469a-ab6b-7fe6a9d97da8
app_type: mobile apps
---
## Get iOS Device Logs

To get iOS device logs using **Apple Configurator 2**, follow these steps:

1. First, install Apple Configurator 2 from App Store and launch the application.
2.  Connect your iOS device to the Mac through USB. On the device screen, you will be asked if you trust the computer. Tap Trust.
3. By default, all the connected devices will appear on the home screen. Double click on the device you wish to get the logs from.
4. Click on Console from the menu on the top left corner of the new window. You can see the log activities on the screen.
5. Click **Clear** to clear the screen and perform the necessary actions (for example, an app crash) you wish to.
6. Click **Save** button to save the logs.


To get iOS device logs using **Xcode**, follow these steps:

1. Install Xcode on your mac machine. Next, launch Xcode.
2. Connect your iOS device to the Mac through USB.
3. Launch Xcode. Go to **Windows > Devices and Simulators**.
4. Reproduce the problem you encountered.
5. Choose your device from the devices section on the left side of the screen.
6. Click on the up-triangle on the bottom of the screen to view device logs.
7. Click on the down arrow on the bottom right of the screen to save the device logs as a file.
8. Select View Device Logs button under the Device Information section on the right-hand panel to view crash logs.
9. Under Process column on the left, identify and select your app and click **Crash Log** to see the contents.
10. Right click the corresponding app entry on the Process Column and click **Export Log** to save the crash log.

To get iOS device logs using **iTools in Windows**, follow these steps:

1. Install iTools on your Windows machine.
2. Launch iTools. Connect your iOS device to the Windows machine through USB.
3. Click Toolbox.
4. When you are ready to reproduce the issue, click **Real-time log** under **Advanced Features**. 
You can see the logging happening in real-time.

Click on Save to save the log activities.

To get iOS device logs using **iOSLogInfo in Windows**, follow these steps:

You must have iTunes installed on your Windows machine before you start using iOSLogInfo.

1. Install iOSLogInfo on your device.
2. Extract the contents of the folder to the local hard drive.
3. Connect your iOS device to the Windows machine through a cable.
4. Open a new command prompt and make sure that you run as administrator.
5. On your command prompt, use the following command to navigate to the location where you have extracted the files. For example, if I have extracted the files to my C drive, the command would be as follows: `cd C:\iOSLogInfo`.
6. Type in the following command to start capturing the device log to a file. Give a suitable name for the file.
`sdsiosloginfo.exe -d C:\iOSLogInfo\logfile.txt`.
7. Reproduce the action causing the issue.
8. Click **CTRL+C** to stop logging.

A new text file(logfile.txt) will be created in the iOSLogInfo folder.
