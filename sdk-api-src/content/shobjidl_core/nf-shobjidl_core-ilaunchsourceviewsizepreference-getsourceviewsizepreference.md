---
UID: NF:shobjidl_core.ILaunchSourceViewSizePreference.GetSourceViewSizePreference
title: ILaunchSourceViewSizePreference::GetSourceViewSizePreference (shobjidl_core.h)
description: Retrieves the view size preference of the application after the application has launched.
old-location: shell\ILaunchSourceViewSizePreference_GetSourceViewSizePreference.htm
tech.root: shell
ms.assetid: A151EA3D-42EE-4F22-B2A8-C696F582F81C
ms.date: 12/05/2018
ms.keywords: GetSourceViewSizePreference, GetSourceViewSizePreference method [Windows Shell], GetSourceViewSizePreference method [Windows Shell],ILaunchSourceViewSizePreference interface, ILaunchSourceViewSizePreference interface [Windows Shell],GetSourceViewSizePreference method, ILaunchSourceViewSizePreference.GetSourceViewSizePreference, ILaunchSourceViewSizePreference::GetSourceViewSizePreference, shell.ILaunchSourceViewSizePreference_GetSourceViewSizePreference, shobjidl_core/ILaunchSourceViewSizePreference::GetSourceViewSizePreference
f1_keywords:
- shobjidl_core/ILaunchSourceViewSizePreference.GetSourceViewSizePreference
dev_langs:
- c++
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
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
- COM
api_location:
- shobjidl_core.h
api_name:
- ILaunchSourceViewSizePreference.GetSourceViewSizePreference
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ILaunchSourceViewSizePreference::GetSourceViewSizePreference


## -description


Retrieves the view size preference of the application after the application has launched.


## -parameters




### -param sourceSizeAfterLaunch [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/ne-shobjidl_core-application_view_size_preference">APPLICATION_VIEW_SIZE_PREFERENCE</a>*</b>

Contains the address of a pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/ne-shobjidl_core-application_view_size_preference">APPLICATION_VIEW_SIZE_PREFERENCE</a>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ilaunchsourceviewsizepreference">ILaunchSourceViewSizePreference</a>
 

 

