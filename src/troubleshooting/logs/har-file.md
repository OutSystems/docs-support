---
summary:
tags: 
locale: en-us
guid: b2a4ae4c-7b24-491b-b3f2-182e0b73e0b0
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
---
# Network HAR file

There are different ways for getting an HAR file for different browsers. Steps to get the HAR file in popular browsers are listed below:

### HAR file for Google Chrome
To get the Network HAR file in Google Chrome, follow these steps:

1. Navigate to the page of the application that is facing the issue.
1. Press **F12** or open the dev tools on the top right of Google Chrome. Under **More tools**, select **Developer Tools**.
1. Open the **Network** tab.
1. Check the **Preserve log** option and clear the log.
1. Turn on recording using the **Record Network Log** button.
1. Attempt to reproduce the issue.
1. Right-click the log and Save as HAR with content.

### HAR file for Firefox
To get the Network HAR file in Firefox, follow these steps:

1. Navigate to the page of the application that is facing the issue.
1. Press **F12** or open the dev tools by selecting the Firefox menu (three horizontal parallel lines) at the top-right of your browser window. Under **More tools**, select **Web Developer Tools**.
1. Open the **Network** tab.
1. Check the **Preserve log** option and clear the log.
1. The recording autostarts when you start performing actions in the browser.
1. Attempt to reproduce the issue.
1. Once you have reproduced the issue and you see that all of the actions have been generated in the Developer Network Panel, right-click anywhere under the **File** column, and click **Save all as Har**.

### HAR file for Edge
To get the Network HAR file in Edge, follow these steps:

1. Press **F12** to open the debug pane.
1. Clear the session history before reproducing.
1. To clear the session history press the button indicated by three lines and a red **X**.
1. Click **Play** at the top left of the debug pane to start recording.
1. Reproduce the issue.
1. Press the **red square** to stop recording.
1. Export the results as a HAR file by pressing the **Save** button that is identified as a floppy disk.

### HAR file for IE11

To get the Network HAR file in IE11, follow these steps:

1. Press **F12** or go to the **Tools** menu and select **F12 Developer Tools**.
1. Open the **Network** tab.
1. Press the **green play button** (Enable network traffic capturing F5) on the left to start capturing.
1. Refresh the page by pressing **F5** on your keyboard, and the network traffic should be displayed.
1. Once the trace is complete, press **Export captured traffic** (second from left) and save the network trace as an xml file.
