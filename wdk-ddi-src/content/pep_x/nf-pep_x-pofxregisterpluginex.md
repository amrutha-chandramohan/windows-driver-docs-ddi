---
UID: NF:pep_x.PoFxRegisterPluginEx
title: PoFxRegisterPluginEx function (pep_x.h)
description: Learn how the PoFxRegisterPluginEx routine registers a platform extension plug-in (PEP) with the Windows power management framework (PoFx).
old-location: kernel\pofxregisterpluginex.htm
tech.root: kernel
ms.date: 04/30/2018
keywords: ["PoFxRegisterPluginEx function"]
ms.keywords: PoFxRegisterPluginEx, PoFxRegisterPluginEx routine [Kernel-Mode Driver Architecture], kernel.pofxregisterpluginex, pepfx/PoFxRegisterPluginEx
req.header: pep_x.h
req.include-header: Pep_x.h
req.target-type: Windows
req.target-min-winverclnt: Available starting with Windows 10.
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
req.lib: Ntoskrnl.lib
req.dll: 
req.irql: PASSIVE_LEVEL
targetos: Windows
req.typenames: 
f1_keywords:
 - PoFxRegisterPluginEx
 - pep_x/PoFxRegisterPluginEx
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - ntoskrnl.lib
 - ntoskrnl.dll
api_name:
 - PoFxRegisterPluginEx
---

# PoFxRegisterPluginEx function (pep_x.h)


## -description

The <b>PoFxRegisterPluginEx</b> routine registers a platform extension plug-in (PEP) with the Windows <a href="/windows-hardware/drivers/ddi/_kernel/#device-power-management">power management framework</a> (PoFx).

## -parameters

### -param PepInformation 

[in]
A pointer to a <a href="/windows-hardware/drivers/ddi/pepfx/ns-pepfx-_pep_information">PEP_INFORMATION</a> structure that contains pointers to one or more callback routines that are implemented by the PEP. These routines handle notifications that are sent to the PEP by PoFx.

### -param Flags 

[in]
A set of flag bits for configuring the PEP interface. Set this member to zero or to the following value.

<table>
<tr>
<th>Flag bit</th>
<th>Description</th>
</tr>
<tr>
<td>PEP_FLAG_WORKER_CONCURRENCY</td>
<td></td>
</tr>
</table>

### -param KernelInformation 

[in, out]
A pointer to a <a href="/windows-hardware/drivers/ddi/pep_x/ns-pep_x-_pep_kernel_information_struct_v1">PEP_KERNEL_INFORMATION</a> structure.

## -returns

<b>PoFxRegisterPluginEx</b> returns STATUS_SUCCESS if the call successfully registers the PEP. Possible error return values include the following status codes.

<table>
<tr>
<th>Return value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>STATUS_INVALID_PARAMETER</dt>
</dl>
</td>
<td width="60%">
The <b>Version</b> or <b>Size</b> member of the <b>PEP_KERNEL_INFORMATION</b> structure is set to an invalid value; or the <b>AcceptDeviceNotification</b> member of this structure is set to NULL.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>STATUS_INVALID_PEP_INFO_VERSION</dt>
</dl>
</td>
<td width="60%">
The <b>Version</b> member of the <b>PEP_INFORMATION</b> structure is set to an invalid value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>STATUS_INSUFFICIENT_RESOURCES</dt>
</dl>
</td>
<td width="60%">
Unable to allocate the resources required to complete the requested registration.

</td>
</tr>
</table>

## -remarks

A PEP calls this routine to register itself with PoFx.

A PEP cannot unregister, and cannot register twice. If the PEP must be serviced, the operating system must restart.

The <a href="/windows-hardware/drivers/ddi/pepfx/nf-pepfx-pofxregisterplugin">PoFxRegisterPlugin</a> routine is similar to <b>PoFxRegisterPluginEx</b>, except that it does not take a <i>Flags</i> parameter.

The PEP must call <b>PoFxRegisterPluginEx</b> at IRQL = PASSIVE_LEVEL.

## -see-also

<a href="/windows-hardware/drivers/ddi/pepfx/ns-pepfx-_pep_information">PEP_INFORMATION</a>



<a href="/windows-hardware/drivers/ddi/pep_x/ns-pep_x-_pep_kernel_information_struct_v1">PEP_KERNEL_INFORMATION</a>



<a href="/windows-hardware/drivers/ddi/pepfx/nf-pepfx-pofxregisterplugin">PoFxRegisterPlugin</a>
