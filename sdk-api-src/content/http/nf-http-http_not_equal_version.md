---
UID: NF:http.HTTP_NOT_EQUAL_VERSION
title: HTTP_NOT_EQUAL_VERSION macro (http.h)
description: Returns a non-zero value if an HTTP_VERSION structure is greater or less than a specified major/minor version combination, or zero if it is equal.
old-location: http\http_not_equal_version.htm
tech.root: http
ms.assetid: 5ce37dd4-dc40-4e24-b6e3-bc9dccf4140b
ms.date: 12/05/2018
ms.keywords: HTTP_NOT_EQUAL_VERSION, HTTP_NOT_EQUAL_VERSION macro [HTTP], _http_http_not_equal_version, http.http_not_equal_version, http/HTTP_NOT_EQUAL_VERSION
f1_keywords:
- http/HTTP_NOT_EQUAL_VERSION
dev_langs:
- c++
req.header: http.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
- Http.h
api_name:
- HTTP_NOT_EQUAL_VERSION
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# HTTP_NOT_EQUAL_VERSION macro


## -description


The 
<b>HTTP_NOT_EQUAL_VERSION</b> macro returns a non-zero value if an 
<a href="https://docs.microsoft.com/windows/desktop/api/http/ns-http-http_version">HTTP_VERSION</a> structure is greater or less than a specified major/minor version combination, or zero if it is equal.


## -parameters




### -param version

The 
<a href="https://docs.microsoft.com/windows/desktop/api/http/ns-http-http_version">HTTP_VERSION</a> structure to be examined.


### -param major

The major portion of the version to be compared.


### -param minor

The minor portion of the version to be compared.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Http/http-server-api-version-1-0-macros">HTTP Server API Version 1.0 Macros</a>
 

 

