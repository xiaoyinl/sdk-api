---
UID: NF:xpsobjectmodel.IXpsOMPath.SetAccessibilityLongDescription
title: IXpsOMPath::SetAccessibilityLongDescription (xpsobjectmodel.h)
description: Sets the long (detailed) textual description of the object's contents.
old-location: xps\ixpsompath_setaccessibilitylongdescription.htm
tech.root: printdocs
ms.assetid: 9727cbea-55f7-48ad-8205-d68d0c906250
ms.date: 12/05/2018
ms.keywords: IXpsOMPath interface [XPS Documents and Packaging],SetAccessibilityLongDescription method, IXpsOMPath.SetAccessibilityLongDescription, IXpsOMPath::SetAccessibilityLongDescription, SetAccessibilityLongDescription, SetAccessibilityLongDescription method [XPS Documents and Packaging], SetAccessibilityLongDescription method [XPS Documents and Packaging],IXpsOMPath interface, xps.ixpsompath_setaccessibilitylongdescription, xpsobjectmodel/IXpsOMPath::SetAccessibilityLongDescription
f1_keywords:
- xpsobjectmodel/IXpsOMPath.SetAccessibilityLongDescription
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
- IXpsOMPath.SetAccessibilityLongDescription
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IXpsOMPath::SetAccessibilityLongDescription


## -description


Sets the long (detailed) textual description of the object's contents. This description is used by accessibility clients to describe the object.


## -parameters




### -param longDescription [in]

The detailed textual description of the object's contents.


## -returns



If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



In the document markup, the value that is set in <i>longDescription</i> will be that of  the <b>AutomationProperties.HelpText</b> attribute of the  <b>Path</b> element.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath">IXpsOMPath</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 

