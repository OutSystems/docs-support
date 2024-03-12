---
summary: The article provides a guide on how to access mobile app package generation logs in Service Studio and Service Center console
tags:
locale: en-us
guid: 5a5f216b-421f-447a-b822-f1ec74910523
app_type: mobile apps
platform-version: o11
figma: https://www.figma.com/file/6tXLupLiqfG9FOElATTGQU/Troubleshooting?node-id=3327:538
---
# Mobile app generation logs

To get mobile app package generation log, follow these steps:

1. If you are in Service Studio, go to the details page of the mobile app and click **Application Management...** to open the mobile app's page in Service Center console. The page opens in a separate browser.

    ![Screenshot highlighting the 'Application Management...' option in Service Studio to access mobile app details in Service Center.](images/get-logs-16.png "Accessing Application Management in Service Studio")

Otherwise, open the Service Center console of the environment (`https://<your_server>/ServiceCenter`), go to **Factory** » **Applications**, and click the mobile app name to go to the app details page.

2. Go to the **Native Platforms** tab. You will see the information about the latest mobile app package generation for each mobile platform.

    ![Screenshot of the Native Platforms tab in Service Center showing where to find the log file icon for mobile app package generation.](images/get-logs-17.png "Native Platforms Tab in Service Center")

3. Click the Log File icon to save the file.

