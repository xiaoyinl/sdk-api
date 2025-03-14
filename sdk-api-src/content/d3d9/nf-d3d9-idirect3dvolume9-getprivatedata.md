---
UID: NF:d3d9.IDirect3DVolume9.GetPrivateData
title: IDirect3DVolume9::GetPrivateData (d3d9.h)
description: Copies the private data associated with the volume to a provided buffer.
old-location: direct3d9\idirect3dvolume9__getprivatedata.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dvolume9__getprivatedata.htm
ms.date: 12/05/2018
ms.keywords: 1b475aea-86d8-9a27-8391-6760763a593e, GetPrivateData, GetPrivateData method [Direct3D 9], GetPrivateData method [Direct3D 9],IDirect3DVolume9 interface, IDirect3DVolume9 interface [Direct3D 9],GetPrivateData method, IDirect3DVolume9.GetPrivateData, IDirect3DVolume9::GetPrivateData, d3d9helper/IDirect3DVolume9::GetPrivateData, direct3d9.idirect3dvolume9__getprivatedata
f1_keywords:
- d3d9/IDirect3DVolume9.GetPrivateData
dev_langs:
- c++
req.header: d3d9.h
req.include-header: D3D9.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D3D9.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- D3D9.lib
- D3D9.dll
api_name:
- IDirect3DVolume9.GetPrivateData
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDirect3DVolume9::GetPrivateData


## -description


Copies the private data associated with the volume to a provided buffer.


## -parameters




### -param refguid [in]

Type: <b><a href="http://go.microsoft.com/?linkid=9742306">REFGUID</a></b>

Reference to (C++) or address of (C) the globally unique identifier that identifies the private data to retrieve. 


### -param pData [in, out]

Type: <b>void*</b>

Pointer to a previously allocated buffer to fill with the requested private data if the call succeeds. The application calling this method is responsible for allocating and releasing this buffer. If this parameter is <b>NULL</b>, this method will return the buffer size in pSizeOfData.


### -param pSizeOfData [in, out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">DWORD</a>*</b>

Pointer to the size of the buffer at 
    pData, in bytes. If this value is less than the actual size of the private data, such as 0, the method sets this parameter to the required buffer size, and the method returns D3DERR_MOREDATA. 


## -returns



Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be one of the following: D3DERR_INVALIDCALL, D3DERR_MOREDATA, D3DERR_NOTFOUND.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dvolume9">IDirect3DVolume9</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3dvolume9-freeprivatedata">IDirect3DVolume9::FreePrivateData</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3dvolume9-setprivatedata">IDirect3DVolume9::SetPrivateData</a>
 

 

