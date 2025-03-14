---
UID: NF:wmsdkidl.IWMDRMTranscryptor.Read
title: IWMDRMTranscryptor::Read (wmsdkidl.h)
description: The Read method reads data from the file loaded in the transcryptor and encrypts it for streaming to devices that support Windows Media DRM 10 for Network Devices.
old-location: wmformat\iwmdrmtranscryptor_read.htm
tech.root: wmformat
ms.assetid: 55b1c73a-5c00-4e16-b0fe-2352ce09bffc
ms.date: 12/05/2018
ms.keywords: IWMDRMTranscryptor interface [windows Media Format],Read method, IWMDRMTranscryptor.Read, IWMDRMTranscryptor::Read, IWMDRMTranscryptorRead, Read, Read method [windows Media Format], Read method [windows Media Format],IWMDRMTranscryptor interface, wmformat.iwmdrmtranscryptor_read, wmsdkidl/IWMDRMTranscryptor::Read
f1_keywords:
- wmsdkidl/IWMDRMTranscryptor.Read
dev_langs:
- c++
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only],Windows Media Format 9.5 SDK
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
req.lib: WMStubDRM.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- WMStubDRM.lib
- WMStubDRM.dll
api_name:
- IWMDRMTranscryptor.Read
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMDRMTranscryptor::Read


## -description


<p class="CCE_Message">[<b>Read</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://go.microsoft.com/fwlink/p/?linkid=325240">Microsoft PlayReady</a>.
]


The <b>Read</b> method reads data from the file loaded in the transcryptor and encrypts it for streaming to devices that support Windows Media DRM 10 for Network Devices.




## -parameters




### -param pbData [in]

Address of a buffer that receives the data.


### -param pcbData [in, out]

Address of a variable containing the size of the data buffer pointed to by <i>pbData</i>. On input, set to the size of the buffer.On output, the value is changed to the number of bytes actually read.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_INVALID_REQUEST</b></dt>
</dl>
</td>
<td width="60%">
The transcryptor is not ready for reading.

OR

Another read is in progress.

</td>
</tr>
</table>
 




## -remarks



This method is asynchronous. It returns immediately, but processing is not complete until a WMT_TRANSCRYPTOR_READ message is sent to the <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus">IWMStatusCallback::OnStatus</a> callback method. Neither the buffer referenced by <i>pbData</i> nor the buffer length referenced by <i>pcbData</i> are updated until the WMT_TRANSCRYPTOR_READ message is sent.

The <b>HRESULT</b> sent with the WMT_TRANSCRYPTOR_READ message contains the return value for the read operation. A special success code, NS_S_TRANSCRYPTOR_EOF, is sent to indicate that the data from this read operation includes the end of the file.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmtranscryptor">IWMDRMTranscryptor Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmdrmtranscryptor-close">IWMDRMTranscryptor::Close</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmdrmtranscryptor-initialize">IWMDRMTranscryptor::Initialize</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmdrmtranscryptor-seek">IWMDRMTranscryptor::Seek</a>
 

 

