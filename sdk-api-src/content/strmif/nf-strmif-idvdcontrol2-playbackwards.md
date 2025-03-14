---
UID: NF:strmif.IDvdControl2.PlayBackwards
title: IDvdControl2::PlayBackwards (strmif.h)
description: The PlayBackwards method plays backward at the specified speed from the current location.
old-location: dshow\idvdcontrol2_playbackwards.htm
tech.root: DirectShow
ms.assetid: d195956b-a4e5-493f-a804-9095e3bba4e2
ms.date: 12/05/2018
ms.keywords: IDvdControl2 interface [DirectShow],PlayBackwards method, IDvdControl2.PlayBackwards, IDvdControl2::PlayBackwards, IDvdControl2PlayBackwards, PlayBackwards, PlayBackwards method [DirectShow], PlayBackwards method [DirectShow],IDvdControl2 interface, dshow.idvdcontrol2_playbackwards, strmif/IDvdControl2::PlayBackwards
f1_keywords:
- strmif/IDvdControl2.PlayBackwards
dev_langs:
- c++
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
api_name:
- IDvdControl2.PlayBackwards
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDvdControl2::PlayBackwards


## -description



The <code>PlayBackwards</code> method plays backward at the specified speed from the current location.




## -parameters




### -param dSpeed [in]

Value that specifies the speed of backward play. This value is a multiplier, where 1.0 is the authored speed. So, a value of 2.5 plays backward at two and one-half times the authored speed, while a value of 0.5 plays backward at half the authored speed. The actual speed of playback depends on the video decoder's capabilities and might differ from the specified rate. For reverse play, audio is muted and no subpicture is displayed. Any speed below 0.00001 is converted to 0.00001.


### -param dwFlags [in]

Bitwise <b>OR</b> of one or more flags from the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/ne-strmif-dvd_cmd_flags">DVD_CMD_FLAGS</a> enumeration, specifying how to synchronize the command.


### -param ppCmd [out]

Receives a pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-idvdcmd">IDvdCmd</a> object that can be used to synchronize DVD commands. The caller must release the interface. This parameter can be <b>NULL</b>. For more information, see <a href="https://docs.microsoft.com/windows/desktop/DirectShow/synchronizing-dvd-commands">Synchronizing DVD Commands</a>.


## -returns



Returns one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_DVD_OPERATION_INHIBITED</b></dt>
</dl>
</td>
<td width="60%">
UOP control prohibits the operation.

</td>
</tr>
</table>
 




## -remarks



This method is demonstrated in the DVDSample application in <b>CDvdCore::Rewind</b>.

The following table shows the Annex J command name to which this method name corresponds, and the domains in which this method is valid.

<table>
<tr>
<td>Annex J Command Name
            </td>
<td>Valid Domains
            </td>
</tr>
<tr>
<td>Backward_Scan</td>
<td>
<ul>
<li>DVD_DOMAIN_VideoManagerMenu</li>
<li>DVD_DOMAIN_VideoTitleSetMenu</li>
<li>DVD_DOMAIN_Title</li>
</ul>
</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/dvd-applications">DVD Applications</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-idvdcontrol2">IDvdControl2 Interface</a>
 

 

