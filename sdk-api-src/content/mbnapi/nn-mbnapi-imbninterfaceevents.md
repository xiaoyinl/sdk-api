---
UID: NN:mbnapi.IMbnInterfaceEvents
title: IMbnInterfaceEvents (mbnapi.h)
description: This interface is a notification interface used to handle asynchronous IMbnInterface method calls as well as changes in the device state.
old-location: mbn\imbninterfaceevents.htm
tech.root: mbn
ms.assetid: 3c641f14-9f53-4d69-9faa-2491189083df
ms.date: 12/05/2018
ms.keywords: IMbnInterfaceEvents, IMbnInterfaceEvents interface [Microsoft Broadband Networks], IMbnInterfaceEvents interface [Microsoft Broadband Networks],described, mbn.imbninterfaceevents, mbnapi/IMbnInterfaceEvents
f1_keywords:
- mbnapi/IMbnInterfaceEvents
dev_langs:
- c++
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mbnapi.idl
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
- mbnapi.h
api_name:
- IMbnInterfaceEvents
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMbnInterfaceEvents interface


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

This interface is a notification interface used to handle asynchronous <a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nn-mbnapi-imbninterface">IMbnInterface</a> method calls as well as changes in the device state.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMbnInterfaceEvents</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMbnInterfaceEvents</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMbnInterfaceEvents</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbninterfaceevents-onemergencymodechange">OnEmergencyModeChange</a>
</td>
<td align="left" width="63%">
The emergency mode has changed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbninterfaceevents-onhomeprovideravailable">OnHomeProviderAvailable</a>
</td>
<td align="left" width="63%">
Home provider information is available.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbninterfaceevents-oninterfacecapabilityavailable">OnInterfaceCapabilityAvailable</a>
</td>
<td align="left" width="63%">
Device capability information is available.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbninterfaceevents-onpreferredproviderschange">OnPreferredProvidersChange</a>
</td>
<td align="left" width="63%">
The list of preferred providers has changed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbninterfaceevents-onreadystatechange">OnReadyStateChange</a>
</td>
<td align="left" width="63%">
The ready state has changed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbninterfaceevents-onscannetworkcomplete">OnScanNetworkComplete</a>
</td>
<td align="left" width="63%">
An operation to scan the network has completed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbninterfaceevents-onsetpreferredproviderscomplete">OnSetPreferredProvidersComplete</a>
</td>
<td align="left" width="63%">
An operation to change the preferred provider completed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbninterfaceevents-onsubscriberinformationchange">OnSubscriberInformationChange</a>
</td>
<td align="left" width="63%">
The subscriber information has changed.

</td>
</tr>
</table> 


## -remarks



The following procedure describes how to register for notifications.

<ol>
<li>Get an <a href="https://go.microsoft.com/fwlink/p/?linkid=109916">IConnectionPointContainer</a>  interface by calling <b>QueryInterface</b> on an <a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nn-mbnapi-imbninterfacemanager">IMbnInterfaceManager</a> object.</li>
<li>Call <a href="https://go.microsoft.com/fwlink/p/?linkid=109922">FindConnectionPoint</a> on the returned interface and pass <b>IID_IMbnInterfaceEvents</b> to <i>riid</i>.</li>
<li>Call <a href="https://go.microsoft.com/fwlink/p/?linkid=109923">Advise</a> on the returned connection point and pass a pointer to an <b>IUnknown</b> interface on an object that implements <b>IMbnInterfaceEvents</b> to <i>pUnk</i>.</li>
</ol>
Notifications can be terminated by calling <a href="https://go.microsoft.com/fwlink/p/?linkid=109924">Unadvise</a> on the connection point returned in step 2.

To view some code that registers for COM notifications, see the Client section of the <a href="https://docs.microsoft.com/en-us/archive/msdn-magazine/2007/september/clr-inside-out-com-connection-points">COM Connection Points</a> article.



