---
summary: This document is for operators who want to delete an OutSystems application deployed manually to a container.
---

# Deleting an application that is manually deployed to a container

Before deleting an application that was manually deployed to a container, you first need to change the application's deployment zone to "Global". You may also need to restart the Windows service **OutSystems Deployment Controller Service**.

1. Find your application in **Service Center** > **Factory** > **Applications** and click on its name. A page with a detailed view of the application properties opens.
1. Go to the **Operation** tab, and in the **Deployment Zone** drop-down list select **Global**. Click **Save**.
1. Still on the same page, click **Publish**.
1. [Undeploy the application](<https://success.outsystems.com/Documentation/11/Managing_the_Applications_Lifecycle/Deploying_to_Containers/Running_Your_Application_in_a_Container#Undeploy_an_Application_in_Containers>) from the container. Verify that the undeployment process was successful.
1. Verify the **Deployment Zone** is still **Global**, click **Delete** and confirm the deletion in the pop-up window that opens.
1. If the deletion was successful, you will see the following message at the top of the page: "The application was deleted successfully". If the page hangs after confirming the deletion in the previous step, restart the Windows service **OutSystems Deployment Controller Service** running on the machine.
