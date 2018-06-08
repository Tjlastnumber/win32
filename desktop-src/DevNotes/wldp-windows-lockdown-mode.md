---
Description: Describes the secure modes (S modes) for a Windows device.
ms.assetid: CE50AC56-0295-477C-93CB-ABAB92482A59
title: WLDP\_WINDOWS\_LOCKDOWN\_MODE enumeration
ms.technology: desktop
ms.prod: windows
ms.author: windowssdkdev
ms.topic: enumeration
ms.date: 05/31/2018
---

# WLDP\_WINDOWS\_LOCKDOWN\_MODE enumeration

Describes the secure modes (S modes) for a Windows device. Used primarily in [**WldpQueryWindowsLockdownMode**](wldpquerywindowslockdownmode.md).

## Syntax


```C++
typedef enum _WLDP_WINDOWS_LOCKDOWN_MODE { 
  WLDP_WINDOWS_LOCKDOWN_MODE_UNLOCKED  = 0,
  WLDP_WINDOWS_LOCKDOWN_MODE_TRIAL     = 1,
  WLDP_WINDOWS_LOCKDOWN_MODE_LOCKED    = 2,
  WLDP_WINDOWS_LOCKDOWN_MODE_MAX       = 3
} WLDP_WINDOWS_LOCKDOWN_MODE, *PWLDP_WINDOWS_LOCKDOWN_MODE;
```



## Constants

<dl> <dt>

<span id="WLDP_WINDOWS_LOCKDOWN_MODE_UNLOCKED"></span><span id="wldp_windows_lockdown_mode_unlocked"></span>**WLDP\_WINDOWS\_LOCKDOWN\_MODE\_UNLOCKED**
</dt> <dd>

Unlocked. Used primarily for Windows devices without the S mode.

</dd> <dt>

<span id="WLDP_WINDOWS_LOCKDOWN_MODE_TRIAL"></span><span id="wldp_windows_lockdown_mode_trial"></span>**WLDP\_WINDOWS\_LOCKDOWN\_MODE\_TRIAL**
</dt> <dd>

Trial. Used primarily for a Windows 10 trial device with the S mode. Trial mode is a special case for Windows 10 devices with the S mode: policies are enforced, but there is no anti-rollback protection for the enforcement of the policy.

</dd> <dt>

<span id="WLDP_WINDOWS_LOCKDOWN_MODE_LOCKED"></span><span id="wldp_windows_lockdown_mode_locked"></span>**WLDP\_WINDOWS\_LOCKDOWN\_MODE\_LOCKED**
</dt> <dd>

Locked. Used primarily for a Windows 10 device with the S mode. A device that is locked will enforce the signed Device Guard policies shipped with the Windows 10 OS image with the S mode.

</dd> <dt>

<span id="WLDP_WINDOWS_LOCKDOWN_MODE_MAX"></span><span id="wldp_windows_lockdown_mode_max"></span>**WLDP\_WINDOWS\_LOCKDOWN\_MODE\_MAX**
</dt> <dd>

The maximum enumeration value.

</dd> </dl>

## Requirements



|                   |                                                                                   |
|-------------------|-----------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wldp.h</dt> </dl> |



 

 



