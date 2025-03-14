---
UID: NF:strsafe.StringCchCopyNExW
title: StringCchCopyNExW function (strsafe.h)
description: Copies the specified number of characters from one string to another.
old-location: menurc\stringcchcopynex.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\strings\stringreference\stringfunctions\stringcchcopynex.htm
ms.date: 12/05/2018
ms.keywords: STRSAFE_FILL_BEHIND_NULL, STRSAFE_FILL_ON_FAILURE, STRSAFE_IGNORE_NULLS, STRSAFE_NO_TRUNCATION, STRSAFE_NULL_ON_FAILURE, StringCchCopyNEx, StringCchCopyNEx function [Menus and Other Resources], StringCchCopyNExA, StringCchCopyNExW, _shell_StringCchCopyNEx, _shell_stringcchcopynex_cpp, menurc.stringcchcopynex, strsafe/StringCchCopyNEx, strsafe/StringCchCopyNExA, strsafe/StringCchCopyNExW, winui._shell_stringcchcopynex
f1_keywords:
- strsafe/StringCchCopyNEx
dev_langs:
- c++
req.header: strsafe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: StringCchCopyNExW (Unicode) and StringCchCopyNExA (ANSI)
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
- HeaderDef
api_location:
- Strsafe.h
api_name:
- StringCchCopyNEx
- StringCchCopyNExA
- StringCchCopyNExW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# StringCchCopyNExW function


## -description


Copies the specified number of characters from one string to another. The size of the destination buffer is provided to the function to ensure that it does not write past the end of this buffer.

<b>StringCchCopyNEx</b> adds to the functionality of <a href="https://docs.microsoft.com/windows/desktop/api/strsafe/nf-strsafe-stringcchcopyna">StringCchCopyN</a> by returning a pointer to the end of the destination string as well as the number of characters left unused in that string. Flags may also be passed to the function for additional control.

<b>StringCchCopyNEx</b> is a replacement for the following functions:
<ul>
<li><a href="https://go.microsoft.com/fwlink/p/?linkid=192506">strncpy, wcsncpy, _tcsncpy</a></li>
</ul>

## -parameters




### -param pszDest [out]

Type: <b>LPTSTR</b>

The destination buffer, which receives the copied string.


### -param cchDest [in]

Type: <b>size_t</b>

The size of <i>pszDest</i>, in characters. This value must be at least large enough to hold the copied characters (the length of <i>pszSrc</i> or the value of <i>cchSrc</i>, whichever is smaller) plus 1 to account for the terminating null character. The maximum number of characters allowed is <b>STRSAFE_MAX_CCH</b>.


### -param pszSrc [in]

Type: <b>LPCTSTR</b>

The source string. TThis string must be readable up to <i>cchSrc</i> characters or a null terminator, whichever comes first.


### -param cchToCopy [in]

Type: <b>size_t</b>

The maximum number of characters to be copied from <i>pszSrc</i> to <i>pszDest</i>.


### -param ppszDestEnd [out, optional]

Type: <b>LPTSTR*</b>

The address of a pointer to the end of <i>pszDest</i>. If <i>ppszDestEnd</i> is non-<b>NULL</b> and any data is copied into the destination buffer, this points to the terminating null character at the end of the string.


### -param pcchRemaining [out, optional]

Type: <b>size_t*</b>

The number of unused characters in <i>pszDest</i>, including the terminating null character. If <i>pcchRemaining</i> is <b>NULL</b>, the count is not kept or returned.


### -param dwFlags [in]

Type: <b>DWORD</b>

One or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="STRSAFE_FILL_BEHIND_NULL"></a><a id="strsafe_fill_behind_null"></a><dl>
<dt><b>STRSAFE_FILL_BEHIND_NULL</b></dt>
<dt>0x00000200</dt>
</dl>
</td>
<td width="60%">
If the function succeeds, the low byte of <i>dwFlags</i> (0) is used to fill the uninitialized portion of <i>pszDest</i> following the terminating null character.

</td>
</tr>
<tr>
<td width="40%"><a id="STRSAFE_IGNORE_NULLS"></a><a id="strsafe_ignore_nulls"></a><dl>
<dt><b>STRSAFE_IGNORE_NULLS</b></dt>
<dt>0x00000100</dt>
</dl>
</td>
<td width="60%">
Treat <b>NULL</b> string pointers like empty strings (TEXT("")).

</td>
</tr>
<tr>
<td width="40%"><a id="STRSAFE_FILL_ON_FAILURE"></a><a id="strsafe_fill_on_failure"></a><dl>
<dt><b>STRSAFE_FILL_ON_FAILURE</b></dt>
<dt>0x00000400</dt>
</dl>
</td>
<td width="60%">
If the function fails, the low byte of <i>dwFlags</i> (0) is used to fill the entire <i>pszDest</i> buffer, and the buffer is null-terminated. In the case of a <b>STRSAFE_E_INSUFFICIENT_BUFFER</b> failure, any truncated string returned is overwritten.

