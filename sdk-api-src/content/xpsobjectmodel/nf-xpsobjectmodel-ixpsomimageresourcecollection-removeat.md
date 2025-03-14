---
UID: NF:xpsobjectmodel.IXpsOMImageResourceCollection.RemoveAt
title: IXpsOMImageResourceCollection::RemoveAt (xpsobjectmodel.h)
description: Removes and releases an IXpsOMImageResource interface pointer from a specified location in the collection.
old-location: xps\ixpsomimageresourcecollection_removeat.htm
tech.root: printdocs
ms.assetid: 29945211-d204-4da9-a77d-20598060750f
ms.date: 12/05/2018
ms.keywords: IXpsOMImageResourceCollection interface [XPS Documents and Packaging],RemoveAt method, IXpsOMImageResourceCollection.RemoveAt, IXpsOMImageResourceCollection::RemoveAt, RemoveAt, RemoveAt method [XPS Documents and Packaging], RemoveAt method [XPS Documents and Packaging],IXpsOMImageResourceCollection interface, xps.ixpsomimageresourcecollection_removeat, xpsobjectmodel/IXpsOMImageResourceCollection::RemoveAt
f1_keywords:
- xpsobjectmodel/IXpsOMImageResourceCollection.RemoveAt
dev_langs:
- c++
req.header: xpsobjectmodel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XpsObjectModel.idl
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
- xpsobjectmodel.h
api_name:
- IXpsOMImageResourceCollection.RemoveAt
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IXpsOMImageResourceCollection::RemoveAt


## -description


Removes and releases an <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimageresource">IXpsOMImageResource</a> interface pointer from a specified location in the collection.


## -parameters




### -param index [in]

The zero-based index in the collection from which  an <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimageresource">IXpsOMImageResource</a> interface pointer is to be removed and released.


## -returns



If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



This method releases the interface  referenced by the pointer at  the location specified by <i>index</i>. After releasing the interface, this method compacts the collection by   reducing by 1 the index of each pointer subsequent to <i>index</i>.

For more information about the collection methods, see  <a href="https://docs.microsoft.com/previous-versions/windows/desktop/dd372931(v=vs.85)">Working with XPS OM Collection Interfaces</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimageresource">IXpsOMImageResource</a>



<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimageresourcecollection">IXpsOMImageResourceCollection</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/dd372931(v=vs.85)">Working with XPS OM Collection Interfaces</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 

