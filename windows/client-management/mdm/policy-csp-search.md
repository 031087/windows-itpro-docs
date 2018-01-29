---
title: Policy CSP - Search
description: Policy CSP - Search
ms.author: maricia
ms.topic: article
ms.prod: w10
ms.technology: windows
author: nickbrower
ms.date: 01/29/2018
---

# Policy CSP - Search

> [!WARNING]
> Some information relates to prereleased product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.


<hr/>

<!--StartPolicies-->
## Search policies  

<dl>
  <dd>
    <a href="#search-allowcloudsearch">Search/AllowCloudSearch</a>
  </dd>
  <dd>
    <a href="#search-allowcortanainaad">Search/AllowCortanaInAAD</a>
  </dd>
  <dd>
    <a href="#search-allowindexingencryptedstoresoritems">Search/AllowIndexingEncryptedStoresOrItems</a>
  </dd>
  <dd>
    <a href="#search-allowsearchtouselocation">Search/AllowSearchToUseLocation</a>
  </dd>
  <dd>
    <a href="#search-allowstoringimagesfromvisionsearch">Search/AllowStoringImagesFromVisionSearch</a>
  </dd>
  <dd>
    <a href="#search-allowusingdiacritics">Search/AllowUsingDiacritics</a>
  </dd>
  <dd>
    <a href="#search-allowwindowsindexer">Search/AllowWindowsIndexer</a>
  </dd>
  <dd>
    <a href="#search-alwaysuseautolangdetection">Search/AlwaysUseAutoLangDetection</a>
  </dd>
  <dd>
    <a href="#search-disablebackoff">Search/DisableBackoff</a>
  </dd>
  <dd>
    <a href="#search-disableremovabledriveindexing">Search/DisableRemovableDriveIndexing</a>
  </dd>
  <dd>
    <a href="#search-donotusewebresults">Search/DoNotUseWebResults</a>
  </dd>
  <dd>
    <a href="#search-preventindexinglowdiskspacemb">Search/PreventIndexingLowDiskSpaceMB</a>
  </dd>
  <dd>
    <a href="#search-preventremotequeries">Search/PreventRemoteQueries</a>
  </dd>
  <dd>
    <a href="#search-safesearchpermissions">Search/SafeSearchPermissions</a>
  </dd>
</dl>


<hr/>

<!--StartPolicy-->
<a href="" id="search-allowcloudsearch"></a>**Search/AllowCloudSearch**  

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
	<td><img src="images/checkmark.png" alt="check mark" /><sup>3</sup></td>
	<td><img src="images/checkmark.png" alt="check mark" /><sup>3</sup></td>
	<td><img src="images/checkmark.png" alt="check mark" /><sup>3</sup></td>
	<td><img src="images/checkmark.png" alt="check mark" /><sup>3</sup></td>
	<td><img src="images/checkmark.png" alt="check mark" /><sup>3</sup></td>
	<td><img src="images/checkmark.png" alt="check mark" /><sup>3</sup></td>
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
Added in Windows 10, version 1709. Allow search and Cortana to search cloud sources like OneDrive and SharePoint. This policy allows corporate administrators to control whether employees can turn off/on the search of these cloud sources. The default policy value is to allow employees access to the setting that controls search of cloud sources.

The following list shows the supported values:

-   0 – Not allowed.
-   1 (default) – Allowed.

<!--/Description-->
<!--EndPolicy-->

<hr/>

<!--StartPolicy-->
<a href="" id="search-allowcortanainaad"></a>**Search/AllowCortanaInAAD**  

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
Added in Windows 10, next major update. This specifies whether the Cortana consent page can appear in the Azure Active Directory (AAD) device out-of-box-experience (OOBE) flow. If this policy is left in its default state, Cortana will not be shown in the AAD OOBE flow. If you opt-in to this policy, then the Cortana consent page will appear in the AAD OOBE flow..

<!--/Description-->
<!--SupportedValues-->
The following list shows the supported values:

-   0 (default) - Not allowed. The Cortana consent page will not appear in AAD OOBE during setup.
-   1 - Allowed. The Cortana consent page will appear in Azure AAD OOBE during setup.

<!--/SupportedValues-->
<!--EndPolicy-->

<hr/>

<!--StartPolicy-->
<a href="" id="search-allowindexingencryptedstoresoritems"></a>**Search/AllowIndexingEncryptedStoresOrItems**  

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
	<td><img src="images/checkmark.png" alt="check mark" /></td>
	<td></td>
	<td><img src="images/checkmark.png" alt="check mark" /></td>
	<td><img src="images/checkmark.png" alt="check mark" /></td>
	<td><img src="images/checkmark.png" alt="check mark" /></td>
	<td><img src="images/checkmark.png" alt="check mark" /></td>
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
Allows or disallows the indexing of items. This switch is for the Windows Search Indexer, which controls whether it will index items that are encrypted, such as the Windows Information Protection (WIP) protected files.

When the policy is enabled, WIP protected items are indexed and the metadata about them are stored in an unencrypted location. The metadata includes things like file path and date modified.

