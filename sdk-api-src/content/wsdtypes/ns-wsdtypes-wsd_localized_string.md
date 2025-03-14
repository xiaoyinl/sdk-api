---
UID: NS:wsdtypes._WSD_LOCALIZED_STRING
title: WSD_LOCALIZED_STRING (wsdtypes.h)
description: Represents a single localized string.
old-location: ncd\wsd_localized_string_struct.htm
tech.root: WsdApi
ms.assetid: c90cc459-a10d-4b2b-81bc-96e562755b6c
ms.date: 12/05/2018
ms.keywords: WSD_LOCALIZED_STRING, WSD_LOCALIZED_STRING structure, ncd.wsd_localized_string_struct, wsdtypes/WSD_LOCALIZED_STRING
f1_keywords:
- wsdtypes/WSD_LOCALIZED_STRING
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
- WSD_LOCALIZED_STRING
targetos: Windows
req.typenames: WSD_LOCALIZED_STRING
req.redist: 
ms.custom: 19H1
---

# WSD_LOCALIZED_STRING structure


## -description


Represents a single localized string.


## -struct-fields




### -field lang

The standard language code used for localization. Valid language codes are specified in <a href="https://go.microsoft.com/fwlink/p/?linkid=84408">RFC 1766</a>.


### -field String

The string data in the localized language.


## -remarks



<a href="https://go.microsoft.com/fwlink/p/?linkid=84408">RFC 1766</a> extends <a href="https://go.microsoft.com/fwlink/p/?linkid=84445">ISO-639</a>. Dialect extensions to the <a href="https://go.microsoft.com/fwlink/p/?linkid=84445">ISO-639</a> codes are used for the <i>lang</i> member. For example, "en-US" is used to indicate a string localized for the USA/English dialect.



