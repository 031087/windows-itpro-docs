---
title: Demo the Windows AutoPilot Deployment Program on a Virtual Machine
description: Step-by-step instructions on how to set-up a Virtual Machine with a Windows AutoPilot deployment
keywords: mdm, setup, windows, windows 10, oobe, manage, deploy, autopilot, ztd, zero-touch, partner, msfb, intune
ms.prod: w10
ms.mktglfcycl: deploy
ms.localizationpriority: high
ms.sitesec: library
ms.pagetype: deploy
author: DaniHalfin
ms.author: daniha
ms.date: 12/13/2017
---

# Demo the Windows AutoPilot Deployment Program on a Virtual Machine

**Applies to**

-   Windows 10

In this topic you'll learn how to set-up a Windows AutoPilot deployment for a Virtual Machine using Hyper-V.

## Prerequisites

These are the thing you'll need on your device to get started:
* Installation media for the latest version of Windows 10 Professional or Enterprise (ISO file)
* Internet access (see [Network connectivity requirements](windows-10-autopilot.md#network-connectivity-requirements))
* Hypervisor needs to be unoccupied, or used by Hyper-V, as we will be using Hyper-V to create the Virtual Machine

See additional prerequisites in the [Windows AutoPilot overview topic](windows-10-autopilot.md#prerequisites).

## Create your Virtual Machine

### Enable Hyper-V
The first thing to do, is to enable the Hyper-V feature on your device.
>[!IMPORTANT]
>If you already have Hyper-V enabled, skip this step.

Open a PowerShell prompt **as an administrator** and run the following:
```powershell
Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Hyper-V -All
```

You will be prompted to restart your device, so save all your work and restart it before you continue.

### Create and start your demo Virtual Machine

Now that Hyper-V is enabled, proceed to create your Virtual Machine.

Open a PowerShell prompt **as an administrator** and run the following:
```powershell
New-VMSwitch -Name AutoPilotExternal -NetAdapterName <Name of Network Adapter with internet access> -AllowManagementOS $true
New-VM -Name WindowsAutoPilot -MemoryStartupBytes 2GB -BootDevice VHD -NewVHDPath .\VMs\WindowsAutoPilot.vhdx -Path .\VMData -NewVHDSizeBytes 80GB -Generation 2 -Switch AutoPilotExternal
Add-VMDvdDrive -Path <Path to Windows 10 ISO> -VMName WindowsAutoPilot
Start-VM -VMName WindowsAutoPilot
```

>[!IMPORTANT]
>Make sure to replace <*Name of Network Adapter with internet access*> and <*Path to Windows 10 ISO*> with the appropriate values.
>Additionally, note that all Virtual Machine related data will be created under the current path in your PowerShell prompt. Consider navigating into a new folder before running the above.

### Install Windows 10

Now that the Virtual Machine was created and started, open **Hyper-V Manager** and connect to the **WindowsAutoPilot** Virtual Machine.
Make sure the Virtual Machine booted from the installation media you've provided and complete the Windows installation process.

Once the installation is complete, create a checkpoint. You will create multiple checkpoints throughout this process, which you can later use to go through the process again.

To create the checkpoint, open a PowerShell prompt **as an administrator** and run the following:
```powershell
Checkpoint-VM -Name WindowsAutoPilot -SnapshotName "Finished Windows install"
```

## Capture your Virtual Machine's hardware ID

On the newly created Virtual Machine, open a PowerShell prompt **as an administrator** and run the following:
```powershell
md c:\HWID
Set-Location c:\HWID
Set-ExecutionPolicy Unrestricted
Install-Script -Name Get-WindowsAutoPilotInfo
Get-WindowsAutoPilotInfo.ps1 -OutputFile AutoPilotHWID.csv
```

>[!NOTE]
>Accept all prompts while running the above cmdlets.

### Mount the Virtual Hard Drive (VHD)

To gain access to the AutoPilotHWID.csv that contains the hardware ID, stop the Virtual Machine to unlock the Virtual Hard Drive. 

To do that, on your device (**not** on the Virtual Machine), open a PowerShell prompt **as an administrator** and run the following:
```powershell
Stop-VM -VMName WindowsAutoPilot
```

Once the Virtual Machine has stopped, create a checkpoint:
```powershell
Checkpoint-VM -Name WindowsAutoPilot -SnapshotName "HWID captured"
```

With the checkpoint created, continue to mount the VHD:
```powershell
Mount-VHD -path (Get-VMHardDiskDrive -VMName WindowsAutoPilot).Path
```

Once mounted, navigate to the new drive and copy **AutoPilotHWID.csv** to a location on your device.

Before you proceed, unmount the VHD to unlock it and start the Virtual Machine:
```powershell
Dismount-VHD -path (Get-VMHardDiskDrive -VMName WindowsAutoPilot).Path
Start-VM -VMName WindowsAutoPilot
```

## Reset Virtual Machine back to Out-Of-Box-Experience (OOBE)

With the hardware ID captured, prepare your Virtual Machine for Windows AutoPilot deployment by resetting it back to OOBE.

On the Virtual Machine, go to **Settings > Update & Security > Recovery** and click on **Get started** under **Reset this PC**.
Select **Remove everything** and **Just remove my files**. Finally, click on **Reset**.

![Reset this PC final prompt](images/autopilot-reset-prompt.jpg)

Resetting your Virtual Machine can take a while. Proceed to the next steps while your Virtual Machine is resetting.

![Reset this PC screen capture](images/autopilot-reset-progress.jpg)

## Configure company branding

>[!IMPORTANT]
>If you already have company branding configured in Azure Active Directory, you can skip this step.

Navigate to [Company branding in Azure Active Directory](https://portal.azure.com/#blade/Microsoft_AAD_IAM/ActiveDirectoryMenuBlade/LoginTenantBranding).

>[!IMPORTANT]
>Make sure to sign-in with a Global Administrator account.

Click on **Configure** and configure any type of company branding you'd like to see during the OOBE.

![Configure button in Company branding](images/autopilot-aad-configure.jpg)

Once finished, click **Save**.

>[!NOTE]
>Changes to company branding can take up to 30 minutes to apply.


## Configure Microsoft Intune auto-enrollment

>[!IMPORTANT]
>If you already have MDM auto-enrollment configured in Azure Active Directory, you can skip this step.

Navigate to [Mobility (MDM and MAM) in Azure Active Directory](https://portal.azure.com/#blade/Microsoft_AAD_IAM/ActiveDirectoryMenuBlade/Mobility) and select **Microsoft Intune**.

For the purposes of this demo, select **All** under the **MDM user scope** and click **Save**.

![MDM user scope in the Mobility blade](images/autopilot-aad-mdm.jpg)

## Register your Virtual Machine to your organization

Navigate to [Microsoft Store for Business device management](https://businessstore.microsoft.com/en-us/manage/devices). Click on **Add devices** and select the **AutoPilotHWID.csv** you've saved earlier. A message will appear indicating your request is being processed. Wait a few moments before refreshing to see your Virtual Machine added.

![Add devices through Microsoft Store for Business](images/autopilot-devices-add.jpg)

## Create and assign a Windows AutoPilot deployment profile

Navigate to [Windows enrollment in Microsoft Intune](https://portal.azure.com/#blade/Microsoft_Intune_Enrollment/OverviewBlade/windowsEnrollment).

Make sure to sync the device you've just registered, by clicking on **Devices** under **Windows Autopilot Deployment Program (Preview)** and selecting **Sync**. Wait a few moments before refreshing to see your Virtual Machine added.

![Microsoft Intune sync Windows devices](images/autopilot-intune-sync.jpg)

### Create a Windows AutoPilot deployment profile

Click on **Deployment profiles** under **Windows Autopilot Deployment Program (Preview)** and select **Create profile**.

![Microsoft Intune create deployment profile](images/autopilot-intune-profile-add.jpg)

In the **Create profile** blade, set the name to **AutoPilot Intune Demo**, click on **Out-of-box experience (OOBE)** and configure the following:
| Setting name | Value |
|---|---|
|Privacy Settings|Hide|
|End user license agreement (EULA)|Hide|
|User account type|Standard|

Click on **Save** and **Create**.

![Create a new deployment profile in Microsoft Intune](images/autopilot-intune-profile-configure.jpg)

### Assign a Windows AutoPilot deployment profile

With the deployment profile created, go back to **Devices** under **Windows Autopilot Deployment Program (Preview)** and select your Virtual Machine. Click on **Assign profile** and in the **Assign Profile** blade select **AutoPilot Intune Demo** under the **AutoPilot profile**. Click on **Assign**.

![Assign AutoPilot Profile in Microsoft Intune](images/autopilot-intune-profile-assign.jpg)

Wait a few minutes for all changes to apply.

## See Windows AutoPilot in action

By now, your Virtual Machine should be back to OOBE. Make sure to wait at least 30 minutes from the time you've [configured company branding](#configure-company-branding)
, otherwise those changes might not show up.

Once you select a language and a keyboard layout, your company branded sign-in screen should appear. Provide your Azure Active Directory credentials and you're all done.

![OOBE sign-in page](images/autopilot-oobe.jpg)

Windows AutoPilot will now take over to automatically join your Virtual Machine into Azure Active Directory and enroll it to Microsoft Intune. Use the checkpoints you've created to go through this process again with different settings.

