# TCP, UDP, SCTP & DCCP Port Reference — 0–65535

> **Updated:** September 12, 2026
>
> This reference combines Wikipedia's broad real-world port coverage with IANA assignments, RFCs, Nmap service data, and vendor/project documentation. It intentionally distinguishes official assignments from unofficial but important uses.

## Scope, classification & coverage

Ports are 16-bit numbers from `0` through `65535`.

| **Port Number Range** | **Designation** |
|---:|---|
| 0–1023 | System/Known (Well-Known) |
| 1024–49151 | User/Registered (Registered) |
| 49152–65535 | Dynamic/Private |

A row represents a **port/protocol/use combination**. TCP, UDP, SCTP, and DCCP are treated independently because a numeric port can have different registrations and uses under different transport protocols.

### Protocol status legend

| **Indicator** | **Protocol Status** | **Meaning** |
|---|---|---|
| 🟢 | **Assigned — Standard/Widely Used** | Assigned by IANA and standardized, specified, or widely used on the port. |
| 🔵 | **Unofficial — Standard/Widely Used** | Not assigned by IANA, but standardized, specified, or widely used on the port. |
| 🟡 | **Assigned — Limited/Unused** | Assigned by IANA, but not standardized, specified, or widely used on the port. |
| 🔴 | **Unassigned / No Known Use** | Not assigned by IANA and not known to have a standardized, specified, or significant use. |
| ⚪ | **Reserved** | Reserved by IANA, generally to prevent collisions after a previous assignment was withdrawn. |

**Status applies to the specific transport protocol in that row.** An unofficial application use does not become an IANA assignment merely because it is common.

### Unknown / unregistered numbers

This reference does not list thousands of numbers whose only useful fact would be that no covered source gives them a notable service. An omitted number is **not** a claim that IANA has individually marked every such number as unassigned. Private software can use many otherwise undocumented ports.

The full IANA registry should be consulted when the formal status of a particular port/protocol combination matters.

### Sources

