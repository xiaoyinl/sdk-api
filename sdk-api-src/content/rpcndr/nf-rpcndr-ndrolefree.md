---
UID: NF:rpcndr.NdrOleFree
title: NdrOleFree function (rpcndr.h)
description: The NdrOleFree function is a wrapper for the CoTaskMemFree function.
old-location: rpc\ndrolefree.htm
tech.root: Rpc
ms.assetid: c4289448-11bb-40d1-ae63-68521b901796
ms.date: 12/05/2018
ms.keywords: NdrOleFree, NdrOleFree function [RPC], rpc.ndrolefree, rpcndr/NdrOleFree
f1_keywords:
- rpcndr/NdrOleFree
dev_langs:
- c++
req.header: rpcndr.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: RpcRT4.lib
req.dll: RpcRT4.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- RpcRT4.dll
api_name:
- NdrOleFree
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# NdrOleFree function


## -description


The <b>NdrOleFree</b> function is a wrapper for the <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function.


## -parameters




### -param NodeToFree [in]

Pointer to the memory to be freed.


## -returns



This function does not return a value.



