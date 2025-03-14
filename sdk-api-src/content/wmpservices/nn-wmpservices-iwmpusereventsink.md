---
UID: NN:wmpservices.IWMPUserEventSink
title: IWMPUserEventSink (wmpservices.h)
description: The IWMPUserEventSink interface receives event notifications from a custom video presenter.
old-location: wmp\iwmpusereventsink.htm
tech.root: WMP
ms.assetid: b9afa601-543e-4338-a603-2fe4cd56db36
ms.date: 12/05/2018
ms.keywords: IWMPUserEventSink, IWMPUserEventSink interface [Windows Media Player], IWMPUserEventSink interface [Windows Media Player],described, IWMPUserEventSinkInterface, wmp.iwmpusereventsink, wmpservices/IWMPUserEventSink
f1_keywords:
- wmpservices/IWMPUserEventSink
dev_langs:
- c++
req.header: wmpservices.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- wmpservices.h
api_name:
- IWMPUserEventSink
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPUserEventSink interface


## -description



The <b>IWMPUserEventSink</b> interface receives event notifications from a custom video presenter. An application that embeds the Windows Media Player control, and provides a custom video presenter, can implement the <b>IWMPUserEventSink</b> interface.

The Windows Media Player control retrieves a pointer to the application's <b>IWMPUserEventSink</b> interface by calling <b>IServiceProvider::QueryService</b>, passing __uuidof(IWMPUserEventSink) in the <i>riid</i> parameter. Therefore, an application that implements the <b>IWMPUserEventSink</b> interface must also implement the <b>IServiceProvider</b> interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPUserEventSink</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMPUserEventSink</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMPUserEventSink</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmpservices/nf-wmpservices-iwmpusereventsink-notifyuserevent">NotifyUserEvent</a>
</td>
<td align="left" width="63%">
Notifies an application of an event generated by a custom video presenter that the application provided to the Enhanced Video Renderer (EVR).

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WMP/interfaces">Interfaces</a>
 

 