- **Wikipedia:** [List of TCP and UDP port numbers](https://en.wikipedia.org/wiki/List_of_TCP_and_UDP_port_numbers) — broad real-world, historical, legacy, and unofficial usage.
- **IANA:** [Service Name and Transport Protocol Port Number Registry](https://www.iana.org/assignments/service-names-port-numbers/service-names-port-numbers.xhtml) — authoritative assignments and protocol status.
- **RFC 6335:** [Service Name and Transport Protocol Port Number Registry](https://www.rfc-editor.org/rfc/rfc6335) — ranges, terminology, and assignment policy.
- **RFC Editor:** [RFC repository](https://www.rfc-editor.org/) — protocol specifications and historical dates.
- **Nmap:** [`nmap-services`](https://nmap.org/book/nmap-services.html) — practical service names and observed usage.
- **Microsoft Learn:** [Service overview and network port requirements](https://learn.microsoft.com/en-us/troubleshoot/windows-server/networking/service-overview-and-network-port-requirements) — Windows-specific services and ports.
- Vendor/project documentation is used for application-specific ports where the sources above are insufficient.

## Port reference

| **Port Number(s)** | **Transport Protocol** | **Protocol Status** | **Designation** | **Description** | **Date Created** | **Note(s)** |
|---:|---|---|---|---|---|---|
| 1 | TCP | 🟢 Assigned — Standard/Widely Used | System/Known | TCPMUX, a TCP service multiplexer. | 1981 | Legacy protocol; rarely used. |
| 7 | TCP | 🟢 Assigned — Standard/Widely Used | System/Known | Echo Protocol. | 1983 | Legacy/testing service. |
| 7 | UDP | 🟢 Assigned — Standard/Widely Used | System/Known | Echo Protocol over UDP. | 1983 | Legacy/testing service. |
| 9 | TCP | 🟢 Assigned — Standard/Widely Used | System/Known | Discard Protocol. | 1983 | Legacy/testing service. |
| 9 | UDP | 🟢 Assigned — Standard/Widely Used | System/Known | Discard Protocol over UDP. | 1983 | Also widely encountered as Wake-on-LAN's destination port; separate from Discard. |
| 11 | TCP | 🟢 Assigned — Standard/Widely Used | System/Known | Active Users / SYSTAT. | 1983 | Legacy. |
| 13 | TCP | 🟢 Assigned — Standard/Widely Used | System/Known | Daytime Protocol. | 1983 | Legacy. |
| 13 | UDP | 🟢 Assigned — Standard/Widely Used | System/Known | Daytime Protocol over UDP. | 1983 | Legacy. |
| 17 | TCP | 🟢 Assigned — Standard/Widely Used | System/Known | Quote of the Day (QOTD). | 1983 | Legacy. |
| 19 | TCP | 🟢 Assigned — Standard/Widely Used | System/Known | Character Generator (CHARGEN). | 1983 | Legacy; can be abused for amplification. |
| 19 | UDP | 🟢 Assigned — Standard/Widely Used | System/Known | Character Generator over UDP. | 1983 | Legacy; amplification risk when exposed. |
| 20 | TCP | 🟢 Assigned — Standard/Widely Used | System/Known | FTP data transfer. | 1971 | FTP data channel. |
| 21 | TCP | 🟢 Assigned — Standard/Widely Used | System/Known | FTP control connection. | 1971 | FTP control channel. |
| 21 | UDP | 🟢 Assigned — Limited/Unused | System/Known | Historical File Service Protocol and related uses. | 1980s | Do not confuse this historical UDP use with standard FTP. |
| 22 | TCP | 🟢 Assigned — Standard/Widely Used | System/Known | Secure Shell (SSH). | 1995 | SFTP and SCP commonly operate through SSH on this port. |
| 23 | TCP | 🟢 Assigned — Standard/Widely Used | System/Known | Telnet. | 1969 | Legacy/insecure remote terminal protocol. |
| 25 | TCP | 🟢 Assigned — Standard/Widely Used | System/Known | Simple Mail Transfer Protocol (SMTP). | 1982 | Server-to-server mail transport. |
| 25 | UDP | 🟡 Assigned — Limited/Unused | System/Known | Historical SMTP-related registration. | 1982 | Modern SMTP overwhelmingly uses TCP. |
| 37 | TCP | 🟢 Assigned — Standard/Widely Used | System/Known | Time Protocol. | 1983 | Legacy. |
| 37 | UDP | 🟢 Assigned — Standard/Widely Used | System/Known | Time Protocol over UDP. | 1983 | Legacy. |
| 43 | TCP | 🟢 Assigned — Standard/Widely Used | System/Known | WHOIS service. | 1985 | Legacy registry lookup protocol; RDAP is the modern replacement for many uses. |
| 53 | TCP | 🟢 Assigned — Standard/Widely Used | System/Known | Domain Name System (DNS). | 1983 | Used for zone transfers and other reliable DNS operations. |
| 53 | UDP | 🟢 Assigned — Standard/Widely Used | System/Known | Domain Name System (DNS). | 1983 | Traditional DNS query transport. |
| 67 | UDP | 🟢 Assigned — Standard/Widely Used | System/Known | DHCP/BOOTP server. | 1985 | Server-side DHCP/BOOTP port. |
| 68 | UDP | 🟢 Assigned — Standard/Widely Used | System/Known | DHCP/BOOTP client. | 1985 | Client-side DHCP/BOOTP port. |
| 69 | UDP | 🟢 Assigned — Standard/Widely Used | System/Known | Trivial File Transfer Protocol (TFTP). | 1981 | Transfer sessions use additional ephemeral UDP ports. |
| 70 | TCP | 🟢 Assigned — Standard/Widely Used | System/Known | Gopher protocol. | 1991 | Legacy Internet information retrieval protocol. |
| 79 | TCP | 🟢 Assigned — Standard/Widely Used | System/Known | Finger user-information protocol. | 1977 | Legacy. |
| 80 | TCP | 🟢 Assigned — Standard/Widely Used | System/Known | Hypertext Transfer Protocol (HTTP). | 1991 | Standard HTTP port. |
| 88 | TCP | 🟢 Assigned — Standard/Widely Used | System/Known | Kerberos authentication. | 1988 | Kerberos V5. |
| 88 | UDP | 🟢 Assigned — Standard/Widely Used | System/Known | Kerberos authentication. | 1988 | Kerberos V5. |
| 102 | TCP | 🟢 Assigned — Standard/Widely Used | System/Known | ISO Transport Service on top of TCP. | 1987 | RFC 1006; used by OSI-derived applications. |
| 104 | TCP | 🟢 Assigned — Standard/Widely Used | System/Known | DICOM network communications. | 1980s | Common default for DICOM. |
| 110 | TCP | 🟢 Assigned — Standard/Widely Used | System/Known | Post Office Protocol version 3 (POP3). | 1988 | POP3S normally uses 995/TCP. |
| 111 | TCP | 🟢 Assigned — Standard/Widely Used | System/Known | ONC RPC portmapper / rpcbind. | 1988 | Maps RPC programs to dynamic ports. |
| 111 | UDP | 🟢 Assigned — Standard/Widely Used | System/Known | ONC RPC portmapper / rpcbind. | 1988 | Legacy and current RPC environments. |
| 113 | TCP | 🟢 Assigned — Standard/Widely Used | System/Known | Identification Protocol (ident). | 1985 | Legacy. |
| 119 | TCP | 🟢 Assigned — Standard/Widely Used | System/Known | Network News Transfer Protocol (NNTP). | 1986 | Usenet/news transport. |
| 123 | UDP | 🟢 Assigned — Standard/Widely Used | System/Known | Network Time Protocol (NTP). | 1985 | Standard NTP transport. |
| 123 | TCP | 🟡 Assigned — Limited/Unused | System/Known | NTP over TCP / fallback or application-specific use. | 1985 | UDP is the normal NTP transport. |
| 135 | TCP | 🟢 Assigned — Standard/Widely Used | System/Known | Microsoft RPC Endpoint Mapper. | 1993 | Windows RPC infrastructure. |
| 137 | UDP | 🟢 Assigned — Standard/Widely Used | System/Known | NetBIOS Name Service. | 1983 | Legacy Windows networking. |
| 138 | UDP | 🟢 Assigned — Standard/Widely Used | System/Known | NetBIOS Datagram Service. | 1983 | Legacy Windows networking. |
| 139 | TCP | 🟢 Assigned — Standard/Widely Used | System/Known | NetBIOS Session Service. | 1983 | Legacy Windows networking; SMB commonly uses 445/TCP directly today. |
| 143 | TCP | 🟢 Assigned — Standard/Widely Used | System/Known | Internet Message Access Protocol (IMAP). | 1986 | Standard IMAP. |
| 161 | UDP | 🟢 Assigned — Standard/Widely Used | System/Known | Simple Network Management Protocol (SNMP). | 1988 | SNMP management traffic. |
| 162 | UDP | 🟢 Assigned — Standard/Widely Used | System/Known | SNMP Trap / Inform receiver. | 1988 | Standard trap transport. |
| 179 | TCP | 🟢 Assigned — Standard/Widely Used | System/Known | Border Gateway Protocol (BGP). | 1989 | Standard BGP transport. |
| 389 | TCP | 🟢 Assigned — Standard/Widely Used | System/Known | Lightweight Directory Access Protocol (LDAP). | 1993 | Standard LDAP. |
| 443 | TCP | 🟢 Assigned — Standard/Widely Used | System/Known | HTTPS, normally HTTP over TLS. | 1994 | Widely used secure web port. |
| 443 | UDP | 🟢 Assigned — Standard/Widely Used | System/Known | QUIC, including HTTP/3. | 2012 | Modern HTTP/3 default transport. |
| 445 | TCP | 🟢 Assigned — Standard/Widely Used | System/Known | Microsoft-DS / SMB directly over TCP. | 1990s | Primary modern SMB transport on Windows networks. |
| 465 | TCP | 🟢 Assigned — Standard/Widely Used | System/Known | SMTP submission over implicit TLS. | 1997 | Reassigned for message submission over TLS. |
| 500 | UDP | 🟢 Assigned — Standard/Widely Used | System/Known | Internet Key Exchange (IKE / ISAKMP). | 1998 | IPsec key-management traffic. |
| 514 | UDP | 🟢 Assigned — Standard/Widely Used | System/Known | Syslog. | 1980s | Traditional syslog transport. |
| 515 | TCP | 🟢 Assigned — Standard/Widely Used | System/Known | Line Printer Daemon / Line Printer Remote. | 1988 | Legacy network printing protocol. |
| 520 | UDP | 🟢 Assigned — Standard/Widely Used | System/Known | Routing Information Protocol (RIP). | 1988 | Legacy interior routing protocol. |
| 546 | UDP | 🟢 Assigned — Standard/Widely Used | System/Known | DHCPv6 client. | 1998 | DHCPv6. |
| 547 | UDP | 🟢 Assigned — Standard/Widely Used | System/Known | DHCPv6 server/relay. | 1998 | DHCPv6. |
| 548 | TCP | 🟡 Assigned — Limited/Unused | System/Known | Apple Filing Protocol (AFP). | 1988 | Legacy on modern Apple systems. |
| 554 | TCP | 🟢 Assigned — Standard/Widely Used | System/Known | Real Time Streaming Protocol (RTSP). | 1998 | Media control protocol. |
| 554 | UDP | 🟢 Assigned — Standard/Widely Used | System/Known | RTSP / RTP-related application use. | 1998 | Implementations vary in media transport. |
| 563 | TCP | 🟢 Assigned — Standard/Widely Used | System/Known | NNTP over TLS. | 1997 | Secure NNTP. |
| 587 | TCP | 🟢 Assigned — Standard/Widely Used | System/Known | SMTP message submission. | 1998 | Preferred authenticated mail-submission port. |
| 631 | TCP | 🟢 Assigned — Standard/Widely Used | System/Known | Internet Printing Protocol (IPP). | 1999 | Widely used network-printing protocol. |
| 636 | TCP | 🟢 Assigned — Standard/Widely Used | System/Known | LDAP over TLS (LDAPS). | 1997 | Direct TLS LDAP connection. |
| 646 | TCP | 🟢 Assigned — Standard/Widely Used | System/Known | Label Distribution Protocol (LDP). | 2001 | MPLS signaling. |
| 646 | UDP | 🟢 Assigned — Standard/Widely Used | System/Known | LDP discovery. | 2001 | TCP carries the primary LDP session. |
| 853 | TCP | 🟢 Assigned — Standard/Widely Used | System/Known | DNS over TLS (DoT). | 2016 | Encrypted DNS. |
| 853 | UDP | 🟢 Assigned — Standard/Widely Used | System/Known | DNS over QUIC. | 2022 | RFC-defined DNS over QUIC uses UDP/853. |
| 873 | TCP | 🟢 Assigned — Standard/Widely Used | System/Known | rsync file synchronization. | 1996 | Standard rsync daemon port. |
| 902 | TCP | 🔵 Unofficial — Standard/Widely Used | System/Known | VMware server / management traffic. | 1998 | Product-specific usage. |
| 903 | TCP | 🔵 Unofficial — Standard/Widely Used | System/Known | VMware remote console. | 1998 | Legacy VMware remote console transport. |
| 989 | TCP | 🟢 Assigned — Standard/Widely Used | System/Known | FTPS data. | 1997 | FTP over TLS/SSL data channel. |
| 990 | TCP | 🟢 Assigned — Standard/Widely Used | System/Known | FTPS control. | 1997 | FTP over TLS/SSL control channel. |
| 992 | TCP | 🟢 Assigned — Standard/Widely Used | System/Known | Telnet over TLS/SSL. | 1996 | Legacy secure Telnet. |
| 993 | TCP | 🟢 Assigned — Standard/Widely Used | System/Known | IMAP over TLS. | 1996 | Secure IMAP. |
| 995 | TCP | 🟢 Assigned — Standard/Widely Used | System/Known | POP3 over TLS. | 1996 | Secure POP3. |
| 1025 | TCP | 🔵 Unofficial — Standard/Widely Used | User/Registered | Historical Microsoft RPC/dynamic-service use. | 1980s | Modern Windows dynamic RPC ranges are configurable. |
| 1080 | TCP | 🟢 Assigned — Standard/Widely Used | User/Registered | SOCKS proxy. | 1992 | Common SOCKS proxy port. |
| 1080 | UDP | 🟢 Assigned — Standard/Widely Used | User/Registered | SOCKS-related UDP relay traffic. | 1992 | SOCKS UDP ASSOCIATE. |
| 1099 | TCP | 🟢 Assigned — Standard/Widely Used | User/Registered | Java RMI Registry. | 1997 | Standard RMI registry port. |
| 1194 | TCP | 🟢 Assigned — Standard/Widely Used | User/Registered | OpenVPN. | 2002 | Common OpenVPN default. |
| 1194 | UDP | 🟢 Assigned — Standard/Widely Used | User/Registered | OpenVPN. | 2002 | Common default and generally preferred transport. |
| 1352 | TCP | 🟢 Assigned — Standard/Widely Used | User/Registered | IBM Notes / Lotus Domino. | 1993 | Common Domino server port. |
| 1433 | TCP | 🟢 Assigned — Standard/Widely Used | User/Registered | Microsoft SQL Server. | 1993 | Default SQL Server instance port. |
| 1434 | UDP | 🟢 Assigned — Standard/Widely Used | User/Registered | SQL Server Browser. | 1998 | Helps clients locate named instances. |
| 1521 | TCP | 🟢 Assigned — Standard/Widely Used | User/Registered | Oracle Net Listener. | 1980s | Common Oracle Database listener port. |
| 1701 | UDP | 🟢 Assigned — Standard/Widely Used | User/Registered | Layer 2 Tunneling Protocol (L2TP). | 1999 | Commonly paired with IPsec. |
| 1723 | TCP | 🟢 Assigned — Standard/Widely Used | User/Registered | Point-to-Point Tunneling Protocol (PPTP). | 1996 | Legacy/insecure VPN protocol. |
| 1812 | UDP | 🟢 Assigned — Standard/Widely Used | User/Registered | RADIUS authentication. | 1997 | Standard RADIUS authentication port. |
| 1813 | UDP | 🟢 Assigned — Standard/Widely Used | User/Registered | RADIUS accounting. | 1997 | Standard accounting port. |
| 1883 | TCP | 🟢 Assigned — Standard/Widely Used | User/Registered | MQTT. | 1999 | Standard non-TLS MQTT port. |
| 1900 | UDP | 🟢 Assigned — Standard/Widely Used | User/Registered | SSDP / UPnP discovery. | 1999 | Local-network discovery; generally not for Internet exposure. |
| 2049 | TCP | 🟢 Assigned — Standard/Widely Used | User/Registered | Network File System (NFS). | 1984 | NFS versions vary in transport behavior. |
| 2049 | UDP | 🟡 Assigned — Limited/Unused | User/Registered | NFS over UDP. | 1984 | Mostly legacy. |
| 2181 | TCP | 🔵 Unofficial — Standard/Widely Used | User/Registered | Apache ZooKeeper client/server connection. | 2010 | Default ZooKeeper client port. |
| 2375 | TCP | 🔵 Unofficial — Standard/Widely Used | User/Registered | Docker daemon API without TLS. | 2013 | Dangerous if exposed to untrusted networks. |
| 2376 | TCP | 🔵 Unofficial — Standard/Widely Used | User/Registered | Docker daemon API with TLS. | 2013 | Secure Docker daemon TCP port. |
| 3000 | TCP | 🔵 Unofficial — Standard/Widely Used | User/Registered | Common HTTP/development/application port. | 1990s | No single universal service. |
| 3128 | TCP | 🔵 Unofficial — Standard/Widely Used | User/Registered | Squid HTTP proxy. | 1996 | Common Squid proxy port. |
| 3260 | TCP | 🟢 Assigned — Standard/Widely Used | User/Registered | iSCSI target. | 2000 | Standard iSCSI transport. |
| 3268 | TCP | 🟢 Assigned — Standard/Widely Used | User/Registered | Microsoft Global Catalog. | 1999 | Active Directory Global Catalog. |
| 3269 | TCP | 🟢 Assigned — Standard/Widely Used | User/Registered | Microsoft Global Catalog over TLS. | 1999 | Secure Global Catalog. |
| 3306 | TCP | 🟢 Assigned — Standard/Widely Used | User/Registered | MySQL/MariaDB database server. | 1995 | Common default database port. |
| 3389 | TCP | 🟢 Assigned — Standard/Widely Used | User/Registered | Microsoft Remote Desktop Protocol (RDP). | 1998 | Standard RDP TCP transport. |
| 3389 | UDP | 🟢 Assigned — Standard/Widely Used | User/Registered | Microsoft RDP UDP transport. | 2012 | Modern RDP can use UDP alongside TCP. |
| 3478 | TCP | 🟢 Assigned — Standard/Widely Used | User/Registered | STUN/TURN server traffic. | 2003 | NAT traversal and media relay. |
| 3478 | UDP | 🟢 Assigned — Standard/Widely Used | User/Registered | STUN/TURN server traffic. | 2003 | Common UDP NAT-traversal transport. |
| 3690 | TCP | 🟢 Assigned — Standard/Widely Used | User/Registered | Subversion (SVN) protocol. | 2000 | Standard SVN server port. |
| 4369 | TCP | 🟢 Assigned — Standard/Widely Used | User/Registered | Erlang Port Mapper Daemon (EPMD). | 1998 | Maps Erlang distributed-node ports. |
| 4444 | TCP | 🔵 Unofficial — Standard/Widely Used | User/Registered | Common application/development port. | 1990s | Widely reused; not synonymous with one service. |
| 4444 | UDP | 🔵 Unofficial — Standard/Widely Used | User/Registered | Common application-specific port. | 1990s | Widely reused. |
| 4500 | UDP | 🟢 Assigned — Standard/Widely Used | User/Registered | IPsec NAT Traversal (NAT-T). | 2005 | Used with IKE/IPsec. |
| 5060 | TCP | 🟢 Assigned — Standard/Widely Used | User/Registered | Session Initiation Protocol (SIP). | 2002 | SIP signaling. |
| 5060 | UDP | 🟢 Assigned — Standard/Widely Used | User/Registered | Session Initiation Protocol (SIP). | 2002 | Common SIP transport. |
| 5061 | TCP | 🟢 Assigned — Standard/Widely Used | User/Registered | SIP over TLS. | 2002 | Secure SIP signaling. |
| 5222 | TCP | 🟢 Assigned — Standard/Widely Used | User/Registered | XMPP client-to-server. | 1999 | Standard XMPP client port. |
| 5269 | TCP | 🟢 Assigned — Standard/Widely Used | User/Registered | XMPP server-to-server. | 1999 | Standard XMPP inter-server port. |
| 5353 | UDP | 🟢 Assigned — Standard/Widely Used | User/Registered | Multicast DNS (mDNS). | 2003 | Local-link discovery. |
| 5432 | TCP | 🟢 Assigned — Standard/Widely Used | User/Registered | PostgreSQL. | 1996 | Default PostgreSQL server port. |
| 5555 | TCP | 🔵 Unofficial — Standard/Widely Used | User/Registered | Common application/debugging port, including ADB over TCP. | 2008 | Not synonymous with ADB; many applications use it. |
| 5555 | UDP | 🔵 Unofficial — Standard/Widely Used | User/Registered | Common application-specific port. | 1990s | Not synonymous with ADB. |
| 5671 | TCP | 🟢 Assigned — Standard/Widely Used | User/Registered | AMQP over TLS. | 2008 | Common RabbitMQ TLS port. |
| 5672 | TCP | 🟢 Assigned — Standard/Widely Used | User/Registered | Advanced Message Queuing Protocol (AMQP). | 2003 | Common RabbitMQ non-TLS port. |
| 5683 | UDP | 🟢 Assigned — Standard/Widely Used | User/Registered | Constrained Application Protocol (CoAP). | 2014 | Standard unsecured CoAP. |
| 5684 | UDP | 🟢 Assigned — Standard/Widely Used | User/Registered | CoAP over DTLS. | 2014 | Secure CoAP. |
| 5900 | TCP | 🟢 Assigned — Standard/Widely Used | User/Registered | VNC / RFB, display :0. | 1998 | Display number normally maps to 5900 + display. |
| 5985 | TCP | 🟢 Assigned — Standard/Widely Used | User/Registered | Windows Remote Management over HTTP. | 2003 | Microsoft management protocol. |
| 5986 | TCP | 🟢 Assigned — Standard/Widely Used | User/Registered | Windows Remote Management over HTTPS. | 2003 | Secure WinRM. |
| 6000 | TCP | 🟢 Assigned — Standard/Widely Used | User/Registered | X Window System display :0. | 1984 | Many modern systems disable network X11. |
| 6379 | TCP | 🟢 Assigned — Standard/Widely Used | User/Registered | Redis. | 2009 | Default Redis server port. |
| 6443 | TCP | 🔵 Unofficial — Standard/Widely Used | User/Registered | Kubernetes API server. | 2014 | Common Kubernetes API endpoint. |
| 6514 | TCP | 🟢 Assigned — Standard/Widely Used | User/Registered | Syslog over TLS. | 2008 | Secure syslog transport. |
| 6667 | TCP | 🟢 Assigned — Standard/Widely Used | User/Registered | Internet Relay Chat (IRC). | 1988 | Common IRC server port. |
| 6881–6889 | TCP | 🔵 Unofficial — Standard/Widely Used | User/Registered | Common BitTorrent peer-to-peer range. | 2001 | Historical/default range; clients can use arbitrary ports. |
| 6881–6889 | UDP | 🔵 Unofficial — Standard/Widely Used | User/Registered | BitTorrent peer-to-peer/DHT-related traffic. | 2001 | Modern clients can use arbitrary ports. |
| 8000 | TCP | 🔵 Unofficial — Standard/Widely Used | User/Registered | Common HTTP alternate/development server port. | 1990s | No single universal service. |
| 8080 | TCP | 🔵 Unofficial — Standard/Widely Used | User/Registered | Common HTTP alternate, proxy, and web-application port. | 1990s | Extremely common application-specific use. |
| 8080 | UDP | 🔵 Unofficial — Standard/Widely Used | User/Registered | Application-specific alternate HTTP/UDP use. | 1990s | Not equivalent to HTTP/TCP in every application. |
| 8443 | TCP | 🔵 Unofficial — Standard/Widely Used | User/Registered | Common HTTPS alternate/application port. | 1990s | Widely used by web applications and administration interfaces. |
| 8888 | TCP | 🔵 Unofficial — Standard/Widely Used | User/Registered | Common HTTP alternate; widely used by development software such as Jupyter. | 1990s | Application-specific. |
| 9000 | TCP | 🔵 Unofficial — Standard/Widely Used | User/Registered | Common application/web-service port. | 1990s | Meaning varies substantially by application. |
| 9090 | TCP | 🔵 Unofficial — Standard/Widely Used | User/Registered | Common HTTP/application port; used by Prometheus. | 2012 | Prometheus default web UI/API port. |
| 9100 | TCP | 🟢 Assigned — Standard/Widely Used | User/Registered | JetDirect / raw network printing. | 1990s | Common raw-printing port. |
| 9200 | TCP | 🔵 Unofficial — Standard/Widely Used | User/Registered | Elasticsearch HTTP/REST API. | 2010 | Default Elasticsearch HTTP port. |
| 9300 | TCP | 🔵 Unofficial — Standard/Widely Used | User/Registered | Elasticsearch node-to-node transport. | 2010 | Elasticsearch internal transport. |
| 9418 | TCP | 🟢 Assigned — Standard/Widely Used | User/Registered | Git native protocol. | 2005 | Unencrypted Git transport. |
| 10000 | TCP | 🔵 Unofficial — Standard/Widely Used | User/Registered | Webmin administration interface. | 1999 | Common Webmin default port. |
| 10050 | TCP | 🟢 Assigned — Standard/Widely Used | User/Registered | Zabbix agent. | 2001 | Default Zabbix agent port. |
| 10051 | TCP | 🟢 Assigned — Standard/Widely Used | User/Registered | Zabbix server/trapper. | 2001 | Default Zabbix server port. |
| 11211 | TCP | 🟢 Assigned — Standard/Widely Used | User/Registered | Memcached. | 2003 | Common Memcached TCP port. |
| 11211 | UDP | 🟢 Assigned — Standard/Widely Used | User/Registered | Memcached over UDP. | 2003 | UDP is optional; exposed UDP memcached has amplification risk. |
| 15672 | TCP | 🔵 Unofficial — Standard/Widely Used | User/Registered | RabbitMQ Management HTTP API/UI. | 2007 | Management interface, not the AMQP data port. |
| 19132 | UDP | 🟢 Assigned — Standard/Widely Used | User/Registered | Minecraft Bedrock Edition server. | 2011 | Common/default Bedrock IPv4 server port. |
| 25565 | TCP | 🟢 Assigned — Standard/Widely Used | User/Registered | Minecraft Java Edition server. | 2009 | Common/default Java Edition server port. |
| 25575 | TCP | 🔵 Unofficial — Standard/Widely Used | User/Registered | Minecraft RCON. | 2009 | Configurable remote-console port. |
| 27015 | TCP | 🔵 Unofficial — Standard/Widely Used | User/Registered | Steam/Source-engine game traffic. | 2003 | Common Source-engine default; game-specific behavior varies. |
| 27015 | UDP | 🔵 Unofficial — Standard/Widely Used | User/Registered | Steam/Source-engine game traffic. | 2003 | Common Source-engine default; game-specific behavior varies. |
| 27017 | TCP | 🟢 Assigned — Standard/Widely Used | User/Registered | MongoDB database service. | 2009 | Default MongoDB port. |
| 32400 | TCP | 🔵 Unofficial — Standard/Widely Used | User/Registered | Plex Media Server. | 2008 | Common/default Plex server port. |
| 51820 | UDP | 🔵 Unofficial — Standard/Widely Used | Dynamic/Private | WireGuard VPN. | 2015 | Common default; WireGuard can use any UDP port. |

## Reading the table

- A port number can appear multiple times because different applications can use it and because transport protocols are independent.
- **Protocol Status** describes the specific transport protocol in that row.
- **Designation** follows the traditional numeric ranges and does not indicate popularity or current deployment.
- **Date Created** is the earliest reliable date associated with the protocol/service where reasonably established; it is not necessarily the IANA registration date.
- `—` should be used when a reliable creation date cannot be established without guessing.
- **Note(s)** records legacy status, obsolete protocols, unofficial uses, security concerns, configurable ports, and other distinctions.

## Assigned vs. commonly used

A port being commonly used by an application does **not** necessarily mean that application is the service officially associated with the port. Conversely, an IANA assignment does not guarantee that a service is still popular or actively deployed. This reference keeps those concepts separate rather than collapsing them into a single service-name field.
