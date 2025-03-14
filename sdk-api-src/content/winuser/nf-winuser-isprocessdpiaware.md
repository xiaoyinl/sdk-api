---
UID: NF:winuser.IsProcessDPIAware
title: IsProcessDPIAware function (winuser.h)
description: IsProcessDPIAware may be altered or unavailable. Instead, use GetProcessDPIAwareness.
old-location: winmsg\isprocessdpiaware.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\isprocessdpiaware.htm
ms.date: 12/05/2018
ms.keywords: IsProcessDPIAware, IsProcessDPIAware function [Windows and Messages], _win32_IsProcessDPIAware, _win32_isprocessdpiaware_cpp, winmsg.isprocessdpiaware, winui._win32_isprocessdpiaware, winuser/IsProcessDPIAware
f1_keywords:
- winuser/IsProcessDPIAware
dev_langs:
- c++
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- User32.dll
- Ext-MS-Win-RTCore-NTUser-sysparams-l1-1-0.dll
- minuser.dll
api_name:
- IsProcessDPIAware
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IsProcessDPIAware function


## -description


<p class="CCE_Message">[<p class="note">IsProcessDPIAware is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use GetProcessDPIAwareness.</p>]

Determines whether the current process is dots per inch (dpi) aware such that it adjusts the sizes of UI elements to compensate for the dpi setting.


## -parameters






## -returns



Type: <strong>Type: <b>BOOL</b>
</strong>

<b>TRUE</b> if the process is dpi aware; otherwise, <b>FALSE</b>.



