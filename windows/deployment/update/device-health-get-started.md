---
title: Get started with Device Health
description: Configure Device Health in OMS to see statistics on frequency and causes of crashes of devices in your network.
keywords: Device Health, oms, operations management suite, prerequisites, requirements, monitoring, crash, drivers
ms.prod: w10
ms.mktglfcycl: deploy
ms.sitesec: library
ms.date: 08/21/2018
ms.pagetype: deploy
author: jaimeo
ms.author: jaimeo
ms.localizationpriority: medium
---

# Get started with Device Health

>[!IMPORTANT]
>**The OMS portal has been deprecated; you should start using the [Azure portal](https://portal.azure.com) instead as soon as possible.** Many experiences are the same in the two portals, but there are some key differences. See [Windows Analytics in the Azure Portal](windows-analytics-azure-portal.md) for steps to use Windows Analytics in the Azure portal. For much more information about the transition from OMS to Azure, see [OMS portal moving to Azure](https://docs.microsoft.com/azure/log-analytics/log-analytics-oms-portal-transition).

This topic explains the steps necessary to configure your environment for Windows Analytics: Device Health. 

Steps are provided in sections that follow the recommended setup process:

1. [Add Device Health](#add-device-health-to-microsoft-operations-management-suite) to Microsoft Operations Management Suite.
2. [Enroll devices in Windows Analytics](#deploy-your-commercial-id-to-your-windows-10-devices) to your organization’s devices.
3. [Use Device Health to monitor frequency and causes of device crashes](#use-device-health-to-monitor-frequency-and-causes-of-device-crashes) once your devices are enrolled.



## Add Device Health to Microsoft Operations Management Suite or Azure Log Analytics

Device Health is offered as a solution in the Microsoft Operations Management Suite (OMS) and Azure Log Analytics, a collection of cloud-based servicing for monitoring and automating your on-premises and cloud environments. For more information about OMS, see [Operations Management Suite overview](https://azure.microsoft.com/en-us/documentation/articles/operations-management-suite-overview/) or the Azure [Log Analytics overview](https://azure.microsoft.com/services/log-analytics/).

**If you are already using Windows Analytics**, you should use the same Azure Log Analytics workspace you're already using. Find Device Health in the Solutions Gallery. Select the **Device Health** tile in the gallery and then click **Add** on the solution's details page. Device Health is now visible in your workspace. While you're in the Solutions Gallery, you should consider installing the [Upgrade Readiness](../upgrade/use-upgrade-readiness-to-manage-windows-upgrades.md)  and [Update Compliance](update-compliance-monitor.md) solutions as well, if you haven't already.

>[!NOTE]
>If you are already using OMS, you can also follow [this link](https://portal.mms.microsoft.com/#Workspace/ipgallery/details/details/index?IPId=DeviceHealthProd) to go directly to the Device Health solution and add it to your workspace.

**If you are not yet using Windows Analytics or Azure Log Analytics**, follow these steps to subscribe:

1.	Go to [Operations Management Suite](https://www.microsoft.com/en-us/cloud-platform/operations-management-suite) on Microsoft.com and click **Sign in**.
   [![Operations Management Suite bar with sign-in button](images/uc-02a.png)](images/uc-02.png)


2.	Sign in to Operations Management Suite (OMS). You can use either a Microsoft Account or a Work or School account to create a workspace. If your company is already using Azure Active Directory (Azure AD), use a Work or School account when you sign in to OMS. Using a Work or School account allows you to use identities from your Azure AD to manage permissions in OMS.
   [![OMS Sign-in dialog box for account name and password](images/uc-03a.png)](images/uc-03.png)


3.	Create a new OMS workspace.

     [![OMS dialog with buttons to create a new OMS workspace or cancel](images/uc-04a.png)](images/uc-04.png)

4.	Enter a name for the workspace, select the workspace region, and provide the email address that you want associated with this workspace. Click **Create**.

    [![OMS Create New Workspace dialog](images/uc-05a.png)](images/uc-05.png)

5.	If your organization already has an Azure subscription, you can link it to your workspace. Note that you may need to request access from your organization’s Azure administrator. If your organization does not have an Azure subscription, create a new one or select the default OMS Azure subscription from the list. If you do not yet have an Azure subscription, follow [this guide](https://blogs.technet.microsoft.com/upgradeanalytics/2016/11/08/linking-operations-management-suite-workspaces-to-microsoft-azure/) to create and link an Azure subscription to an OMS workspace.

    [![OMS dialog to link existing Azure subscription or create a new one](images/uc-06a.png)](images/uc-06.png)

6.	To add Update Readiness to your workspace, go to the Solution Gallery, Select the **Update Readiness** tile and then select **Add** on the solution's detail page.

    [![Windows Analytics details page in Solutions Gallery](images/solution-bundle.png)](images/solution-bundle.png)

7.	Click the **Update Readiness** tile to configure the solution. The **Settings Dashboard** opens. In this example, both Upgrade Readiness and Device Health solutions have been added.

    [![OMS Settings Dashboard showing Device Health and Upgrade Readiness tiles](images/OMS-after-adding-solution.jpg)](images/OMS-after-adding-solution.jpg)



After you have added Device Health and devices have a Commercial ID, you will begin receiving data. It will typically take 24-48 hours for the first data to begin appearing. The following section explains how to deploy your Commercial ID to your Windows 10 devices.

>[!NOTE]
>You can unsubscribe from the Device Health solution if you no longer want to monitor your organization’s devices. User device data will continue to be shared with Microsoft while the opt-in keys are set on user devices and the proxy allows traffic.

## Enroll devices in Windows Analytics

Once you've added Update Compliance to Microsoft Operations Management Suite, you can now start enrolling the devices in your organization. For full instructions, see [Enrolling devices in Windows Analytics](windows-analytics-get-started.md).


## Use Device Health to monitor frequency and causes of device crashes

Once your devices are enrolled, you can move on to [Using Device Health](device-health-using.md).


## Related topics

[Use Device Health to monitor frequency and causes of device crashes](device-health-using.md)<BR>
For the latest information on Windows Analytics, including new features and usage tips, see the [Windows Analytics blog](https://blogs.technet.microsoft.com/upgradeanalytics)
