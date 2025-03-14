---
UID: NF:dbghelp.SymEnumSourceLines
title: SymEnumSourceLines function (dbghelp.h)
description: Enumerates all source lines in a module.
old-location: base\symenumsourcelines.htm
tech.root: Debug
ms.assetid: 395dd97b-4d0b-4f55-80af-38fc748c924a
ms.date: 12/05/2018
ms.keywords: SymEnumSourceLines, SymEnumSourceLines function, SymEnumSourceLinesW, base.symenumsourcelines, dbghelp/SymEnumSourceLines, dbghelp/SymEnumSourceLinesW
f1_keywords:
- dbghelp/SymEnumSourceLines
dev_langs:
- c++
req.header: dbghelp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SymEnumSourceLinesW (Unicode) and SymEnumSourceLines (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dbghelp.lib
req.dll: Dbghelp.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Dbghelp.dll
api_name:
- SymEnumSourceLines
- SymEnumSourceLines
- SymEnumSourceLinesW
targetos: Windows
req.typenames: 
req.redist: DbgHelp.dll 6.4 or later
ms.custom: 19H1
---

# SymEnumSourceLines function


## -description


Enumerates all source lines in a module.


## -parameters




### -param hProcess [in]

A handle to a process. This handle must have been previously passed to the 
<a href="https://docs.microsoft.com/windows/desktop/api/dbghelp/nf-dbghelp-syminitialize">SymInitialize</a> function.


### -param Base [in]

The base address of the module.


### -param Obj [in, optional]

The name of an .obj file within the module. The scope of the enumeration is limited to this file. If this parameter is <b>NULL</b> or an empty string, all .obj files are searched. 


### -param File [in, optional]

A wildcard expression that indicates the names of the source files to be searched. If this parameter is <b>NULL</b> or an empty string, all files are searched.


### -param Line [in, optional]

The line number of a line within the module. The scope of the enumeration is limited to this line. If this parameter is 0, all lines are searched.


### -param Flags [in]

If this parameter is ESLFLAG_FULLPATH, the function matches the full path in the <i>File</i> parameter.


### -param EnumLinesCallback [in]

A 
<a href="https://docs.microsoft.com/windows/desktop/api/dbghelp/nc-dbghelp-psym_enumlines_callback">SymEnumLinesProc</a> callback function that receives the line information.


### -param UserContext [in, optional]

A user-defined value that is passed to the callback function, or <b>NULL</b>. This parameter is typically used by an application to pass a pointer to a data structure that provides context for the callback function.


## -returns



If the function succeeds, the return value is <b>TRUE</b>.
						

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dbghelp/nc-dbghelp-psym_enumlines_callback">SymEnumLinesProc</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dbghelp/nf-dbghelp-syminitialize">SymInitialize</a>
 

 

