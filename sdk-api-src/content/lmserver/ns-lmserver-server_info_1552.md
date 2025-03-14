---
UID: NS:lmserver._SERVER_INFO_1552
title: SERVER_INFO_1552 (lmserver.h)
description: The SERVER_INFO_1552 structure specifies the maximum time allowed for a link delay.
old-location: netmgmt\server_info_1552_str.htm
tech.root: NetMgmt
ms.assetid: eb725f37-4bcd-4402-968f-ea6d58d7d79a
ms.date: 12/05/2018
ms.keywords: '*LPSERVER_INFO_1552, *PSERVER_INFO_1552, LPSERVER_INFO_1552, LPSERVER_INFO_1552 structure pointer [Network Management], PSERVER_INFO_1552, PSERVER_INFO_1552 structure pointer [Network Management], SERVER_INFO_1552, SERVER_INFO_1552 structure [Network Management], _win32_server_info_1552_str, lmserver/LPSERVER_INFO_1552, lmserver/PSERVER_INFO_1552, lmserver/SERVER_INFO_1552, netmgmt.server_info_1552_str'
f1_keywords:
- lmserver/SERVER_INFO_1552
dev_langs:
- c++
req.header: lmserver.h
req.include-header: Lm.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Lmserver.h
api_name:
- SERVER_INFO_1552
targetos: Windows
req.typenames: SERVER_INFO_1552, *PSERVER_INFO_1552, *LPSERVER_INFO_1552
req.redist: 
ms.custom: 19H1
---

# SERVER_INFO_1552 structure


## -description


The
				<b>SERVER_INFO_1552</b> structure specifies the maximum time allowed for a link delay.


## -struct-fields




### -field sv1552_maxlinkdelay

Specifies the maximum time allowed for a link delay, in seconds. If delays exceed this number, the server disables raw I/O for this connection.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/lmserver/nf-lmserver-netservergetinfo">NetServerGetInfo</a>



<a href="https://docs.microsoft.com/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>



<a href="https://docs.microsoft.com/windows/desktop/NetMgmt/server-functions">Server Functions</a>
 

 

