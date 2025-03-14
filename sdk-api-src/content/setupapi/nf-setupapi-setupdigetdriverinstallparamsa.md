---
UID: NF:setupapi.SetupDiGetDriverInstallParamsA
title: SetupDiGetDriverInstallParamsA function (setupapi.h)
description: The SetupDiGetDriverInstallParams function retrieves driver installation parameters for a device information set or a particular device information element.
old-location: devinst\setupdigetdriverinstallparams.htm
tech.root: devinst
ms.assetid: 7c5b0e3f-75cd-48e1-b84e-d81e4e4db7b2
ms.date: 12/05/2018
ms.keywords: SetupDiGetDriverInstallParams, SetupDiGetDriverInstallParams function [Device and Driver Installation], SetupDiGetDriverInstallParamsA, SetupDiGetDriverInstallParamsW, devinst.setupdigetdriverinstallparams, di-rtns_b8e7fdca-3201-42f9-86b4-a8a97be8cb90.xml, setupapi/SetupDiGetDriverInstallParams
f1_keywords:
- setupapi/SetupDiGetDriverInstallParams
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
- SetupDiGetDriverInstallParams - SetupDiGetDriverInstallParamsA
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SetupDiGetDriverInstallParamsA function


## -description


The <b>SetupDiGetDriverInstallParams</b> function retrieves driver installation parameters for a device information set or a particular device information element.


## -parameters




### -param DeviceInfoSet [in]

A handle to a <a href="https://docs.microsoft.com/windows-hardware/drivers/install/device-information-sets">device information set</a> that contains a driver information element that represents the driver for which to retrieve installation parameters.


### -param DeviceInfoData [in, optional]

A pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/setupapi/ns-setupapi-sp_devinfo_data">SP_DEVINFO_DATA</a> structure that contains a device information element that represents the device for which to retrieve installation parameters. This parameter is optional and can be <b>NULL</b>. If this parameter is specified, <b>SetupDiGetDriverInstallParams</b> retrieves information about a driver that is a member of a driver list for the specified device. If this parameter is <b>NULL</b>, <b>SetupDiGetDriverInstallParams</b> retrieves information about a driver  that is a member of the global class driver list for <i>DeviceInfoSet</i>.


### -param DriverInfoData [in]

A pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/setupapi/ns-setupapi-sp_drvinfo_data_v1_a">SP_DRVINFO_DATA</a> structure that specifies the driver information element that represents the driver for which to retrieve installation parameters. If <i>DeviceInfoData</i> is supplied, the driver must be a member of the driver list for the device that is specified by <i>DeviceInfoData</i>. Otherwise, the driver must be a member of the global class driver list for <i>DeviceInfoSet</i>.


### -param DriverInstallParams [out]

A pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/setupapi/ns-setupapi-sp_drvinstall_params">SP_DRVINSTALL_PARAMS</a> structure to receive the installation parameters for this driver. 


## -returns



The function returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b> and the logged error can be retrieved by a call to <a href="https://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/setupapi/nf-setupapi-setupdisetdriverinstallparamsa">SetupDiSetDriverInstallParams</a>
 

 

