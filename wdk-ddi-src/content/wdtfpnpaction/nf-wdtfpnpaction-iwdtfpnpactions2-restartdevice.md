---
UID: NF:wdtfpnpaction.IWDTFPNPActions2.RestartDevice
title: IWDTFPNPActions2::RestartDevice (wdtfpnpaction.h)
description: Learn how the method initiates a device restart.
old-location: dtf\iwdtfpnpactions2_restartdevice.htm
tech.root: dtf
ms.date: 04/04/2018
keywords: ["IWDTFPNPActions2::RestartDevice"]
ms.keywords: IWDTFPNPActions2 interface [Windows Device Testing Framework],RestartDevice method, IWDTFPNPActions2.RestartDevice, IWDTFPNPActions2::RestartDevice, RestartDevice, RestartDevice method [Windows Device Testing Framework], RestartDevice method [Windows Device Testing Framework],IWDTFPNPActions2 interface, dtf.iwdtfpnpactions2_restartdevice, wdtfpnpaction/IWDTFPNPActions2::RestartDevice
req.header: wdtfpnpaction.h
req.include-header: 
req.target-type: Desktop
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WDTFPNPAction.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
f1_keywords:
 - IWDTFPNPActions2::RestartDevice
 - wdtfpnpaction/IWDTFPNPActions2::RestartDevice
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wdtfpnpaction.h
api_name:
 - IWDTFPNPActions2::RestartDevice
---

# IWDTFPNPActions2::RestartDevice


## -description

Initiates a device restart.

## -parameters

### -param pbSuccess 

[out, retval]
True if the operation succeeds; otherwise, false.

## -returns

If this method succeeds, it returns **S_OK**. Otherwise, it returns an **HRESULT** error code.

## -remarks

From a SetupDi interface perspective, this will translate to a DICS_PROPCHANGE.   
See the MSDN docs for details.

