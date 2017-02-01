---
title: Customize Windows 10 Start with ICD and provisioning packages (Windows 10)
description: In Windows 10, you can use a provisioning package to deploy a customized Start layout to users.
ms.assetid: AC952899-86A0-42FC-9E3C-C25F45B1ACAC
keywords: ["Start layout", "start menu"]
ms.prod: w10
ms.mktglfcycl: manage
ms.sitesec: library
author: jdeckerMS
localizationpriority: medium
---

# Customize Windows 10 Start and taskbar with ICD and provisioning packages


**Applies to**

- Windows 10
- Windows 10 Mobile

**Looking for consumer information?**

-   [Customize the Start menu](https://go.microsoft.com/fwlink/p/?LinkId=623630)



In Windows 10 Pro, Windows 10 Mobile, Windows 10 Enterprise, and Windows 10 Education, version 170#, you can use a provisioning package that you create with Windows Imaging and Configuration Designer (ICD) tool to deploy a customized Start and taskbar layout to users. No reimaging is required, and the Start and taskbar layout can be updated simply by overwriting the .xml file that contains the layout. The provisioning package can be applied to a running device. This enables you to customize Start and taskbar layouts for different departments or organizations, with minimal management overhead.

>[!NOTE]
>Taskbar configuration is available starting in Windows 10, version 1607.
>
>Start and taskbar configuration are available for Windows 10 Pro in version 170#.

>[!IMPORTANT]
>If you use a provisioning package to configure the taskbar, your configuration will be reapplied each time the explorer.exe process restarts. If your configuration pins an app and the user unpins that app, the user's change will be overwritten the next time the configuration is applied. To apply a taskbar configuration and allow users to make changes that will persist, apply your configuration by using Group Policy.

**Before you begin**: [Customize and export Start layout](customize-and-export-start-layout.md) for desktop editions or [create a Start layout XML](start-layout-xml-mobile.md) for mobile.

## <a href="" id="bkmk-howstartscreencontrolworks"></a>How Start layout control works


Three features enable Start and taskbar layout control:

-   The **Export-StartLayout** cmdlet in Windows PowerShell exports a description of the current Start layout in .xml file format. 

    >[!NOTE]  
    >To import the layout of Start to a mounted Windows image, use the [Import-StartLayout](https://go.microsoft.com/fwlink/p/?LinkId=623707) cmdlet.

-    [You can modify the Start .xml file](configure-windows-10-taskbar.md) to include  `<CustomTaskbarLayoutCollection>` or create an .xml file just for the taskbar configuration.


-   In ICD, you use the **Start/StartLayout** setting to set the path to the .xml file that defines the Start and taskbar layout.

## <a href="" id="bkmk-domaingpodeployment"></a>Create a provisioning package that contains a customized Start layout


Use the [Imaging and Configuration Designer (ICD) tool](https://go.microsoft.com/fwlink/p/?LinkID=525483) included in the Windows Assessment and Deployment Kit (ADK) for Windows 10 to create a provisioning package that applies a customized Start and taskbar layout. [Install the ADK.](https://developer.microsoft.com/windows/hardware/windows-assessment-deployment-kit)

>[!IMPORTANT]
>When you build a provisioning package, you may include sensitive information in the project files and in the provisioning package (.ppkg) file. Although you have the option to encrypt the .ppkg file, project files are not encrypted. You should store the project files in a secure location and delete the project files when they are no longer needed.

1.  Open ICD (by default, %systemdrive%\\Program Files (x86)\\Windows Kits\\10\\Assessment and Deployment Kit\\Imaging and Configuration Designer\\x86\\ICD.exe).
<<<<<<< HEAD

=======
>>>>>>> refs/remotes/origin/rs2
2. Choose **Advanced provisioning**.

3.  Name your project, and click **Next**.

4.  Choose **All Windows desktop editions** and click **Next**.

5.  On **New project**, click **Finish**. The workspace for your package opens.

6.  Expand **Runtime settings** &gt; **Start**, and click **StartLayout**.

    >[!TIP]
    >If **Start** is not listed, check the type of settings you selected in step 4. You must create the project using settings for **All Windows desktop editions**.

7.  Specify the path and file name of the Start layout .xml that you created with the [Export-StartLayout](https://go.microsoft.com/fwlink/p/?LinkId=620879) cmdlet.

8.  On the **File** menu, select **Save.**

9.  On the **Export** menu, select **Provisioning package**.

10. Change **Owner** to **IT Admin**, which will set the precedence of this provisioning package higher than provisioning packages applied to this device from other sources, and then select **Next.**

11. Optional. In the **Provisioning package security** window, you can choose to encrypt the package and enable package signing.

    -   **Enable package encryption** - If you select this option, an auto-generated password will be shown on the screen.

    -   **Enable package signing** - If you select this option, you must select a valid certificate to use for signing the package. You can specify the certificate by clicking **Select...** and choosing the certificate you want to use to sign the package.

12. Click **Next** to specify the output location where you want the provisioning package to go when it's built. By default, Windows Imaging and Configuration Designer (ICD) uses the project folder as the output location.

    Optionally, you can click **Browse** to change the default output location.

13. Click **Next**.

14. Click **Build** to start building the package. The provisioning package doesn't take long to build. The project information is displayed in the build page and the progress bar indicates the build status.

    If you need to cancel the build, click **Cancel**. This cancels the current build process, closes the wizard, and takes you back to the **Customizations Page**.

15. If your build fails, an error message will show up that includes a link to the project folder. You can scan the logs to determine what caused the error. Once you fix the issue, try building the package again.

    If your build is successful, the name of the provisioning package, output directory, and project directory will be shown.

    -   If you choose, you can build the provisioning package again and pick a different path for the output package. To do this, click **Back** to change the output package name and path, and then click **Next** to start another build.
    -   If you are done, click **Finish** to close the wizard and go back to the **Customizations Page**.

16. Copy the provisioning package to the target device.

17. Double-click the ppkg file and allow it to install.

## Related topics

- [Manage Windows 10 Start and taskbar layout](windows-10-start-layout-options-and-policies.md)
- [Configure Windows 10 taskbar](configure-windows-10-taskbar.md)
- [Customize and export Start layout](customize-and-export-start-layout.md)
- [Start layout XML for desktop editions of Windows 10 (reference)](start-layout-xml-desktop.md)
- [Start layout XML for mobile editions of Windows 10 (reference)](start-layout-xml-mobile.md)
- [Customize Windows 10 Start and taskbar with Group Policy](customize-windows-10-start-screens-by-using-group-policy.md)
- [Customize Windows 10 Start and taskbar with mobile device management (MDM)](customize-windows-10-start-screens-by-using-mobile-device-management.md)

 

 





