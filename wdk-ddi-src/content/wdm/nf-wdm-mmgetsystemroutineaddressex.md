---
UID: NF:wdm.MmGetSystemRoutineAddressEx
title: MmGetSystemRoutineAddressEx function
description: The MmGetSystemRoutineAddressEx function returns the address of the specified function in the specified system module.
tech.root: kernel
ms.date: 03/01/2020
ms.keywords: MmGetSystemRoutineAddressEx
req.header: wdm.h
req.include-header: 
req.target-type: 
req.target-min-winverclnt: Xbox
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.lib: 
req.dll: 
req.irql: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
targetos: Windows
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - wdm.h
api_name:
 - MmGetSystemRoutineAddressEx
product:
 - Windows
f1_keywords:
 - MmGetSystemRoutineAddressEx
 - wdm/MmGetSystemRoutineAddressEx
---

# MmGetSystemRoutineAddressEx function

## -description

The **MmGetSystemRoutineAddressEx** function returns the address of the specified function in the specified system module.

## -parameters

### -param ModuleName

Supplies a pointer to a **UNICODE_STRING** that describes the system module.

### -param FunctionName

Supplies a pointer to the name of the desired function.

## -returns

If the specified module is not in the loaded module list, the specified loaded module is the kernel or the HAL, or the specified function cannot be located, then NULL is returned. Otherwise, the appropriate bit is set in the CFG bitmap and a pointer to the specified function is returned.

## -remarks

## -see-also
