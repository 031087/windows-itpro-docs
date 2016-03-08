---
title: Determine What to Migrate (Windows 10)
description: Determine What to Migrate
ms.assetid: 01ae1d13-c3eb-4618-b39d-ee5d18d55761
ms.prod: W10
ms.mktglfcycl: deploy
ms.sitesec: library
author: CFaw
---

# Determine What to Migrate


By default, User State Migration Tool (USMT) 10.0 migrates the items listed in [What Does USMT Migrate?](what-does-usmt-migrate-usmt-win7-usmt-win8.md), depending on the migration .xml files you specify. These default settings are often enough for a basic migration.

However, when considering what settings to migrate, you should also consider what settings you would like the user to be able to configure, if any, and what settings you would like to standardize. Many organizations use their migration as an opportunity to create and begin enforcing a better-managed environment. Some of the settings that users can configure on unmanaged computers prior to the migration can be locked on the new, managed computers. For example, standard wallpaper, Internet Explorer security settings, and desktop configuration are some of the items you can choose to standardize.

To reduce complexity and increase standardization, your organization should consider creating a *standard operating environment (SOE)*. An SOE is a combination of hardware and software that you distribute to all users. This means selecting a baseline for all computers, including standard hardware drivers; core operating system features; core productivity applications, especially if they are under volume licensing; and core utilities. This environment should also include a standard set of security features, as outlined in the organization’s corporate policy. Using a standard operating environment can vastly simplify the migration and reduce overall deployment challenges.

## In This Section


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>[Identify Users](identify-users-usmt-win7-usmt-win8.md)</p></td>
<td align="left"><p>Use command-line options to specify which users to migrate and how they should be migrated.</p></td>
</tr>
<tr class="even">
<td align="left"><p>[Identify Applications Settings](identify-applications-settings-usmt-win7-usmt-win8.md)</p></td>
<td align="left"><p>Determine which applications you want to migrate and prepare a list of application settings to be migrated.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>[Identify Operating System Settings](identify-operating-system-settings-usmt-win7-usmt-win8.md)</p></td>
<td align="left"><p>Use migration to create a new standard environment on each of the destination computers.</p></td>
</tr>
<tr class="even">
<td align="left"><p>[Identify File Types, Files, and Folders](identify-file-types-files-and-folders-usmt-win8.md)</p></td>
<td align="left"><p>Determine and locate the standard, company-specified, and non-standard locations of the file types, files, folders, and settings that you want to migrate.</p></td>
</tr>
</tbody>
</table>

 

## Related topics


[What Does USMT Migrate?](what-does-usmt-migrate-usmt-win7-usmt-win8.md)

 

 