</td>
</tr>
<tr>
<td width="40%"><a id="STRSAFE_NULL_ON_FAILURE"></a><a id="strsafe_null_on_failure"></a><dl>
<dt><b>STRSAFE_NULL_ON_FAILURE</b></dt>
<dt>0x00000800</dt>
</dl>
</td>
<td width="60%">
If the function fails, <i>pszDest</i> is set to an empty string (TEXT("")). In the case of a <b>STRSAFE_E_INSUFFICIENT_BUFFER</b> failure, any truncated string is overwritten.

</td>
</tr>
<tr>
<td width="40%"><a id="STRSAFE_NO_TRUNCATION"></a><a id="strsafe_no_truncation"></a><dl>
<dt><b>STRSAFE_NO_TRUNCATION</b></dt>
<dt>0x00001000</dt>
</dl>
</td>
<td width="60%">
As in the case of <b>STRSAFE_NULL_ON_FAILURE</b>, if the function fails, <i>pszDest</i> is set to an empty string (TEXT("")). In the case of a <b>STRSAFE_E_INSUFFICIENT_BUFFER</b> failure, any truncated string is overwritten.

</td>
</tr>
</table>
 


## -returns



Type: <b>HRESULT</b>

This function can return one of the following values. It is strongly recommended that you use the <a href="https://docs.microsoft.com/windows/desktop/api/winerror/nf-winerror-succeeded">SUCCEEDED</a> and <a href="https://docs.microsoft.com/windows/desktop/api/winerror/nf-winerror-failed">FAILED</a> macros to test the return value of this function.

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
Source data was present, fully copied without truncation, and the resultant destination buffer is null-terminated.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STRSAFE_E_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
Either <i>pszDest</i> or <i>pszSrc</i> is greater than <b>STRSAFE_MAX_CCH</b>, <i>pszDest</i> is <b>NULL</b> when there is source data present to copy, or an invalid flag was passed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STRSAFE_E_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The copy operation failed due to insufficient buffer space. Depending on the value of <i>dwFlags</i>, the destination buffer may contain a truncated, null-terminated version of the intended result. In situations where truncation is acceptable, this may not necessarily be seen as a failure condition.

</td>
</tr>
</table>
 

Note that this function returns an <b>HRESULT</b> value, unlike the functions that it replaces.




## -remarks



<b>StringCchCopyNEx</b> provides additional processing for proper buffer handling in your code. Poor buffer handling is implicated in many security issues that involve buffer overruns. <b>StringCchCopyNEx</b>always null-terminates and never overflows a valid destination buffer, even if the contents of the source string change during the operation.

While this routine is meant as a replacement for <a href="https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/xdsywd25(v=vs.100)">strncpy</a>, there are differences in behavior. If <i>cchSrc</i> is larger than the number of characters in <i>pszSrc</i>, <b>StringCchCopyNEx</b>—unlike <b>strncpy</b>—does not continue to pad <i>pszDest</i> with null characters until <i>cchSrc</i> characters have been copied.

Behavior is undefined if the strings pointed to by <i>pszSrc</i> and <i>pszDest</i> overlap.

Neither <i>pszSrc</i> nor <i>pszDest</i> should be <b>NULL</b> unless the <b>STRSAFE_IGNORE_NULLS</b> flag is specified, in which case both may be <b>NULL</b>. However, an error due to insufficient space may still be returned even though <b>NULL</b> values are ignored.

<b>StringCchCopyNEx</b> can be used in its generic form, or in its more specific forms. The data type of the string determines the form of this function that you should use, as shown in the following table.

<table class="clsStd">
<tr>
<th>String Data Type</th>
<th>String Literal</th>
<th>Function</th>
</tr>
<tr>
<td><b>char</b></td>
<td>"string"</td>
<td><b>StringCchCopyNExA</b></td>
</tr>
<tr>
<td><b>TCHAR</b></td>
<td>TEXT("string")</td>
<td><b>StringCchCopyNEx</b></td>
</tr>
<tr>
<td><b>WCHAR</b></td>
<td>L"string"</td>
<td><b>StringCchCopyNExW</b></td>
</tr>
</table>
 




## -see-also




<b>Reference</b>



<a href="https://docs.microsoft.com/windows/desktop/api/strsafe/nf-strsafe-stringcbcopynexa">StringCbCopyNEx</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strsafe/nf-strsafe-stringcchcopyna">StringCchCopyN</a>
 

 