When the policy is disabled, the WIP protected items are not indexed and do not show up in the results in Cortana or file explorer. There may also be a performance impact on photos and Groove apps if there are a lot of WIP protected media files on the device.

Most restricted value is 0.

<!--/Description-->
<!--SupportedValues-->
The following list shows the supported values:

-   0 – Not allowed.
-   1 (default) – Allowed.

<!--/SupportedValues-->
<!--EndPolicy-->

<hr/>

<!--StartPolicy-->
<a href="" id="search-allowsearchtouselocation"></a>**Search/AllowSearchToUseLocation**  

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
	<td><img src="images/checkmark.png" alt="check mark" /></td>
	<td></td>
	<td><img src="images/checkmark.png" alt="check mark" /></td>
	<td><img src="images/checkmark.png" alt="check mark" /></td>
	<td><img src="images/checkmark.png" alt="check mark" /></td>
	<td><img src="images/checkmark.png" alt="check mark" /></td>
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
Specifies whether search can leverage location information.

Most restricted value is 0.

<!--/Description-->
<!--SupportedValues-->
The following list shows the supported values:

-   0 – Not allowed.
-   1 (default) – Allowed.

<!--/SupportedValues-->
<!--EndPolicy-->

<hr/>

<!--StartPolicy-->
<a href="" id="search-allowstoringimagesfromvisionsearch"></a>**Search/AllowStoringImagesFromVisionSearch**  

