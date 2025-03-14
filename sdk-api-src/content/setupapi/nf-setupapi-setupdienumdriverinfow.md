---
UID: NF:setupapi.SetupDiEnumDriverInfoW
title: SetupDiEnumDriverInfoW function (setupapi.h)
description: The SetupDiEnumDriverInfo function enumerates the members of a driver list.
old-location: devinst\setupdienumdriverinfo.htm
tech.root: devinst
ms.assetid: c4a66d0c-e9a9-41f8-87df-576795667b5c
ms.date: 12/05/2018
ms.keywords: SetupDiEnumDriverInfo, SetupDiEnumDriverInfo function [Device and Driver Installation], SetupDiEnumDriverInfoA, SetupDiEnumDriverInfoW, devinst.setupdienumdriverinfo, di-rtns_8d84a225-9dac-4ab3-8c9a-5048284d82be.xml, setupapi/SetupDiEnumDriverInfo
f1_keywords:
- setupapi/SetupDiEnumDriverInfo
dev_langs:
- c++
req.header: setupapi.h
req.include-header: Setupapi.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Microsoft Windows 2000 and later versions of Windows.
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
req.lib: Setupapi.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- LibDef
api_location:
- Setupapi.lib
- Setupapi.dll
api_name:
- SetupDiEnumDriverInfo - SetupDiEnumDriverInfoW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SetupDiEnumDriverInfoW function


## -description


The <b>SetupDiEnumDriverInfo</b> function enumerates the members of a driver list.


## -parameters




### -param DeviceInfoSet [in]

A handle to the <a href="https://docs.microsoft.com/windows-hardware/drivers/install/device-information-sets">device information set</a> that contains the driver list to enumerate.


### -param DeviceInfoData [in, optional]

 A pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/setupapi/ns-setupapi-sp_devinfo_data">SP_DEVINFO_DATA</a> structure that specifies a device information element in <i>DeviceInfoSet</i>. This parameter is optional and can be <b>NULL</b>. If this parameter is specified, <b>SetupDiEnumDriverInfo</b> enumerates a driver list for the specified device. If this parameter is <b>NULL</b>, <b>SetupDiEnumDriverInfo</b> enumerates the global class driver list that is associated with <i>DeviceInfoSet</i> (this list is of type SPDIT_CLASSDRIVER).


### -param DriverType [in]

The type of driver list to enumerate, which must be one of the following values:





#### SPDIT_CLASSDRIVER

Enumerate a class driver list. This driver list type must be specified if <i>DeviceInfoData</i> is not specified.



#### SPDIT_COMPATDRIVER

Enumerate a list of compatible drivers for the specified device. This driver list type can be specified only if <i>DeviceInfoData</i> is also specified.


### -param MemberIndex [in]

The zero-based index of the driver information member to retrieve.


### -param DriverInfoData [out]

A pointer to a caller-initialized <a href="https://docs.microsoft.com/windows/desktop/api/setupapi/ns-setupapi-sp_drvinfo_data_v1_a">SP_DRVINFO_DATA</a> structure that receives information about the enumerated driver. The caller must set <i>DriverInfoData.</i><b>cbSize</b> to <b>sizeof(</b>SP_DRVINFO_DATA<b>)</b> before calling <b>SetupDiEnumDriverInfo</b>. If the <b>cbSize</b> member is not properly set, <b>SetupDiEnumDriverInfo</b> will return <b>FALSE</b>.  


##### - DriverType.SPDIT_CLASSDRIVER

Enumerate a class driver list. This driver list type must be specified if <i>DeviceInfoData</i> is not specified.


##### - DriverType.SPDIT_COMPATDRIVER

Enumerate a list of compatible drivers for the specified device. This driver list type can be specified only if <i>DeviceInfoData</i> is also specified.


## -returns



The function returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b> and the logged error can be retrieved with a call to <a href="https://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a>.




## -remarks



To enumerate driver information set members, an installer should first call <b>SetupDiEnumDriverInfo</b> with the <i>MemberIndex</i> parameter set to 0. It should then increment <i>MemberIndex</i> and call <b>SetupDiEnumDriverInfo</b> until there are no more values. When there are no more values, the function fails and a call to <a href="https://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a> returns ERROR_NO_MORE_ITEMS.

If you do not properly initialize the <b>cbSize</b> member of the SP_DRVINFO_DATA structure that is supplied by the pointer <i>DriverInfoData</i>, the function will fail and log the error ERROR_INVALID_USER_BUFFER.

To build a list of drivers associated with a specific device or with the global class driver list for a device information set first use <a href="https://docs.microsoft.com/windows/desktop/api/setupapi/nf-setupapi-setupdibuilddriverinfolist">SetupDiBuildDriverInfoList</a> then pass that list to <b>SetupDiEnumDriverInfo</b>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/setupapi/nf-setupapi-setupdibuilddriverinfolist">SetupDiBuildDriverInfoList</a>
 

 

