---
UID: NE:ksmedia.__unnamed_enum_114
title: KS_AMVP_MODE (ksmedia.h)
description: The KS_AMVP_MODE enumeration defines video port display modes.
old-location: stream\ks_amvp_mode.htm
tech.root: stream
ms.date: 04/23/2018
keywords: ["KS_AMVP_MODE enumeration"]
ms.keywords: KS_AMVP_MODE, KS_AMVP_MODE enumeration [Streaming Media Devices], KS_AMVP_MODE_BOBINTERLEAVED, KS_AMVP_MODE_BOBNONINTERLEAVED, KS_AMVP_MODE_SKIPEVEN, KS_AMVP_MODE_SKIPODD, KS_AMVP_MODE_WEAVE, ksmedia/KS_AMVP_MODE, ksmedia/KS_AMVP_MODE_BOBINTERLEAVED, ksmedia/KS_AMVP_MODE_BOBNONINTERLEAVED, ksmedia/KS_AMVP_MODE_SKIPEVEN, ksmedia/KS_AMVP_MODE_SKIPODD, ksmedia/KS_AMVP_MODE_WEAVE, stream.ks_amvp_mode, vidcapstruct_64634d5e-72a6-4300-9fa9-e1d6859f0813.xml
req.header: ksmedia.h
req.include-header: Ksmedia.h
req.target-type: Windows
req.target-min-winverclnt: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: KS_AMVP_MODE
f1_keywords:
 - KS_AMVP_MODE
 - ksmedia/KS_AMVP_MODE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ksmedia.h
api_name:
 - KS_AMVP_MODE
---

# KS_AMVP_MODE enumeration


## -description

The KS_AMVP_MODE enumeration defines video port display modes.

## -enum-fields

### -field KS_AMVP_MODE_WEAVE

Specifies the weave method to display interlaced video. In the weave mode, alternating fields are combined to form a single frame.

### -field KS_AMVP_MODE_BOBINTERLEAVED

Specifies the interleaved bob method to display video. In the interleaved bob mode, each field is displayed individually, and the gaps between fields are filled with interpolated values.

### -field KS_AMVP_MODE_BOBNONINTERLEAVED

Specifies the non-interleaved bob method to display video.

### -field KS_AMVP_MODE_SKIPEVEN

Specifies that even video fields should be skipped when displaying video.

### -field KS_AMVP_MODE_SKIPODD

Specifies that odd video fields should be skipped when displaying video.

