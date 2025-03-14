---
UID: NS:wsdtypes._WSD_SCOPES
title: WSD_SCOPES (wsdtypes.h)
description: A collection of scopes used in WS-Discovery messaging.
old-location: ncd\wsd_scopes_struct.htm
tech.root: WsdApi
ms.assetid: 3415fef0-dbf4-4ece-bad0-6cd6831404db
ms.date: 12/05/2018
ms.keywords: WSD_SCOPES, WSD_SCOPES structure, ncd.wsd_scopes_struct, wsdtypes/WSD_SCOPES
f1_keywords:
- wsdtypes/WSD_SCOPES
dev_langs:
- c++
req.header: wsdtypes.h
req.include-header: Wsdapi.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- WsdTypes.h
api_name:
- WSD_SCOPES
targetos: Windows
req.typenames: WSD_SCOPES
req.redist: 
ms.custom: 19H1
---

# WSD_SCOPES structure


## -description


A collection of scopes used in WS-Discovery messaging.


## -struct-fields




### -field MatchBy

A matching rule used for scopes.


### -field Scopes

Reference to a <a href="https://docs.microsoft.com/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_uri_list">WSD_URI_LIST</a> structure that contains a list of scopes.

