---
title: Implement Windows Hello in your organization (Windows 10)
description: You can create a Group Policy or mobile device management (MDM) policy that will implement Windows Hello for Business on devices running Windows 10.
ms.assetid: 47B55221-24BE-482D-BD31-C78B22AC06D8
keywords: identity, PIN, biometric, Hello
ms.prod: w10
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
author: jdeckerMS
localizationpriority: high
---

# Implement Windows Hello for Business in your organization

**Applies to**
-   Windows 10
-   Windows 10 Mobile

You can create a Group Policy or mobile device management (MDM) policy that will implement Windows Hello on devices running Windows 10.

>[!IMPORTANT]
>The Group Policy setting **Turn on PIN sign-in** does not apply to Windows Hello for Business. It still prevents or enables the creation of a convenience PIN for Windows 10, version 1507 and 1511. 
>
>Beginning in version 1607, Windows Hello as a convenience PIN is disabled by default on all domain-joined computers. To enable a convenience PIN for Windows 10, version 1607, enable the Group Policy setting **Turn on convenience PIN sign-in**. 
>
>Use **Windows Hello for Business** policy settings to manage PINs for Windows Hello for Business.
 
## Group Policy settings for Windows Hello for Business

The following table lists the Group Policy settings that you can configure for Hello use in your workplace. These policy settings are available in both **User configuration** and **Computer Configuration** under **Policies** &gt; **Administrative Templates** &gt; **Windows Components** &gt; **Windows Hello for Business**.


<table>
<tr>
<th colspan="2">Policy</th>
<th>Options</th>
</tr>
<tr>
<td>Use Windows Hello for Business</td>
<td></td>
<td>
<p><b>Not configured</b>: Users can provision Windows Hello for Business, which encrypts their domain password.</p>
<p><b>Enabled</b>: Device provisions Windows Hello for Business using keys or certificates for all users.</p>
<p><b>Disabled</b>: Device does not provision Windows Hello for Business for any user.</p>
</td>
</tr>
<tr>
<td>Use a hardware security device</td>
<td></td>
<td>
<p><b>Not configured</b>: Windows Hello for Business will be provisioned using TPM if available, and will be provisioned using software if TPM is not available.</p>
<p><b>Enabled</b>: Windows Hello for Business will only be provisioned using TPM.</p>
<p><b>Disabled</b>: Windows Hello for Business will be provisioned using TPM if available, and will be provisioned using software if TPM is not available.</p>
</td>
</tr>
<tr>
<td>Use biometrics</td>
<td></td>
<td>
<p><b>Not configured</b>: Biometrics can be used as a gesture in place of a PIN.</p>
<p><b>Enabled</b>: Biometrics can be used as a gesture in place of a PIN.</p>
<p><b>Disabled</b>: Only a PIN can be used as a gesture.</p>
</td>
</tr>
<tr>
<td rowspan="8">PIN Complexity</td>
<td>Require digits</td>
<td>
<p><b>Not configured</b>: Users must include a digit in their PIN.</p>
<p><b>Enabled</b>: Users must include a digit in their PIN.</p>
<p><b>Disabled</b>: Users cannot use digits in their PIN.</p>
</td>
</tr>
<tr>
<td>Require lowercase letters</td>
<td>
<p><b>Not configured</b>: Users cannot use lowercase letters in their PIN.</p>
<p><b>Enabled</b>: Users must include at least one lowercase letter in their PIN.</p>
<p><b>Disabled</b>: Users cannot use lowercase letters in their PIN.</p>
</td>
</tr>
<tr>
<td>Maximum PIN length</td>
<td>
<p><b>Not configured</b>: PIN length must be less than or equal to 127.</p>
<p><b>Enabled</b>: PIN length must be less than or equal to the number you specify.</p>
<p><b>Disabled</b>: PIN length must be less than or equal to 127.</p>
</td>
</tr>
<tr>
<td>Minimum PIN length</td>
<td>
<p><b>Not configured</b>: PIN length must be greater  than or equal to 4.</p>
<p><b>Enabled</b>: PIN length must be greater than or equal to the number you specify.</p>
<p><b>Disabled</b>: PIN length must be greater  than or equal to 4.</p>
</td>
</tr>
<tr>
<td>Expiration</td>
<td>
<p><b>Not configured</b>: PIN does not expire.</p>
<p><b>Enabled</b>: PIN can be set to expire after any number of days between 1 and 730, or PIN can be set to never expire by setting policy to 0.</p>
<p><b>Disabled</b>: PIN does not expire.</p>
</td>
</tr>
<tr>
<td>History</td>
<td>
<p><b>Not configured</b>: Previous PINs are not stored.</p>
<p><b>Enabled</b>: Specify the number of previous PINs that can be associated to a user account that can't be reused.</p>
<p><b>Disabled</b>: Previous PINs are not stored.</p>
<div class="alert"><b>Note</b>  Current PIN is included in PIN history.</div>
<div> </div>
</td>
</tr>
<tr>
<td>Require special characters</td>
<td>
<p><b>Not configured</b>: Users cannot include a special character in their PIN.</p>
<p><b>Enabled</b>: Users must include at least one special character in their PIN.</p>
<p><b>Disabled</b>: Users cannot include a special character in their PIN.</p>
</td>
</tr>
<tr>
<td>Require uppercase letters</td>
<td>
<p><b>Not configured</b>: Users cannot include an uppercase letter in their PIN.</p>
<p><b>Enabled</b>: Users must include at least one uppercase letter in their PIN.</p>
<p><b>Disabled</b>: Users cannot include an uppercase letter in their PIN.</p>
</td>
</tr>
<tr>
<td><a href="prepare-people-to-use-microsoft-passport.md#bmk-remote">Phone Sign-in</a></td>
<td>
<p>Use Phone Sign-in</p>
<div class="alert"><b>Note</b>  Applies to desktop only. Phone sign-in is currently limited to select Technology Adoption Program (TAP) participants.</div>
<div> </div>
</td>
<td>
<p><b>Not configured</b>: Phone sign-in is disabled.</p>
<p><b>Enabled</b>: Users can use a portable, registered device as a companion device for desktop authentication.</p>
<p><b>Disabled</b>: Phone sign-in is disabled.</p>
</td>
</tr>
</table>

