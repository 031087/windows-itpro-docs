---
title: Deploy your Windows Information Protection (WIP) policy using Microsoft Intune (Windows 10)
description: After you’ve created your Windows Information Protection (WIP) policy, you'll need to deploy it to your organization's enrolled devices.
ms.assetid: 9c4a01e7-0b1c-4f15-95d0-0389f0686211
keywords: WIP, Windows Information Protection, EDP, Enterprise Data Protection, Intune
ms.prod: w10
ms.mktglfcycl: explore
ms.sitesec: library
ms.pagetype: security
author: eross-msft
localizationpriority: high
---

# Deploy your Windows Information Protection (WIP) policy using Microsoft Intune
**Applies to:**

-   Windows 10, version 1607
-   Windows 10 Mobile

After you’ve created your Windows Information Protection (WIP) policy, you'll need to deploy it to your organization's enrolled devices. Enrollment can be done for business or personal devices, allowing the devices to use your managed apps and to sync with your managed content and information.

**To deploy your WIP policy**

1.  On the **Configuration policies** page, locate your newly-created policy, click to select it, and then click the **Manage Deployment** button.

    ![Microsoft Intune: Click the Manage Deployment link from the Configuration Policies screen](images/intune-managedeployment.png)

2.  In the left pane of the **Manage Deployment** box, click the employees or groups that should get the policy, and then click **Add**.<p>
The added people move to the **Selected Groups** list on the right-hand pane.

    ![Microsoft Intune: Pick the group of employees that should get the policy](images/intune-groupselection.png)

3.  After you've picked all of the employees and groups that should get the policy, click **OK**.<p>
The policy is deployed to the selected users' devices.

## Related topics
- [Create a Windows Information Protection (WIP) policy using Microsoft Intune](create-wip-policy-using-intune.md)
- [Add apps to your Windows Information Protection (WIP) policy by using the Microsoft Intune custom URI functionality](add-apps-to-protected-list-using-custom-uri.md)
- [Create and deploy a VPN policy for Windows Information Protection (WIP) using Microsoft Intune](create-vpn-and-wip-policy-using-intune.md)
- [General guidance and best practices for Windows Information Protection (WIP)](guidance-and-best-practices-wip.md)