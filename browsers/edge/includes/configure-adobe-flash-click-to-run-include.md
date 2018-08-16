<!-- ## Configure the Adobe Flash Click-to-Run setting -->
>*Supported versions: Microsoft Edge on Windows 10, version 1703 or later*<br> 
>*Default setting: Enabled or not configured (Does not load content automatically)*

[!INCLUDE [configure-adobe-flash-click-to-run-setting-shortdesc](../shortdesc/configure-adobe-flash-click-to-run-setting-shortdesc.md)]

### Supported values

|Group Policy  |MDM |Registry |Description |Most restricted |
|---|:---:|:---:|---|:---:|
|Disabled |0 |0 |Load and run Adobe Flash content automatically. | |
|Enabled or not configured<br>**(default)** |1 |1 |Do not load or run Adobe Flash content automatically. Requires action from the user.  |![Most restricted value](../images/check-gn.png) |
---

### ADMX info and settings

#### ADMX info
- **GP English name:** Configure the Adobe Flash Click-to-Run setting
- **GP name:**  AllowFlashClickToRun
- **GP path:** Windows Components/Microsoft Edge
- **GP ADMX file name:** MicrosoftEdge.admx

#### MDM settings
- **MDM name:** Browser/[AllowFlashClickToRun](https://docs.microsoft.com/en-us/windows/client-management/mdm/policy-csp-browser#browser-allowflashclicktorun)
- **Supported devices:** Desktop
- **URI full path:** ./Vendor/MSFT/Policy/Config/Browser/AllowFlashClickToRun 
- **Data type:** Integer

#### Registry settings
- **Path:** HKLM\\Software\\Policies\\Microsoft\\MicrosoftEdge\\Security
- **Value name:** FlashClickToRunMode
- **Value type:** REG_DWORD

<hr>