---
title: AutoLogon
description: AutoLogon specifies the account to use to log on to a computer automatically. AutoLogon credentials are deleted from the unattended installation answer file after Windows Setup is complete.
MSHAttr:
- 'PreferredSiteName:MSDN'
- 'PreferredLib:/library/windows/hardware'
ms.assetid: 52db5702-5c0d-4045-b92d-d0a6eac9e43a
ms.mktglfcycl: deploy
ms.sitesec: msdn
ms.author: alhopper
ms.date: 05/02/2017
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-oem
---

# AutoLogon


`AutoLogon` specifies the account to use to log on to a computer automatically. `AutoLogon` credentials are deleted from the unattended installation answer file after Windows Setup is complete.

**Important**  
-   In Windows 10, if you configure `AutoLogon`, the OS will skip the user account creation phase during OOBE. This is a change from previous versions of Windows.

    In addition, the account creation phase during OOBE is skipped in all versions of Windows when at least one user account is created through the `UserAccounts` section of the same unattend file. This change only applies when no user account is created by unattend such as when setting `AutoLogon` for a built-in or existing account like Administrator or Guest. In these scenarios, Microsoft recommends using unattend to create at least one user account in the Administrators group to ensure that the device can be managed after the autologon is complete.

-   Make sure `AutoLogon` is disabled on computers that are delivered to customers.

 

For more information about the built-in administrator account, see the [How to Enable and Disable the Built-in Administrator Account](http://go.microsoft.com/fwlink/?LinkId=206616) topic in the Windows Assessment and Deployment Kit (Windows ADK) Technical Reference.

**Note**  
These settings are valid for upgrades.

 

## Child Elements


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>[Domain](microsoft-windows-shell-setup-autologon-domain.md)</p></td>
<td><p>Specifies the domain to which the computer is logging on.</p></td>
</tr>
<tr class="even">
<td><p>[Enabled](microsoft-windows-shell-setup-autologon-enabled.md)</p></td>
<td><p>Specifies whether the automatic logon process is enabled.</p></td>
</tr>
<tr class="odd">
<td><p>[LogonCount](microsoft-windows-shell-setup-autologon-logoncount.md)</p></td>
<td><p>Specifies the number of times that the account has been used. <code>LogonCount</code> must be specified if <code>AutoLogon</code> is used.</p></td>
</tr>
<tr class="even">
<td><p>[Password](microsoft-windows-shell-setup-autologon-password.md)</p></td>
<td><p>Specifies the password for the account that is used for automatic logon.</p></td>
</tr>
<tr class="odd">
<td><p>[Username](microsoft-windows-shell-setup-autologon-username.md)</p></td>
<td><p>Specifies the user account name that is used for automatic logon.</p></td>
</tr>
</tbody>
</table>

 

## Valid Configuration Passes


auditSystem

oobeSystem

specialize

## Parent Hierarchy


[Microsoft-Windows-Shell-Setup](microsoft-windows-shell-setup.md) | **AutoLogon**

## Applies To


For a list of the Windows editions and architectures that this component supports, see [Microsoft-Windows-Shell-Setup](microsoft-windows-shell-setup.md). This setting is not configured in a Nano Server image.

## XML Example


The following XML output shows how to set automatic logon.

``` syntax
<AutoLogon>
   <Password>
      <Value>MyPassword</Value>
   </Password>
   <Domain>FabrikamDomain</Domain>
   <Enabled>true</Enabled>
   <LogonCount>2</LogonCount>
   <Username>MyUserName</Username>
</AutoLogon>
```

## Related topics


[Microsoft-Windows-Shell-Setup](microsoft-windows-shell-setup.md)

 

 







