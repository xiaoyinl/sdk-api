---
UID: NS:windns.__unnamed_struct_32
title: DNS_NAPTR_DATAW (windns.h)
description: The DNS_NAPTR_DATA structure represents a Naming Authority Pointer (NAPTR) DNS Resource Record (RR) as specified in RFC 2915.
old-location: dns\dns_naptr_data.htm
tech.root: DNS
ms.assetid: 8f576efb-4ef3-4fc0-8cf5-d373460a3b3c
ms.date: 12/05/2018
ms.keywords: '*PDNS_NAPTR_DATA, *PDNS_NAPTR_DATAW, DNS_NAPTR_DATA, DNS_NAPTR_DATA structure [DNS], DNS_NAPTR_DATAW, PDNS_NAPTR_DATA, PDNS_NAPTR_DATA structure pointer [DNS], dns.dns_naptr_data, windns/DNS_NAPTR_DATA, windns/PDNS_NAPTR_DATA'
f1_keywords:
- windns/DNS_NAPTR_DATA
dev_langs:
- c++
req.header: windns.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Windns.h
api_name:
- DNS_NAPTR_DATA
targetos: Windows
req.typenames: DNS_NAPTR_DATAW, *PDNS_NAPTR_DATAW
req.redist: 
ms.custom: 19H1
---

# DNS_NAPTR_DATAW structure


## -description


The 
<b>DNS_NAPTR_DATA</b> structure represents a Naming Authority Pointer (NAPTR) DNS Resource Record (RR) as specified in <a href="https://go.microsoft.com/fwlink/p/?linkid=107024">RFC 2915</a>.


## -struct-fields




### -field wOrder

 A value that determines the NAPTR RR processing order as defined in section 2 of <a href="https://go.microsoft.com/fwlink/p/?linkid=107024">RFC 2915</a>.


### -field wPreference

A value that determines the NAPTR RR processing  order  for records with the same <b>wOrder</b> value as defined in section 2 of <a href="https://go.microsoft.com/fwlink/p/?linkid=107024">RFC 2915</a>.


### -field pFlags

A pointer to a string  that represents a set of NAPTR RR flags which determine the interpretation and processing of NAPTR record fields as defined in section 2 of <a href="https://go.microsoft.com/fwlink/p/?linkid=107024">RFC 2915</a>.


### -field pService

A pointer to a string that represents the available services in this rewrite path as defined in section 2 of <a href="https://go.microsoft.com/fwlink/p/?linkid=107024">RFC 2915</a>.


### -field pRegularExpression

A pointer to a string that represents a substitution expression as defined in sections 2 and 3 of <a href="https://go.microsoft.com/fwlink/p/?linkid=107024">RFC 2915</a>.


### -field pReplacement

A pointer to a string that represents the next NAPTR query name as defined in section 2 of <a href="https://go.microsoft.com/fwlink/p/?linkid=107024">RFC 2915</a>.


## -see-also




<a href="https://docs.microsoft.com/windows/win32/api/windns/ns-windns-dns_recorda">DNS_RECORD</a>
 

 