## MDM policy settings for Windows Hello for Business

The following table lists the MDM policy settings that you can configure for Windows Hello for Business use in your workplace. These MDM policy settings use the [PassportForWork configuration service provider (CSP)](https://go.microsoft.com/fwlink/p/?LinkId=692070).

>[!IMPORTANT]
>Starting in Windows 10, version 1607, all devices only have one PIN associated with Windows Hello for Business. This means that any PIN on a device will be subject to the policies specified in the PassportForWork CSP. The values specified take precedence over any complexity rules set via Exchange ActiveSync (EAS) or the DeviceLock CSP. 

<table>
<tr>
<th colspan="2">Policy</th>
<th>Scope</th>
<th>Default</th>
<th>Options</th>
</tr>
<tr>
<td>UsePassportForWork</td>
<td></td>
<td>Device</td>
<td>True</td>
<td>
<p>True: Windows Hello for Business will be provisioned for all users on the device.</p>
<p>False: Users will not be able to provision Windows Hello for Business. </p>
<div class="alert"><b>Note</b>  If Windows Hello for Business is enabled, and then the policy is changed to False, users who previously set up Windows Hello for Business can continue to use it, but will not be able to set up Windows Hello for Business on other devices.</div>
<div> </div>
</td>
</tr>
<tr>
<td>RequireSecurityDevice</td>
<td></td>
<td>Device</td>
<td>False</td>
<td>
<p>True: Windows Hello for Business will only be provisioned using TPM.</p>
<p>False: Windows Hello for Business will be provisioned using TPM if available, and will be provisioned using software if TPM is not available.</p>
</td>
</tr>
<tr>
<td rowspan="2">Biometrics</td>
<td>
<p>UseBiometrics</p>
</td>
<td>Device </td>
<td>False</td>
<td>
<p>True: Biometrics can be used as a gesture in place of a PIN for domain sign-in.</p>
<p>False: Only a PIN can be used as a gesture for domain sign-in.</p>
</td>
</tr>
<tr>
<td>
<p>FacialFeaturesUser</p>
<p>EnhancedAntiSpoofing</p>
</td>
<td>Device</td>
<td>Not configured</td>
<td>
<p>Not configured: users can choose whether to turn on enhanced anti-spoofing.</p>
<p>True: Enhanced anti-spoofing is required on devices which support it.</p>
<p>False: Users cannot turn on enhanced anti-spoofing.</p>
</td>
</tr>
<tr>
<td rowspan="9">PINComplexity</td>
</tr>
<tr>
<td>Digits </td>
<td>Device or user</td>
<td>2 </td>
<td>
<p>1: Numbers are not allowed. </p>
<p>2: At least one number is required.</p>
</td>
</tr>
<tr>
<td>Lowercase letters </td>
<td>Device or user</td>
<td>1 </td>
<td>
<p>1: Lowercase letters are not allowed. </p>
<p>2: At least one lowercase letter is required.</p>
</td>
</tr>
<tr>
<td>Maximum PIN length </td>
<td>Device or user</td>
<td>127 </td>
<td>
<p>Maximum length that can be set is 127. Maximum length cannot be less than minimum setting.</p>
</td>
</tr>
<tr>
<td>Minimum PIN length</td>
<td>Device or user</td>
<td>4</td>
<td>
<p>Minimum length that can be set is 4. Minimum length cannot be greater than maximum setting.</p>
</td>
</tr>
<tr>
<td>Expiration </td>
<td>Device or user</td>
<td>0</td>
<td>
<p>Integer value specifies the period of time (in days) that a PIN can be used before the system requires the user to change it. The largest number you can configure for this policy setting is 730. The lowest number you can configure for this policy setting is 0. If this policy is set to 0, then the user’s PIN will never expire. 
</p>
</td>
</tr>
<tr>
<td>History</td>
<td>Device or user</td>
<td>0</td>
<td>
<p>Integer value that specifies the number of past PINs that can be associated to a user account that can’t be reused. The largest number you can configure for this policy setting is 50. The lowest number you can configure for this policy setting is 0. If this policy is set to 0, then storage of previous PINs is not required. 
</p>
</td>
</tr>
<tr>
<td>Special characters</td>
<td>Device or user</td>
<td>1</td>
<td>
<p>1: Special characters are not allowed. </p>
<p>2: At least one special character is required.</p>
</td>
</tr>
<tr>
<td>Uppercase letters</td>
<td>Device or user</td>
<td>1</td>
<td>
<p>1: Uppercase letters are not allowed. </p>
<p>2: At least one uppercase letter is required</p>
</td>
</tr>
<tr>
<td>Remote</td>
<td>
<p>UseRemotePassport</p>
<div class="alert"><b>Note</b>  Applies to desktop only. Phone sign-in is currently limited to select Technology Adoption Program (TAP) participants.</div>
<div> </div>
</td>
<td>Device or user</td>
<td>False</td>
<td>
<p>True: <a href="prepare-people-to-use-microsoft-passport.md#bmk-remote">Phone sign-in</a> is enabled.</p>
<p>False: <a href="prepare-people-to-use-microsoft-passport.md#bmk-remote">Phone sign-in</a> is disabled.</p>
</td>
</tr>
</table>

>[!NOTE]  
> If policy is not configured to explicitly require letters or special characters, users will be restricted to creating a numeric PIN.
 
## Prerequisites

You’ll need this software to set Windows Hello for Business policies in your enterprise.
<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Windows Hello for Business mode</th>
<th align="left">Azure AD</th>
<th align="left">Azure AD/AD hybrid (available with production release of Windows Server 2016)</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left">Key-based authentication</td>
<td align="left">[Azure AD subscription](https://docs.microsoft.com/azure/active-directory/active-directory-howto-tenant)</td>
<td align="left"><ul>
<li>[Azure AD subscription](https://docs.microsoft.com/azure/active-directory/active-directory-howto-tenant)</li>
<li>[Azure AD Connect](https://docs.microsoft.com/azure/active-directory/active-directory-aadconnect)</li>
<li>A few Windows Server 2016 domain controllers on-site</li>
<li>A management solution, such as [Configuration Manager](https://docs.microsoft.com/sccm/index), Group Policy, or MDM</li>
<li>[Active Directory Certificate Services](https://technet.microsoft.com/windowsserver/dd448615.aspx) (AD CS) without Network Device Enrollment Service (NDES)</li>
</ul></td>
</tr>
<tr class="even">
<td align="left">Certificate-based authentication</td>
<td align="left"><ul>
<li>[Azure AD subscription](https://docs.microsoft.com/azure/active-directory/active-directory-howto-tenant)</li>
<li>Intune or non-Microsoft mobile device management (MDM) solution</li>
<li>[PKI infrastructure](https://msdn.microsoft.com/library/windows/desktop/bb427432(v=vs.85).aspx)</li>
</ul></td>
<td align="left"><ul>
<li>[Azure AD subscription](https://docs.microsoft.com/azure/active-directory/active-directory-howto-tenant)</li>
<li>[Azure AD Connect](https://docs.microsoft.com/azure/active-directory/active-directory-aadconnect)</li>
<li>[AD CS](https://technet.microsoft.com/windowsserver/dd448615.aspx) with NDES</li>
<li>[Configuration Manager](https://docs.microsoft.com/sccm/index) for domain-joined certificate enrollment, or [InTune](https://docs.microsoft.com/intune/deploy-use/control-microsoft-passport-settings-on-devices-with-microsoft-intune) for non-domain-joined devices, or a non-Microsoft MDM service that supports Hello for Business</li>
</ul></td>
</tr>
</tbody>
</table>
 
Configuration Manager and MDM provide the ability to manage Windows Hello for Business policy and to deploy and manage certificates protected by Windows Hello for Business.

Azure AD provides the ability to register devices with your enterprise and to provision Windows Hello for Business for organization accounts.

[Learn more about enabling Windows Hello for Business in an Azure AD/AD hybrid environment.](https://docs.microsoft.com/azure/active-directory/active-directory-azureadjoin-passport-deployment)


## Windows Hello for BYOD

Windows Hello can be managed on personal devices that your employees use for work purposes using MDM. On personal devices, users can create a personal Windows Hello PIN for unlocking the device and used this PIN for access to work resources.

The PIN is managed using the same Windows Hello for Business policies that you can use to manage Windows Hello for Business on organization-owned devices. The PIN can also be managed using DeviceLock policy. DeviceLock policy can be used to control length, complexity, history, and expiration requirements and can be configured using the [Policy configuration service provider](https://go.microsoft.com/fwlink/p/?LinkID=623244).

## Related topics

[Windows Hello biometrics in the enterprise](windows-hello-in-enterprise.md)

[Why a PIN is better than a password](why-a-pin-is-better-than-a-password.md)

[Manage identity verification using Windows Hello for Business](manage-identity-verification-using-microsoft-passport.md)

[Enable phone sign-in to PC or VPN](enable-phone-signin-to-pc-and-vpn.md) 

[Prepare people to use Windows Hello](prepare-people-to-use-microsoft-passport.md)

[Windows Hello and password changes](microsoft-passport-and-password-changes.md)

[Windows Hello errors during PIN creation](microsoft-passport-errors-during-pin-creation.md)

[Event ID 300 - Windows Hello successfully created](passport-event-300.md)

[Windows Hello biometrics in the enterprise](windows-hello-in-enterprise.md)
 