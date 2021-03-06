---
title: Key
description: Key
MSHAttr:
- 'PreferredSiteName:MSDN'
- 'PreferredLib:/library/windows/hardware'
ms.assetid: 9708430e-cf23-4d46-8177-127d0435767d
ms.mktglfcycl: deploy
ms.sitesec: msdn
ms.author: alhopper
ms.date: 05/02/2017
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-oem
---

# Key


`Key` specifies the unique string to identify the name of the firewall group.

The value for `Key` is added to the answer file as an attribute of the [FirewallGroup](networking-mpssvc-svcfirewallgroups-firewallgroup.md) element. The attribute `wcm:keyValue` is used to identify each unique firewall group. For example, you can specify three different firewall groups by using the `Key` value of **RemoteDesktop**, **WindowsMediaPlayer**, and **HomeGroup**.

## Values


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><em>Key</em></p></td>
<td><p>Specifies the unique string used to identify the firewall group. <em>Key</em> is a string.</p></td>
</tr>
</tbody>
</table>

 

This string type does not support empty elements. Do not create an empty value for this setting.

## Parent Hierarchy


[Networking-MPSSVC-Svc](networking-mpssvc-svc.md) | [FirewallGroups](networking-mpssvc-svcfirewallgroups.md) | [FirewallGroup](networking-mpssvc-svcfirewallgroups-firewallgroup.md) | **Key**

## Valid Passes


specialize

## Applies To


For a list of the supported Windows editions and architectures that this component supports, see [Networking-MPSSVC-Svc](networking-mpssvc-svc.md).

## XML Example


The following XML output shows how to set Windows Firewall groups.

``` syntax
<FirewallGroups>
      <FirewallGroup wcm:action="add" wcm:keyValue="RemoteDesktop">
      <Active>true</Active> 
      <Group>Remote Desktop</Group> 
      <Profile>all</Profile> 
   </FirewallGroup>
</FirewallGroups>
```

## Related topics


[FirewallGroup](networking-mpssvc-svcfirewallgroups-firewallgroup.md)

 

 







