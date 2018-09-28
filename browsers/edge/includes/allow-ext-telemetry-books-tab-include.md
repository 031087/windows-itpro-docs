---
author: shortpatti
ms.author: pashort
ms.date:  10/02/2018
ms.prod: edge
ms:topic: include
---

<!-- ## Allow extended telemetry for the Books tab -->
>*Supported versions: Microsoft Edge on Windows 10, version 1803 or later* 
>*Default setting:  Disabled or not configured (Gather and send only basic diagnostic data)*

[!INCLUDE [allow-extended-telemetry-for-books-tab-shortdesc](../shortdesc/allow-extended-telemetry-for-books-tab-shortdesc.md)]

### Supported values

|Group Policy  |MDM |Registry |Description |Most restricted |
|---|:---:|:---:|---|:---:|
|Disabled or not configured<br>**(default)** |0 |0 |Gather and send only basic diagnostic data. |![Most restricted value](../images/check-gn.png) |
|Enabled |1 |1 |Gather all diagnostic data. For this policy to work correctly, you must set the diagnostic data in _Settings > Diagnostics & feedback_ to **Full**. | |
---

### ADMX info and settings

#### ADMX info
- **GP English name:** Allow extended telemetry for the Books tab
- **GP name:** EnableExtendedBooksTelemetry
- **GP path:** Windows Components/Microsoft Edge
- **GP ADMX file name:** MicrosoftEdge.admx

#### MDM settings
- **MDM name:** [Browser/EnableExtendedBooksTelemetry](https://docs.microsoft.com/en-us/windows/client-management/mdm/policy-csp-browser#browser-enableextendedbookstelemetry)
- **Supported devices:** Desktop and Mobile
- **URI full path:** ./Vendor/MSFT/Policy/Config/Browser/EnableExtendedBooksTelemetry
- **Data type:** Integer

#### Registry settings
- **Path:** HKLM\\Software\\Policies\\Microsoft\\MicrosoftEdge\\BooksLibrary
- **Value name:** EnableExtendedBooksTelemetry
- **Value type:** REG_DWORD


<hr>
