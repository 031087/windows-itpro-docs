---
title: Windows Autopilot platforms
ms.reviewer: 
manager: laurawi
description: Windows Autopilot deployment
keywords: mdm, setup, windows, windows 10, oobe, manage, deploy, autopilot, ztd, zero-touch, partner, msfb, intune
ms.prod: w10
ms.mktglfcycl: deploy
ms.localizationpriority: medium
ms.sitesec: library
ms.pagetype: deploy
author: greg-lindsay
ms.author: greglin
ms.collection: M365-modern-desktop
ms.topic: article
---


# Windows Autopilot platforms

**Applies to**

-   Windows 10

Several platforms are available to register devices with Windows Autopilot. A summary of each platform's capabilities is provided below.

>Microsoft recommends **Intune** to register Autopilot devices and configure settings.

<br><table>
<tr>
<td BGCOLOR="#a0e4fa"><B>Platform/Portal</th>
<td BGCOLOR="#a0e4fa"><B>Register devices?</th>
<td BGCOLOR="#a0e4fa"><B>Create/Assign profile</th>
<td BGCOLOR="#a0e4fa"><B>Acceptable DeviceID</th>
</tr>

<tr>
<td>OEM Direct API</td>
<td>YES - 1000 at a time max</td>
<td>NO</td>
<td>Tuple or PKID</td>
</tr>

<tr>
<td><a href="https://docs.microsoft.com/partner-center/autopilot">Partner Center</a></td>
<td>YES - 1000 at a time max</td>
<td>YES</td>
<td>Tuple or PKID or 4K HH</td>
</tr>

<tr>
<td><a href="https://docs.microsoft.com/intune/enrollment-autopilot">Intune</a></td>
<td>YES - 500 at a time max<b>\*</b></td>
<td>YES<b>\*</b></td>
<td>4K HH</td>
</tr>

<tr>
<td><a href="https://docs.microsoft.com/microsoft-store/add-profile-to-devices#manage-autopilot-deployment-profiles">Microsoft Store for Business</a></td>
<td>YES - 1000 at a time max</td>
<td>YES</td>
<td>4K HH</td>
</tr>

<tr>
<td><a href="https://docs.microsoft.com/microsoft-365/business/create-and-edit-autopilot-profiles">Microsoft Business 365</a></td>
<td>YES - 1000 at a time max</td>
<td>YES</td>
<td>4K HH</td>
</tr>

</table>

><b>*</b>Microsoft recommended platform to use


## Related topics

[Adding devices to Windows Autopilot](add-devices.md)<br>
[Configuring device profiles](profiles.md)