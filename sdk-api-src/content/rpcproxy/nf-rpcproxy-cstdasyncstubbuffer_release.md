---
UID: NF:rpcproxy.CStdAsyncStubBuffer_Release
title: CStdAsyncStubBuffer_Release function (rpcproxy.h)
description: Implements the IRpcStubBuffer::Release method.
old-location: rpc\cstdasyncstubbuffer_release.htm
tech.root: Rpc
ms.assetid: 963EB39C-F260-4FE5-94A9-D23AC7CC59E1
ms.date: 12/05/2018
ms.keywords: CStdAsyncStubBuffer_Release, CStdAsyncStubBuffer_Release function [RPC], rpc.cstdasyncstubbuffer_release, rpcproxy/CStdAsyncStubBuffer_Release
f1_keywords:
- rpcproxy/CStdAsyncStubBuffer_Release
dev_langs:
- c++
req.header: rpcproxy.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2016 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- ole32.dll
- API-MS-Win-Core-Com-MidlProxyStub-L1-1-0.dll
- COMBase.dll
api_name:
- CStdAsyncStubBuffer_Release
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CStdAsyncStubBuffer_Release function


## -description


<p class="CCE_Message">[CStdAsyncStubBuffer_Release is not supported and may be altered or unavailable in the future.]

Implements the <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-irpcstubbuffer">IRpcStubBuffer::Release</a> method.


## -parameters




### -param pthis [in]

Pointer to  the <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-irpcstubbuffer">IRpcStubBuffer</a> object. 


## -returns



Returns an integer from 1 to <i>n</i>, indicating the value of the new reference count.




## -remarks



This function is used internally by proxies that are generated by MIDL.



