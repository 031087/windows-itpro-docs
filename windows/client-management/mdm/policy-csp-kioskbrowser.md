---
title: Policy CSP - KioskBrowser
description: Policy CSP - KioskBrowser
ms.author: maricia
ms.topic: article
ms.prod: w10
ms.technology: windows
author: MariciaAlforque
ms.date: 04/11/2018
---

# Policy CSP - KioskBrowser


These policies currently only apply to Kiosk Browser app. Kiosk Browser is a Microsoft Store app, added in Windows 10 version 1803, that provides IT a way to customize the end user’s browsing experience to fulfill kiosk, signage, and shared device scenarios. Application developers can also create their own kiosk browser and read these policies using [NamedPolicy.GetPolicyFromPath(String, String) Method](https://docs.microsoft.com/en-us/uwp/api/windows.management.policies.namedpolicy.getpolicyfrompath#Windows_Management_Policies_NamedPolicy_GetPolicyFromPath_System_String_System_String_). 


<hr/>

<!--Policies-->
## KioskBrowser policies  

<dl>
  <dd>
    <a href="#kioskbrowser-blockedurlexceptions">KioskBrowser/BlockedUrlExceptions</a>
  </dd>
  <dd>
    <a href="#kioskbrowser-blockedurls">KioskBrowser/BlockedUrls</a>
  </dd>
  <dd>
    <a href="#kioskbrowser-defaulturl">KioskBrowser/DefaultURL</a>
  </dd>
  <dd>
    <a href="#kioskbrowser-enableendsessionbutton">KioskBrowser/EnableEndSessionButton</a>
  </dd>
  <dd>
    <a href="#kioskbrowser-enablehomebutton">KioskBrowser/EnableHomeButton</a>
  </dd>
  <dd>
    <a href="#kioskbrowser-enablenavigationbuttons">KioskBrowser/EnableNavigationButtons</a>
  </dd>
  <dd>
    <a href="#kioskbrowser-restartonidletime">KioskBrowser/RestartOnIdleTime</a>
  </dd>
</dl>


<hr/>

<!--Policy-->
<a href="" id="kioskbrowser-blockedurlexceptions"></a>**KioskBrowser/BlockedUrlExceptions**  

<!--SupportedSKUs-->
<table>
<tr>
	<th>Home</th>
	<th>Pro</th>
	<th>Business</th>
	<th>Enterprise</th>
	<th>Education</th>
	<th>Mobile</th>
	<th>Mobile Enterprise</th>
</tr>
<tr>
	<td><img src="images/crossmark.png" alt="cross mark" /></td>
	<td><img src="images/checkmark.png" alt="check mark" /><sup>4</sup></td>
	<td><img src="images/checkmark.png" alt="check mark" /><sup>4</sup></td>
	<td><img src="images/checkmark.png" alt="check mark" /><sup>4</sup></td>
	<td><img src="images/checkmark.png" alt="check mark" /><sup>4</sup></td>
	<td><img src="images/crossmark.png" alt="cross mark" /></td>
	<td><img src="images/crossmark.png" alt="cross mark" /></td>
</tr>
</table>

<!--/SupportedSKUs-->
<!--Scope-->
[Scope](./policy-configuration-service-provider.md#policy-scope):

> [!div class = "checklist"]
> * Device

<hr/>

<!--/Scope-->
<!--Description-->
Added in Windows 10, version 1803. List of exceptions to the blocked website URLs (with wildcard support). This is used to configure URLs kiosk browsers are allowed to navigate to, which are a subset of the blocked URLs.

> [!Note]  
> This policy only applies to the Kiosk Browser app in Microsoft Store.

<!--/Description-->
<!--/Policy-->

<hr/>

<!--Policy-->
<a href="" id="kioskbrowser-blockedurls"></a>**KioskBrowser/BlockedUrls**  

<!--SupportedSKUs-->
<table>
<tr>
	<th>Home</th>
	<th>Pro</th>
	<th>Business</th>
	<th>Enterprise</th>
	<th>Education</th>
	<th>Mobile</th>
	<th>Mobile Enterprise</th>
</tr>
<tr>
	<td><img src="images/crossmark.png" alt="cross mark" /></td>
	<td><img src="images/checkmark.png" alt="check mark" /><sup>4</sup></td>
	<td><img src="images/checkmark.png" alt="check mark" /><sup>4</sup></td>
	<td><img src="images/checkmark.png" alt="check mark" /><sup>4</sup></td>
	<td><img src="images/checkmark.png" alt="check mark" /><sup>4</sup></td>
	<td><img src="images/crossmark.png" alt="cross mark" /></td>
	<td><img src="images/crossmark.png" alt="cross mark" /></td>
</tr>
</table>

<!--/SupportedSKUs-->
<!--Scope-->
[Scope](./policy-configuration-service-provider.md#policy-scope):

> [!div class = "checklist"]
> * Device

<hr/>

<!--/Scope-->
<!--Description-->
Added in Windows 10, version 1803. List of blocked website URLs (with wildcard support). This is used to configure blocked URLs kiosk browsers cannot navigate to.

> [!Note]  
> This policy only applies to the Kiosk Browser app in Microsoft Store.

<!--/Description-->
<!--/Policy-->

<hr/>

<!--Policy-->
<a href="" id="kioskbrowser-defaulturl"></a>**KioskBrowser/DefaultURL**  

<!--SupportedSKUs-->
<table>
<tr>
	<th>Home</th>
	<th>Pro</th>
	<th>Business</th>
	<th>Enterprise</th>
	<th>Education</th>
	<th>Mobile</th>
	<th>Mobile Enterprise</th>
</tr>
<tr>
	<td><img src="images/crossmark.png" alt="cross mark" /></td>
	<td><img src="images/checkmark.png" alt="check mark" /><sup>4</sup></td>
	<td><img src="images/checkmark.png" alt="check mark" /><sup>4</sup></td>
	<td><img src="images/checkmark.png" alt="check mark" /><sup>4</sup></td>
	<td><img src="images/checkmark.png" alt="check mark" /><sup>4</sup></td>
	<td><img src="images/crossmark.png" alt="cross mark" /></td>
	<td><img src="images/crossmark.png" alt="cross mark" /></td>
</tr>
</table>

<!--/SupportedSKUs-->
<!--Scope-->
[Scope](./policy-configuration-service-provider.md#policy-scope):

> [!div class = "checklist"]
> * Device

<hr/>

<!--/Scope-->
<!--Description-->
Added in Windows 10, version 1803. Configures the default URL kiosk browsers to navigate on launch and restart.

> [!Note]  
> This policy only applies to the Kiosk Browser app in Microsoft Store.

<!--/Description-->
<!--/Policy-->

<hr/>

<!--Policy-->
<a href="" id="kioskbrowser-enableendsessionbutton"></a>**KioskBrowser/EnableEndSessionButton**  

<!--SupportedSKUs-->
<table>
<tr>
	<th>Home</th>
	<th>Pro</th>
	<th>Business</th>
	<th>Enterprise</th>
	<th>Education</th>
	<th>Mobile</th>
	<th>Mobile Enterprise</th>
</tr>
<tr>
	<td><img src="images/crossmark.png" alt="cross mark" /></td>
	<td><img src="images/checkmark.png" alt="check mark" /><sup>4</sup></td>
	<td><img src="images/checkmark.png" alt="check mark" /><sup>4</sup></td>
	<td><img src="images/checkmark.png" alt="check mark" /><sup>4</sup></td>
	<td><img src="images/checkmark.png" alt="check mark" /><sup>4</sup></td>
	<td><img src="images/crossmark.png" alt="cross mark" /></td>
	<td><img src="images/crossmark.png" alt="cross mark" /></td>
</tr>
</table>

<!--/SupportedSKUs-->
<!--Scope-->
[Scope](./policy-configuration-service-provider.md#policy-scope):

> [!div class = "checklist"]
> * Device

<hr/>

<!--/Scope-->
<!--Description-->
Shows the Kiosk Browser's end session button. When the policy is enabled, the Kiosk Browser app shows a button to reset the browser. When the user clicks on the button, the app will prompt the user for confirmation to end the session. When the user confirms, the Kiosk broswser will clear all browsing data (cache, cookies, etc.) and navigate back to the default URL.

<!--/Description-->
<!--SupportedValues-->

<!--/SupportedValues-->
<!--Example-->

<!--/Example-->
<!--Validation-->

<!--/Validation-->
<!--/Policy-->

<hr/>

<!--Policy-->
<a href="" id="kioskbrowser-enablehomebutton"></a>**KioskBrowser/EnableHomeButton**  

<!--SupportedSKUs-->
<table>
<tr>
	<th>Home</th>
	<th>Pro</th>
	<th>Business</th>
	<th>Enterprise</th>
	<th>Education</th>
	<th>Mobile</th>
	<th>Mobile Enterprise</th>
</tr>
<tr>
	<td><img src="images/crossmark.png" alt="cross mark" /></td>
	<td><img src="images/checkmark.png" alt="check mark" /><sup>4</sup></td>
	<td><img src="images/checkmark.png" alt="check mark" /><sup>4</sup></td>
	<td><img src="images/checkmark.png" alt="check mark" /><sup>4</sup></td>
	<td><img src="images/checkmark.png" alt="check mark" /><sup>4</sup></td>
	<td><img src="images/crossmark.png" alt="cross mark" /></td>
	<td><img src="images/crossmark.png" alt="cross mark" /></td>
</tr>
</table>

<!--/SupportedSKUs-->
<!--Scope-->
[Scope](./policy-configuration-service-provider.md#policy-scope):

> [!div class = "checklist"]
> * Device

<hr/>

<!--/Scope-->
<!--Description-->
Added in Windows 10, version 1803. Enable/disable kiosk browser's home button.

> [!Note]  
> This policy only applies to the Kiosk Browser app in Microsoft Store.

<!--/Description-->
<!--/Policy-->

<hr/>

<!--Policy-->
<a href="" id="kioskbrowser-enablenavigationbuttons"></a>**KioskBrowser/EnableNavigationButtons**  

<!--SupportedSKUs-->
<table>
<tr>
	<th>Home</th>
	<th>Pro</th>
	<th>Business</th>
	<th>Enterprise</th>
	<th>Education</th>
	<th>Mobile</th>
	<th>Mobile Enterprise</th>
</tr>
<tr>
	<td><img src="images/crossmark.png" alt="cross mark" /></td>
	<td><img src="images/checkmark.png" alt="check mark" /><sup>4</sup></td>
	<td><img src="images/checkmark.png" alt="check mark" /><sup>4</sup></td>
	<td><img src="images/checkmark.png" alt="check mark" /><sup>4</sup></td>
	<td><img src="images/checkmark.png" alt="check mark" /><sup>4</sup></td>
	<td><img src="images/crossmark.png" alt="cross mark" /></td>
	<td><img src="images/crossmark.png" alt="cross mark" /></td>
</tr>
</table>

<!--/SupportedSKUs-->
<!--Scope-->
[Scope](./policy-configuration-service-provider.md#policy-scope):

> [!div class = "checklist"]
> * Device

<hr/>

<!--/Scope-->
<!--Description-->
Added in Windows 10, version 1803. Enable/disable kiosk browser's navigation buttons (forward/back).

> [!Note]  
> This policy only applies to the Kiosk Browser app in Microsoft Store.

<!--/Description-->
<!--/Policy-->

<hr/>

<!--Policy-->
<a href="" id="kioskbrowser-restartonidletime"></a>**KioskBrowser/RestartOnIdleTime**  

<!--SupportedSKUs-->
<table>
<tr>
	<th>Home</th>
	<th>Pro</th>
	<th>Business</th>
	<th>Enterprise</th>
	<th>Education</th>
	<th>Mobile</th>
	<th>Mobile Enterprise</th>
</tr>
<tr>
	<td><img src="images/crossmark.png" alt="cross mark" /></td>
	<td><img src="images/checkmark.png" alt="check mark" /><sup>4</sup></td>
	<td><img src="images/checkmark.png" alt="check mark" /><sup>4</sup></td>
	<td><img src="images/checkmark.png" alt="check mark" /><sup>4</sup></td>
	<td><img src="images/checkmark.png" alt="check mark" /><sup>4</sup></td>
	<td><img src="images/crossmark.png" alt="cross mark" /></td>
	<td><img src="images/crossmark.png" alt="cross mark" /></td>
</tr>
</table>

<!--/SupportedSKUs-->
<!--Scope-->
[Scope](./policy-configuration-service-provider.md#policy-scope):

> [!div class = "checklist"]
> * Device

<hr/>

<!--/Scope-->
<!--Description-->
Added in Windows 10, version 1803. Amount of time in minutes the session is idle until the kiosk browser restarts in a fresh state.  

The value is an int 1-1440 that specifies the amount of minutes the session is idle until the kiosk browser restarts in a fresh state. The default value is empty which means there is no idle timeout within the kiosk browser.

> [!Note]  
> This policy only applies to the Kiosk Browser app in Microsoft Store.

<!--/Description-->
<!--/Policy-->
<hr/>

Footnote:

-   1 - Added in Windows 10, version 1607.
-   2 - Added in Windows 10, version 1703.
-   3 - Added in Windows 10, version 1709.
-   4 - Added in Windows 10, version 1803.

<!--/Policies-->

