---
title: Get started with Upgrade Readiness (Windows 10)
description: Explains how to get started with Upgrade Readiness.
keywords: windows analytics, oms, operations management suite, prerequisites, requirements, upgrades, log analytics, 
ms.prod: w10
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: deploy
author: jaimeo
ms.author: jaimeo
ms.date: 08/21/2018
ms.localizationpriority: medium
---

# Get started with Upgrade Readiness

>[!IMPORTANT]
>**The OMS portal has been deprecated; you should start using the [Azure portal](LINK) instead as soon as possible.** Many experiences are the same in the two portals, but there are some key differences. See [Windows Analytics in the Azure Portal](windows-analytics-azure-portal.md) for steps to use Windows Analytics in the Azure portal. For much more information about the transition from OMS to Azure, see [OMS portal moving to Azure](https://docs.microsoft.com/azure/log-analytics/log-analytics-oms-portal-transition).

This topic explains how to obtain and configure Upgrade Readiness for your organization. 

You can use Upgrade Readiness to plan and manage your upgrade project end-to-end. Upgrade Readiness works by establishing communications between computers in your organization and Microsoft. Upgrade Readiness collects computer, application, and driver data for analysis. This data is used to identify compatibility issues that can block your upgrade and to suggest fixes that are known to Microsoft.

Before you begin, consider reviewing the following helpful information:<BR>
    - [Upgrade Readiness requirements](upgrade-readiness-requirements.md): Provides detailed requirements to use Upgrade Readiness.<BR>
    - [Upgrade Readiness blog](https://blogs.technet.microsoft.com/UpgradeAnalytics): Contains announcements of new features and provides helpful tips for using Upgrade Readiness.

>If you are using System Center Configuration Manager, also check out information about how to integrate Upgrade Readiness with Configuration Manager: [Integrate Upgrade Readiness with System Center Configuration Manager](https://docs.microsoft.com/sccm/core/clients/manage/upgrade/upgrade-analytics).

When you are ready to begin using Upgrade Readiness, perform the following steps:

1. Review [data collection and privacy](#data-collection-and-privacy) information.
2. [Add Upgrade Readiness to OMS](#add-upgrade-readiness-to-operations-management-suite).
3. [Enroll devices in Windows Analytics](#enroll-devices-in-windows-analytics).
4. [Use Upgrade Readiness to manage Windows Upgrades](#use-upgrade-readiness-to-manage-windows-upgrades) once your devices are enrolled.

## Data collection and privacy 

To enable system, application, and driver data to be shared with Microsoft, you must configure user computers to send data. For information about what diagnostic data Microsoft collects and how that data is used and protected by Microsoft, see the following topics, refer to [Frequently asked questions and troubleshooting Windows Analytics](https://docs.microsoft.com/windows/deployment/update/windows-analytics-FAQ-troubleshooting), which discusses the issues and provides links to still more detailed information.

## Add Upgrade Readiness to Operations Management Suite or Azure Log Analytics

Upgrade Readiness is offered as a solution in the Microsoft Operations Management Suite (OMS), a collection of cloud based services for managing your on-premises and cloud environments. For more information about OMS, see [Operations Management Suite overview](http://azure.microsoft.com/documentation/articles/operations-management-suite-overview/).

>[!IMPORTANT]
>Upgrade Readiness is a free solution for Azure subscribers. When configured correctly, all data associated with the Upgrade Readiness solution are exempt from billing in both OMS and Azure. Upgrade Readiness data **do not** count toward OMS daily upload limits. The Upgrade Readiness service will ingest a full snapshot of your data into your OMS workspace on a daily basis. Each snapshot includes all of your devices that have been active within the past 30 days regardless of your OMS retention period.

If you are already using OMS, you’ll find Upgrade Readiness in the Solutions Gallery. Select the **Upgrade Readiness** tile in the gallery and then click **Add** on the solution's details page. Upgrade Readiness is now visible in your workspace. While you have this dialog open, you should also consider adding the [Device Health](../update/device-health-monitor.md) and [Update Compliance](../update/update-compliance-monitor.md) solutions as well, if you haven't already. To do so, just select the check boxes for those solutions.

>[!NOTE]
>If you are already using OMS, you can also follow [this link](https://portal.mms.microsoft.com/#Workspace/ipgallery/details/details/index?IPId=CompatibilityAssessment) to go directly to the Upgrade Readiness solution and add it to your workspace.

If you are not using OMS or Azure Log Analytics:

1.  Go to [Log Analytics](https://azure.microsoft.com/services/log-analytics/) on Microsoft.com and select **Start free** to start the setup process. During the process, you’ll create a workspace and add the Upgrade Readiness solution to it.
2.  Sign in to Operations Management Suite (OMS) or Azure Log Analytics. You can use either a Microsoft Account or a Work or School account to create a workspace. If your company is already using Azure Active Directory (Azure AD), use a Work or School account when you sign in to OMS. Using a Work or School account allows you to use identities from your Azure AD to manage permissions in OMS.
3.  Create a new workspace. Enter a name for the workspace, select the workspace region, and provide the email address that you want associated with this workspace. Select **Create**.
4.  If your organization already has an Azure subscription, you can link it to your workspace. Note that you may need to request access from your organization’s Azure administrator.

    > If your organization does not have an Azure subscription, create a new one or select the default OMS Azure subscription from the list. Your workspace opens.

5.  To add the Upgrade Readiness solution to your workspace, go to the **Solutions Gallery**. Select the **Upgrade Readiness** tile in the gallery and then select **Add** on the solution’s details page. The solution is now visible on your workspace. Note that you may need to scroll to find Upgrade Readiness.

## Enroll devices in Windows Analytics

Once you've added Update Compliance to Microsoft Operations Management Suite, you can now start enrolling the devices in your organization. For full instructions, see [Enrolling devices in Windows Analytics](https://docs.microsoft.com/windows/deployment/update/windows-analytics-get-started).



## Use Upgrade Readiness to manage Windows Upgrades

Now that your devices are enrolled, you can move on to [Use Upgrade Readiness to manage Windows Upgrades](https://docs.microsoft.com/windows/deployment/upgrade/use-upgrade-readiness-to-manage-windows-upgrades).
