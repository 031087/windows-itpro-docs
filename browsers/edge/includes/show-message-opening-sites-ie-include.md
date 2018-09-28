---
author: shortpatti
ms.author: pashort
ms.date:  10/02/2018
ms.prod: edge
ms:topic: include
---

<!-- ## Show message when opening sites in Internet Explorer --> 

>*Supported versions: Microsoft Edge on Windows 10, version 1607 and later*<br> 
>*Default setting:  Disabled or not configured (No additional message)*

<!-- RS5 update: add option for showing interstitial page with stay in Edge link (Koch) -->
[!INCLUDE [show-message-when-opening-sites-in-ie-shortdesc](../shortdesc/show-message-when-opening-sites-in-ie-shortdesc.md)]


Microsoft Edge does not show a notification before opening sites in Internet Explorer 11. However, with this policy, you can configure Microsoft Edge to display a notification before a site opens in IE11 or let users continue in Microsoft Edge.  If you want users to continue in Microsoft Edge, enable this policy to show the _Keep going in Microsoft Edge_ link in the notification. For this policy to work correctly, you must also enable the Configure the Enterprise Mode Site List or Send all intranet sites to Internet Explorer 11, or both.

### Supported values

|Group Policy  |MDM |Registry |Description |Most restricted |
|---|:---:|:---:|---|:---:|
|Disabled or not configured<br>**(default)** |0 |0 |No additional message displays. |![Most restricted value](../images/check-gn.png) |
|Enabled |1 |1 |Show an additional message stating that a site has opened in IE11. | |
|Enabled |2 |2 |Show an additional message with a _Keep going in Microsoft Edge_ link to allow users to open the site in Microsoft Edge. | |
---

### ADMX info and settings
#### ADMX info 
- **GP English name:** Show message when opening sites in Internet Explorer 
- **GP name:** ShowMessageWhenOpeningSitesInInternetExplorer
- **GP path:** Windows Components/Microsoft Edge
- **GP ADMX file name:** MicrosoftEdge.admx

#### MDM settings
- **MDM name:** Browser/[ShowMessageWhenOpeningSitesInInternetExplorer](https://docs.microsoft.com/en-us/windows/client-management/mdm/policy-csp-browser#browser-showmessagewhenopeningsitesininternetexplorer)
- **Supported devices:** Desktop
- **URI full path:** ./Vendor/MSFT/Policy/Config/Browser/ShowMessageWhenOpeningSitesInInternetExplorer
- **Data type:** Integer

#### Registry settings
- **Path:** HKLM\Software\Policies\Microsoft\MicrosoftEdge\Main
- **Value name:** ShowMessageWhenOpeningSitesInInternetExplorer
- **Value type:** REG_DWORD

### Related policies

- [Configure the Enterprise Mode Site List](../available-policies.md#configure-the-enterprise-mode-site-list): [!INCLUDE [configure-enterprise-mode-site-list-shortdesc](../shortdesc/configure-enterprise-mode-site-list-shortdesc.md)] 

- [Send all intranet sites to Internet Explorer 11](../available-policies.md#send-all-intranet-sites-to-internet-explorer-11): [!INCLUDE [send-all-intranet-sites-to-ie-shortdesc](../shortdesc/send-all-intranet-sites-to-ie-shortdesc.md)]


<hr>