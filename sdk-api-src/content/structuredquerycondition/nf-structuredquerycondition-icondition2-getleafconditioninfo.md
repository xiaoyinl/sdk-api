---
UID: NF:structuredquerycondition.ICondition2.GetLeafConditionInfo
title: ICondition2::GetLeafConditionInfo (structuredquerycondition.h)
description: Retrieves the property name, operation, and value from a leaf search condition node.
old-location: search\_search_ICondition2_GetLeafConditionInfo.htm
tech.root: search
ms.assetid: VS|SEARCH|~\search\wds3x\reference\ifaces\querying\icondition2\getleafconditioninfo.htm
ms.date: 12/05/2018
ms.keywords: GetLeafConditionInfo, GetLeafConditionInfo method [search], GetLeafConditionInfo method [search],ICondition2 interface, ICondition2 interface [search],GetLeafConditionInfo method, ICondition2.GetLeafConditionInfo, ICondition2::GetLeafConditionInfo, _search_ICondition2_GetLeafConditionInfo, search._search_ICondition2_GetLeafConditionInfo, structuredquerycondition/ICondition2::GetLeafConditionInfo
f1_keywords:
- structuredquerycondition/ICondition2.GetLeafConditionInfo
dev_langs:
- c++
req.header: structuredquerycondition.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Structuredquerycondition.idl
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
- Structuredquerycondition.h
api_name:
- ICondition2.GetLeafConditionInfo
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICondition2::GetLeafConditionInfo


## -description


Retrieves the property name, operation, and value from a leaf search condition node.
        


## -parameters




### -param ppropkey [out, optional]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/wtypes/ns-wtypes-propertykey">PROPERTYKEY</a>*</b>

Receives the name of the property of the leaf condition as a PROPERTYKEY.
                


### -param pcop [out, optional]

Type: <b><a href="https://docs.microsoft.com/windows/win32/api/structuredquerycondition/ne-structuredquerycondition-condition_operation">CONDITION_OPERATION</a>*</b>

Receives the operation of the leaf condition as a <a href="https://docs.microsoft.com/windows/win32/api/structuredquerycondition/ne-structuredquerycondition-condition_operation">CONDITION_OPERATION</a> enumeration.
                


### -param ppropvar [out, optional]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>*</b>

Receives the property value of the leaf condition as a <a href="https://docs.microsoft.com/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>. 
                


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, E_FAIL if this is not a leaf node, or an error value otherwise.




## -remarks



Any or all of the three parameters can be <b>NULL</b>.

The StructuredQuerySample code sample, available on <a href="https://go.microsoft.com/fwlink/p/?linkid=155654">Code Gallery</a> and the <a href="https://go.microsoft.com/fwlink/p/?linkid=129787">Windows 7 SDK</a>, demonstrates how to read lines from the console, parse them using the system schema, and display the resulting 
condition trees.




## -see-also




<a href="https://docs.microsoft.com/windows/win32/api/structuredquerycondition/ne-structuredquerycondition-condition_operation">CONDITION_OPERATION</a>



<a href="https://docs.microsoft.com/windows/win32/api/structuredquerycondition/ne-structuredquerycondition-condition_type">CONDITION_TYPE</a>



<a href="https://docs.microsoft.com/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition">ICondition</a>



<a href="https://docs.microsoft.com/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition2">ICondition2</a>



<b>Reference</b>
 

 

