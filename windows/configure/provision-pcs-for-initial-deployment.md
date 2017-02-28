---
title: Provision PCs with common settings (Windows 10)
description: Create a provisioning package to apply common settings to a PC running Windows 10. 
ms.assetid: 66D14E97-E116-4218-8924-E2A326C9367E
keywords: ["runtime provisioning", "provisioning package"]
ms.prod: W10
ms.mktglfcycl: deploy
ms.sitesec: library
author: jdeckerMS
localizationpriority: high
---

# Provision PCs with common settings for initial deployment (simple provisioning)


**Applies to**

-   Windows 10

This topic explains how to create and apply a simple provisioning package that contains common enterprise settings to a device running all desktop editions of Windows 10 except Windows 10 Home.

You can apply a provisioning package on a USB drive to off-the-shelf devices during setup, making it fast and easy to configure new devices. 

## Advantages
-   You can configure new devices without reimaging.

-   Works on both mobile and desktop devices.

-   No network connectivity required.

-   Simple to apply.

[Learn more about the benefits and uses of provisioning packages.](provisioning-packages.md)

## What does simple provisioning do?

In a simple provisioning package, you can configure:

- Device name
- Upgraded product edition
- Configure the device for shared use
- Remove pre-installed software
- Wi-Fi network 
- Active Directory or Azure Active Directory enrollment
- Local administrator account 
- Add applications and certificates

Provisioning packages can include management instructions and policies, installation of specific apps, customization of network connections and policies, and more. 

> [!TIP]
> Use simple provisioning to create a package with the common settings, then switch to the advanced editor to add other settings, apps, policies, etc.

![open advanced editor](images/icd-simple-edit.png)

## Create the provisioning package

Use the Windows Imaging and Configuration Designer (ICD) tool included in the Windows Assessment and Deployment Kit (ADK) for Windows 10 to create a provisioning package. [Install the ADK and select **Configuration Designer**.](https://developer.microsoft.com/windows/hardware/windows-assessment-deployment-kit)

1. Open Windows ICD (by default, %windir%\Program Files (x86)\Windows Kits\10\Assessment and Deployment Kit\Imaging and Configuration Designer\x86\ICD.exe).

2. Click **Simple provisioning**.

  ![ICD start options](images/icdstart-option.png)   

3. Name your project and click **Finish**. The screens for simple provisioning will walk you through the following steps.

  ![ICD simple provisioning](images/icd-simple.png)

4. In the **Set up device** step, enter a unique 15-character name for the device. For help generating a unique name, you can use %SERIAL%, which includes a hardware-specific serial number, or you can use %RAND:x%, which generates random characters of x length.

5. (*Optional*) You can upgrade the following editions of Windows 10 by providing a product key for the edition to upgrade to.
    - Pro to Education
    - Pro to Enterprise
    - Enterprise to Education
   
6. Click **Set up network**.

7. Toggle **On** or **Off** for wireless network connectivity. If you select **On**, enter the SSID, type, and (if required) password for the wireless network.

8. Click **Enroll into Active Directory**.

9. Toggle **Yes** or **No** for Active Directory enrollment. If you select **Yes**, enter the credentials for an account with permissions to enroll the device. (*Optional*) Enter a user name and password to create a local administrator account.

    > **Warning**: If you don't create a local administrator account and the device fails to enroll in Active Directory for any reason, you will have to reimage the device and start over. As a best practice, we recommend:
      - Use a least-privileged domain account to join the device to the domain.
      - Create a temporary administrator account to use for debugging or reprovisioning if the device fails to enroll successfully.
      - [Use Group Policy to delete the temporary administrator account](https://blogs.technet.microsoft.com/canitpro/2014/12/10/group-policy-creating-a-standard-local-admin-account/) after the device is enrolled in Active Directory.

10. Click **Finish**.

11. Review your settings in the summary. You can return to previous pages to change your selections. Then, under **Protect your package**, toggle **Yes** or **No** to encrypt the provisioning package. If you select **Yes**, enter a password. This password must be entered to apply the encrypted provisioning package.

12. Click **Create**.

> [!IMPORTANT]
> When you build a provisioning package, you may include sensitive information in the project files and in the provisioning package (.ppkg) file. Although you have the option to encrypt the .ppkg file, project files are not encrypted. You should store the project files in a secure location and delete the project files when they are no longer needed.


 **Next step**: [How to apply a provisioning package](provisioning-apply-package.md)   


## Learn more

-   Watch the video: [Provisioning Windows 10 Devices with New Tools](https://go.microsoft.com/fwlink/p/?LinkId=615921)

-   Watch the video: [Windows 10 for Mobile Devices: Provisioning Is Not Imaging](https://go.microsoft.com/fwlink/p/?LinkId=615922)

 
## Related topics

- [Provisioning packages for Windows 10](provisioning-packages.md)
- [How provisioning works in Windows 10](provisioning-how-it-works.md)
- [Install Windows Configuration Designer](provisioning-install-icd.md)
- [Create a provisioning package](provisioning-create-package.md)
- [Apply a provisioning package](provisioning-apply-package.md)
- [Settings changed when you uninstall a provisioning package](provisioning-uninstall-package.md)
- [Use a script to install a desktop app in provisioning packages](provisioning-script-to-install-app.md)
- [NFC-based device provisioning](provisioning-nfc.md)
- [Windows Configuration Designer command-line interface (reference)](provisioning-command-line.md)
- [Create a provisioning package with multivariant settings](provisioning-multivariant.md)





