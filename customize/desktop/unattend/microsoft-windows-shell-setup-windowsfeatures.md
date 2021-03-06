---
title: WindowsFeatures
description: WindowsFeatures
MSHAttr:
- 'PreferredSiteName:MSDN'
- 'PreferredLib:/library/windows/hardware'
ms.assetid: 5b23171f-3c76-4c79-ae15-bb4c8fcc65b7
ms.mktglfcycl: deploy
ms.sitesec: msdn
ms.author: alhopper
ms.date: 05/02/2017
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-oem
---

# WindowsFeatures


`WindowsFeatures` specifies whether to show entry points for Internet Explorer, Media Center, Windows Media Player, and Windows Mail.

**Important**  
Using these settings to remove components that do not exist in the image will cause Windows Setup to fail.

 

This setting has no effect on Server Core installations of Windows Server 2008, Windows Server 2008 R2, and Windows Server 2012.

## Child Elements


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>[ShowInternetExplorer](microsoft-windows-shell-setup-windowsfeatures-showinternetexplorer.md)</p></td>
<td><p>Specifies whether to show entry points for Internet Explorer.</p></td>
</tr>
<tr class="even">
<td><p>[ShowMediaCenter](microsoft-windows-shell-setup-windowsfeatures-showmediacenter.md)</p></td>
<td><p>Specifies whether to show entry points for Media Center.</p></td>
</tr>
<tr class="odd">
<td><p>[ShowWindowsMediaPlayer](microsoft-windows-shell-setup-windowsfeatures-showwindowsmediaplayer.md)</p></td>
<td><p>Specifies whether to show entry points for Windows Media Player.</p></td>
</tr>
</tbody>
</table>

 

## Valid Passes


auditSystem

auditUser

oobeSystem

specialize

## Parent Hierarchy


[Microsoft-Windows-Shell-Setup](microsoft-windows-shell-setup.md) | **WindowsFeatures**

## Applies To


For the list of the supported Windows editions and architectures that this component supports, see [Microsoft-Windows-Shell-Setup](microsoft-windows-shell-setup.md).

## XML Example


The following XML output shows how to specify that the entry points for these Windows features not be displayed.

``` syntax
<WindowsFeatures>
   <ShowInternetExplorer>false</ShowInternetExplorer>
   <ShowMediaCenter>false</ShowMediaCenter>
   <ShowWindowsMediaPlayer>false</ShowWindowsMediaPlayer>
   <ShowWindowsMail>false</ShowWindowsMail>
</WindowsFeatures>
```

## Related topics


[Microsoft-Windows-Shell-Setup](microsoft-windows-shell-setup.md)

 

 







