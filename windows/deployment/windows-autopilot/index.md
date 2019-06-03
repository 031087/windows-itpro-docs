---
title: Windows Autopilot deployment
description: Windows Autopilot deployment
keywords: mdm, setup, windows, windows 10, oobe, manage, deploy, autopilot, ztd, zero-touch, partner, msfb, intune
ms.reviewer: mniehaus
manager: laurawi
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


# Windows Autopilot deployment

**Applies to**

-   Windows 10

Windows Autopilot modernizes Windows deployment with a zero-touch, self-service process that runs immediately after powering on a new computer for the first time. With Windows Autopilot, and employee can receive a new device and configure it to be business-ready with just a few clicks.  

This guide is intended for use by an IT-specialist, system architect, or business decision maker. The guide provides an overview of how Windows Autopilot deployment works, including detailed requirements, deployment scenarios, and platform capabilities. The document highlights options that are available to you when planning a modern, cloud-joined Windows 10 deployment strategy. Before you read this guide, you should have a good understanding of your organizational requirements.

When you are ready to deploy client devices with Windows Autopilot, see the detailed configuration procedures documented for your chosen [platform](windows-autopilot-platforms.md) (recommended platform: [Intune](https://docs.microsoft.com/en-us/intune/enrollment-autopilot)).

## In this guide

The following topics are available in this guide:

### Understanding Windows Autopilot

<table>
<tr><td>[Overview of Windows Autopilot](windows-autopilot.md)<td>A review of Windows Autopilot is provided with a video walkthrough. Benefits and general requirements are discussed.<br>
<tr><td>[Requirements](windows-autopilot-requirements.md)<td> Detailed software, network, licensiing, and configuration requirments are provided.<br>
<tr><td>[What's new](windows-autopilot-whats-new.md)<td> Windows Autopilot is always being updated with new features! Read about the latest new capabilities here.<br>
<tr><td>[Platforms](windows-autopilot-platforms.md)<td> A summary of platforms available for registering Windows Autopilot devices.<br>
<tr><td>[Scenarios and Capabilities](windows-autopilot-scenarios.md)<td> A summary of Windows Autopilot deployment scenarios and capabilities.<br>
<tr><td>[Get started](demonstrate-deployment-on-vm.md)<td> Interested in trying out Autopilot? A step-by-step walkthrough is provided for testing Windows Autopilot on a virtual machine or physical device with a free 30-day trial premium Intune account. <br>
</table>

### Deployment scenarios

<table>
<tr><td>[User-driven mode](user-driven.md)<td> Requirements and validation steps for deploying a new Azure Active Directory (AAD) joined or hybrid AAD-joined Windows 10 device are provided.
<tr><td>[Self-deploying mode](self-deploying.md)<td>Requirements and validation steps for deploying a new Windows 10 device device with little to no user interaction are provided.
<tr><td>[Windows Autopilot Reset](windows-autopilot-reset.md)<td> Using Windows Autopilot Reset, a device can be restored to its original settings, taking it back to a business-ready state. Both local and remote reset scenarios are discussed.
<tr><td>[Windows Autopilot for white glove deployment](white-glove.md)<td> Requirements and procedures are described that enable additional policies and apps to be delivered to a Windows Autopilot device.
<tr><td>[Support for existing devices](existing-devices.md)<td> This topic describes how Windows Autopilot can be used to convert Windows 7 or Windows 8.1 domain-joined computers to AAD-joined computers running Windows 10.
</table>

### Using Windows Autopilot

<table>
<tr><td>[Registering devices](add-devices.md)<td> The process of registering a device with the Windows Autopilot deployment service is described.<br>
<tr><td>[Configuring device profiles](profiles.md)<td> The device profile settings that specifie its behavior when it is deployed are described.<br>
<tr><td>[Enrollment status page](enrollment-status.md)<td> Settings that are available on the Enrollment Status Page are described.<br>
<tr><td>[Bitlocker encryptions](bitlocker.md)<td> Available options for configuring BitLocker on Windows Autopilot devices are described.<br>
<tr><td>[Troubleshooting Windows Autopilot](troubleshooting.md)<td> Diagnotic event information and troubleshooting procedures are provided.<br>
<tr><td>[Known issues](known-issues.md)<td> A list of current known issues and solutions is provided.<br>
</table>

### Support topics

<table>
<tr><td>[FAQ](autopilot-faq.md)<td> Frequently asked questions on several topics are provided.<br>
<tr><td>[Support contacts](autopilot-support.md)<td> Support information is provided.<br>
<tr><td>[Registration authorization](registration-auth.md)<td> This article discusses how a CSP partner or OEM can obtain customer authorization to register Windows Autopilot devices.<br>
</table>

## Related topics

