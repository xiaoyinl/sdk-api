---
UID: NS:udpmib._MIB_UDPROW_OWNER_PID
title: MIB_UDPROW_OWNER_PID (udpmib.h)
description: Contains an entry from the User Datagram Protocol (UDP) listener table for IPv4 on the local computer. The entry also includes the process ID (PID) that issued the call to the bind function for the UDP endpoint.
old-location: mib\mib_udprow_owner_pid.htm
tech.root: MIB
ms.assetid: b914b6eb-adf9-4a61-ae8f-05d3ff90ce90
ms.date: 12/05/2018
ms.keywords: '*PMIB_UDPROW_OWNER_PID, MIB_UDPROW_OWNER_PID, MIB_UDPROW_OWNER_PID structure [MIB], PMIB_UDPROW_OWNER_PID, PMIB_UDPROW_OWNER_PID structure pointer [MIB], iprtrmib/MIB_UDPROW_OWNER_PID, iprtrmib/PMIB_UDPROW_OWNER_PID, mib.mib_udprow_owner_pid, udpmib/MIB_UDPROW_OWNER_PID, udpmib/PMIB_UDPROW_OWNER_PID'
f1_keywords:
- udpmib/MIB_UDPROW_OWNER_PID
dev_langs:
- c++
req.header: udpmib.h
req.include-header: Iphlpapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2008, Windows Server 2003 with SP1 [desktop apps only]
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
- Udpmib.h
- Iprtrmib.h
api_name:
- MIB_UDPROW_OWNER_PID
targetos: Windows
req.typenames: MIB_UDPROW_OWNER_PID, *PMIB_UDPROW_OWNER_PID
req.redist: 
ms.custom: 19H1
---

# MIB_UDPROW_OWNER_PID structure


## -description


The <b>MIB_UDPROW_OWNER_PID</b> structure contains an entry from the User Datagram Protocol (UDP)  listener table for IPv4 on the local computer. The entry also includes the process ID (PID) that issued the call to the <a href="https://docs.microsoft.com/windows/desktop/api/winsock/nf-winsock-bind">bind</a> function for the UDP endpoint.


## -struct-fields




### -field dwLocalAddr

The IPv4 address of the UDP endpoint on the local computer. 

A value of zero indicates a UDP listener  willing to accept datagrams for any IP interface associated
                      with the local computer.


### -field dwLocalPort

The port number of the UDP endpoint on the local computer. This member is stored in network byte order.


### -field dwOwningPid

The PID of the process that issued the call to the <a href="https://docs.microsoft.com/windows/desktop/api/winsock/nf-winsock-bind">bind</a> function for the UDP endpoint. This member is set to 0 when the PID is unavailable.


## -remarks



The <a href="https://docs.microsoft.com/windows/desktop/api/udpmib/ns-udpmib-mib_udptable_owner_pid">MIB_UDPTABLE_OWNER_PID</a> structure is returned by a call to <a href="https://docs.microsoft.com/windows/desktop/api/iphlpapi/nf-iphlpapi-getextendedudptable">GetExtendedUdpTable</a> with the <i>TableClass</i> parameter set to <b>UDP_TABLE_OWNER_PID</b> and the <i>ulAf</i> parameter set to <b>AF_INET</b>. The <b>MIB_UDPTABLE_OWNER_PID</b> structure contains an array of <b>MIB_UDPROW_OWNER_PID</b> structures.

The <b>dwLocalAddr</b> member is stored as a <b>DWORD</b> in the same format as the  <a href="https://docs.microsoft.com/windows/desktop/api/winsock2/ns-winsock2-in_addr">in_addr</a> structure. In order to use the <b>dwLocalAddr</b> member, the <a href="https://docs.microsoft.com/windows/desktop/api/winsock/nf-winsock-ntohl">ntohl</a> or <a href="https://docs.microsoft.com/windows/desktop/api/wsipv6ok/nf-wsipv6ok-inet_ntoa">inet_ntoa</a> functions in Windows Sockets or similar functions may be needed. On Windows Vistaand later, the <a href="https://docs.microsoft.com/windows/desktop/api/ip2string/nf-ip2string-rtlipv4addresstostringa">RtlIpv4AddressToString</a> or <a href="https://docs.microsoft.com/windows/desktop/api/ip2string/nf-ip2string-rtlipv4addresstostringexw">RtlIpv4AddressToStringEx</a> functions may be used to convert the IPv4 address in the <b>dwLocalAddr</b>  member to a string without loading the Windows Sockets DLL. 

The <b>dwLocalPort</b> member is in network byte order. In order to use the <b>dwLocalPort</b> member, the <a href="https://docs.microsoft.com/windows/desktop/api/winsock/nf-winsock-ntohs">ntohs</a> or <a href="https://docs.microsoft.com/windows/desktop/api/wsipv6ok/nf-wsipv6ok-inet_ntoa">inet_ntoa</a> functions in Windows Sockets or similar functions may be needed. 

The <a href="https://docs.microsoft.com/windows/desktop/api/udpmib/ns-udpmib-mib_udptable_owner_pid">MIB_UDPTABLE_OWNER_PID</a> structure contains the UDP listener table for IPv4 on the local computer. The name is based on the definition of this table in RFC 1213 published by the IETF. For more information, see 
<a href="https://go.microsoft.com/fwlink/p/?linkid=85984">http://www.ietf.org/rfc/rfc1213.txt</a>. This table contains UDP  endpoints for IPv4 that have been bound to an address. It should be noted that an application can create a UDP socket and bind it to an address for the sole purpose of sending a UDP datagram, with no intention of receiving packets using this socket (functioning as a listener). 

On the Microsoft Windows Software Development Kit (SDK) released for Windows Vistaand later, the organization of header files has changed. This  structure is defined in the <i>Udpmib.h</i> header file, not in the <i>Iprtrmib.h</i> header file. Note that the <i>Udpmib.h</i> header file is automatically included in <i>Iprtrmib.h</i>, which is automatically included in the <i>Iphlpapi.h</i> header file. The  <i>Udpmib.h</i> and <i>Iprtrmib.h</i> header files should never be used directly.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/iphlpapi/nf-iphlpapi-getextendedudptable">GetExtendedUdpTable</a>



<a href="https://docs.microsoft.com/windows/desktop/api/iphlpapi/nf-iphlpapi-getudp6table">GetUdp6Table</a>



<a href="https://docs.microsoft.com/windows/desktop/api/iphlpapi/nf-iphlpapi-getudptable">GetUdpTable</a>



<a href="https://docs.microsoft.com/windows/desktop/api/udpmib/ns-udpmib-mib_udp6row_owner_pid">MIB_UDP6ROW_OWNER_PID</a>



<a href="https://docs.microsoft.com/windows/desktop/api/udpmib/ns-udpmib-mib_udp6table_owner_pid">MIB_UDP6TABLE_OWNER_PID</a>



<a href="https://docs.microsoft.com/windows/desktop/api/udpmib/ns-udpmib-mib_udptable_owner_pid">MIB_UDPTABLE_OWNER_PID</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ip2string/nf-ip2string-rtlipv4addresstostringa">RtlIpv4AddressToString</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ip2string/nf-ip2string-rtlipv4addresstostringexw">RtlIpv4AddressToStringEx</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winsock/nf-winsock-bind">bind</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winsock2/ns-winsock2-in_addr">in_addr</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wsipv6ok/nf-wsipv6ok-inet_ntoa">inet_ntoa</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winsock/nf-winsock-ntohl">ntohl</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winsock/nf-winsock-ntohs">ntohs</a>
 

 