<!--Scope-->
[Scope](./policy-configuration-service-provider.md#policy-scope):

> [!div class = "checklist"]
> * Device

<hr/>

<!--/Scope-->
<!--Description-->
This policy has been deprecated.

<!--/Description-->
<!--EndPolicy-->

<hr/>

<!--StartPolicy-->
<a href="" id="search-allowusingdiacritics"></a>**Search/AllowUsingDiacritics**  

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
	<td><img src="images/checkmark.png" alt="check mark" /></td>
	<td></td>
	<td><img src="images/checkmark.png" alt="check mark" /></td>
	<td><img src="images/checkmark.png" alt="check mark" /></td>
	<td><img src="images/checkmark.png" alt="check mark" /></td>
	<td><img src="images/checkmark.png" alt="check mark" /></td>
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
Allows the use of diacritics.

The following list shows the supported values:

-   0 – Not allowed.
-   1 (default) – Allowed.

Most restricted value is 0.

<!--/Description-->
<!--EndPolicy-->

<hr/>

<!--StartPolicy-->
<a href="" id="search-allowwindowsindexer"></a>**Search/AllowWindowsIndexer**  

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
	<td><img src="images/checkmark.png" alt="check mark" /></td>
	<td></td>
	<td><img src="images/checkmark.png" alt="check mark" /></td>
	<td><img src="images/checkmark.png" alt="check mark" /></td>
	<td><img src="images/checkmark.png" alt="check mark" /></td>
	<td><img src="images/checkmark.png" alt="check mark" /></td>
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
Allow Windows indexer. Value type is integer.

<!--/Description-->
<!--EndPolicy-->

<hr/>

<!--StartPolicy-->
<a href="" id="search-alwaysuseautolangdetection"></a>**Search/AlwaysUseAutoLangDetection**  

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
	<td><img src="images/checkmark.png" alt="check mark" /></td>
	<td></td>
	<td><img src="images/checkmark.png" alt="check mark" /></td>
	<td><img src="images/checkmark.png" alt="check mark" /></td>
	<td><img src="images/checkmark.png" alt="check mark" /></td>
	<td><img src="images/checkmark.png" alt="check mark" /></td>
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
Specifies whether to always use automatic language detection when indexing content and properties.

The following list shows the supported values:

-   0 – Not allowed.
-   1 (default) – Allowed.

Most restricted value is 0.

<!--/Description-->
<!--EndPolicy-->

<hr/>

<!--StartPolicy-->
<a href="" id="search-disablebackoff"></a>**Search/DisableBackoff**  

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
	<td><img src="images/checkmark.png" alt="check mark" /></td>
	<td></td>
	<td><img src="images/checkmark.png" alt="check mark" /></td>
	<td><img src="images/checkmark.png" alt="check mark" /></td>
	<td><img src="images/checkmark.png" alt="check mark" /></td>
	<td><img src="images/checkmark.png" alt="check mark" /></td>
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
If enabled, the search indexer backoff feature will be disabled. Indexing will continue at full speed even when system activity is high. If disabled, backoff logic will be used to throttle back indexing activity when system activity is high. Default is disabled.

The following list shows the supported values:

-   0 (default) – Disable.
-   1 – Enable.

<!--/Description-->
<!--EndPolicy-->

<hr/>

<!--StartPolicy-->
<a href="" id="search-disableremovabledriveindexing"></a>**Search/DisableRemovableDriveIndexing**  

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
	<td><img src="images/checkmark.png" alt="check mark" /></td>
	<td></td>
	<td><img src="images/checkmark.png" alt="check mark" /></td>
	<td><img src="images/checkmark.png" alt="check mark" /></td>
	<td><img src="images/checkmark.png" alt="check mark" /></td>
	<td><img src="images/checkmark.png" alt="check mark" /></td>
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
This policy setting configures whether or not locations on removable drives can be added to libraries.

If you enable this policy setting, locations on removable drives cannot be added to libraries. In addition, locations on removable drives cannot be indexed.

If you disable or do not configure this policy setting, locations on removable drives can be added to libraries. In addition, locations on removable drives can be indexed.

The following list shows the supported values:

-   0 (default) – Disable.
-   1 – Enable.

<!--/Description-->
<!--EndPolicy-->

<hr/>

<!--StartPolicy-->
<a href="" id="search-donotusewebresults"></a>**Search/DoNotUseWebResults**  

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
Added in Windows 10, next major update. Don't search the web or display web results in Search.

This policy setting allows you to control whether or not Search can perform queries on the web, and if the web results are displayed in Search.
If you enable this policy setting, queries won't be performed on the web and web results won't be displayed when a user performs a query in Search.

If you disable this policy setting, queries will be performed on the web and web results will be displayed when a user performs a query in Search.

<!--/Description-->
<!--SupportedValues-->
The following list shows the supported values:

- 0 - Not allowed. Queries won't be performed on the web and web results won't be displayed when a user performs a query in Search.
- 1 (default) - Allowed. Queries will be performed on the web and web results will be displayed when a user performs a query in Search.

<!--/SupportedValues-->
<!--EndPolicy-->

<hr/>

<!--StartPolicy-->
<a href="" id="search-preventindexinglowdiskspacemb"></a>**Search/PreventIndexingLowDiskSpaceMB**  

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
	<td><img src="images/checkmark.png" alt="check mark" /></td>
	<td></td>
	<td><img src="images/checkmark.png" alt="check mark" /></td>
	<td><img src="images/checkmark.png" alt="check mark" /></td>
	<td><img src="images/checkmark.png" alt="check mark" /></td>
	<td><img src="images/checkmark.png" alt="check mark" /></td>
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
Enabling this policy prevents indexing from continuing after less than the specified amount of hard drive space is left on the same drive as the index location. Select between 0 and 1.

Enable this policy if computers in your environment have extremely limited hard drive space.

When this policy is disabled or not configured, Windows Desktop Search automatically manages your index size.

The following list shows the supported values:

-   0 – Disable.
-   1 (default) – Enable.

<!--/Description-->
<!--EndPolicy-->

<hr/>

<!--StartPolicy-->
<a href="" id="search-preventremotequeries"></a>**Search/PreventRemoteQueries**  

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
	<td><img src="images/checkmark.png" alt="check mark" /></td>
	<td></td>
	<td><img src="images/checkmark.png" alt="check mark" /></td>
	<td><img src="images/checkmark.png" alt="check mark" /></td>
	<td><img src="images/checkmark.png" alt="check mark" /></td>
	<td><img src="images/checkmark.png" alt="check mark" /></td>
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
If enabled, clients will be unable to query this computer's index remotely. Thus, when they are browsing network shares that are stored on this computer, they will not search them using the index. If disabled, client search requests will use this computer's index..

The following list shows the supported values:

-   0 – Disable.
-   1 (default) – Enable.

<!--/Description-->
<!--EndPolicy-->

<hr/>

<!--StartPolicy-->
<a href="" id="search-safesearchpermissions"></a>**Search/SafeSearchPermissions**  

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
	<td><img src="images/crossmark.png" alt="cross mark" /></td>
	<td></td>
	<td><img src="images/crossmark.png" alt="cross mark" /></td>
	<td><img src="images/crossmark.png" alt="cross mark" /></td>
	<td><img src="images/checkmark.png" alt="check mark" /></td>
	<td><img src="images/checkmark.png" alt="check mark" /></td>
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
> [!NOTE]
> This policy is only enforced in Windows 10 Mobile and not supported in Windows 10 for desktop.


Specifies what level of safe search (filtering adult content) is required.

The following list shows the supported values:

-   0 – Strict, highest filtering against adult content.
-   1 (default) – Moderate filtering against adult content (valid search results will not be filtered).

Most restricted value is 0.

<!--/Description-->
<!--EndPolicy-->
<hr/>

Footnote:

-   1 - Added in Windows 10, version 1607.
-   2 - Added in Windows 10, version 1703.
-   3 - Added in Windows 10, version 1709.

<!--EndPolicies-->

<!--StartEAS-->
## <a href="" id="eas"></a>Search policies that can be set using Exchange Active Sync (EAS)  

-   [Search/AllowSearchToUseLocation](#search-allowsearchtouselocation)  
<!--EndEAS-->

<!--StartHoloLens-->
## <a href="" id="hololenspolicies"></a>Search policies supported by Windows Holographic for Business  

-   [Search/AllowSearchToUseLocation](#search-allowsearchtouselocation)  
<!--EndHoloLens-->

