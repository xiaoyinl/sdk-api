---
UID: NN:bdaiface.IBDA_ISDBConditionalAccess
title: IBDA_ISDBConditionalAccess (bdaiface.h)
description: Sends conditional access system (CAS) commands for Integrated Services Digital Broadcasting (ISDB).
old-location: mstv\ibda_isdbconditionalaccess.htm
tech.root: mstv
ms.assetid: 0e45e5ea-9f38-4a96-be44-8ee123492aa9
ms.date: 12/05/2018
ms.keywords: IBDA_ISDBConditionalAccess, IBDA_ISDBConditionalAccess interface [Microsoft TV Technologies], IBDA_ISDBConditionalAccess interface [Microsoft TV Technologies],described, bdaiface/IBDA_ISDBConditionalAccess, mstv.ibda_isdbconditionalaccess
f1_keywords:
- bdaiface/IBDA_ISDBConditionalAccess
dev_langs:
- c++
req.header: bdaiface.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bdaiface.idl
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
- bdaiface.h
api_name:
- IBDA_ISDBConditionalAccess
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IBDA_ISDBConditionalAccess interface


## -description


Sends conditional access system (CAS) commands for Integrated Services Digital Broadcasting (ISDB).

For more information, refer to ARIB STD-B25, <i>Conditional Access System Specifications for Digital Broadcasting</i>. (This resource may not be available in some languages 

and countries.)


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBDA_ISDBConditionalAccess</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IBDA_ISDBConditionalAccess</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IBDA_ISDBConditionalAccess</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_isdbconditionalaccess-setisdbcasrequest">SetIsdbCasRequest</a>
</td>
<td align="left" width="63%">
Sends a CAS command.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IBDA_ISDBConditionalAccess)</code>.



