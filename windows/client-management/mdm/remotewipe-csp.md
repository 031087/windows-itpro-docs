---
title: RemoteWipe CSP
description: RemoteWipe CSP
ms.assetid: 6e89bd37-7680-4940-8a67-11ed062ffb70
ms.author: maricia
ms.topic: article
ms.prod: w10
ms.technology: windows
author: MariciaAlforque
ms.date: 03/23/2018
---

# RemoteWipe CSP


The RemoteWipe configuration service provider can be used by mobile operators DM server or enterprise management server to remotely wipe a device. The RemoteWipe configuration service provider can make the data stored in memory and hard disks difficult to recover if the device is remotely wiped after being lost or stolen.

The following diagram shows the RemoteWipe configuration service provider management object in tree format as used by both OMA DM and OMA Client Provisioning. Enterprise IT Professionals can update these settings by using the Exchange Server.

![remotewipe csp (dm,cp)](images/provisioning-csp-remotewipe-dmandcp.png)

<a href="" id="dowipe"></a>**doWipe**  
Specifies that a remote wipe of the device should be performed. The return status code indicates whether the device accepted the Exec command.

When used with OMA Client Provisioning, a dummy value of "1" should be included for this element.

Supported operation is Exec.

<a href="" id="dowipepersistprovisioneddata"></a>**doWipePersistProvisionedData**  
Specifies that provisioning data should be backed up to a persistent location, and then a remote wipe of the device should be performed.

Supported operation is Exec.

When used with OMA Client Provisioning, a dummy value of "1" should be included for this element.

The information that was backed up will be restored and applied to the device when it resumes. The return status code shows whether the device accepted the Exec command.

<a href="" id="doWipeProtected"></a>**doWipeProtected**  
Added in Windows 10, version 1703. Exec on this node performs a remote wipe on the device and fully clean the internal drive. In some device configurations, this command may leave the device unable to boot. The return status code indicates whether the device accepted the Exec command.

The doWipeProtected is functionally similar to doWipe. But unlike doWipe, which can be easily circumvented by simply power cycling the device, doWipeProtected will keep trying to reset the device until it’s done.

Supported operation is Exec.

<a href="" id="doWipePersistUserData"></a>**doWipePersistUserData**  
Added in Windows 10, version 1709.  Exec on this node will perform a remote reset on the device and persist user accounts and data. The return status code shows whether the device accepted the Exec command.
 

## Related topics


[Configuration service provider reference](configuration-service-provider-reference.md)

 

 






