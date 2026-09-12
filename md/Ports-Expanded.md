# TCP, UDP, SCTP & DCCP Port Reference — 0–65535

> **Updated:** September 11, 2026
>
> This reference combines the broad, practical coverage of Wikipedia's [List of TCP and UDP port numbers](https://en.wikipedia.org/wiki/List_of_TCP_and_UDP_port_numbers) with authoritative IANA assignments, RFCs, Nmap service data, and vendor/project documentation. It is intended to describe both officially assigned ports and important real-world, legacy, historical, or unofficial uses.

## Scope, classification & coverage

Ports are 16-bit numbers from `0` through `65535`. The traditional IANA designation ranges are:

| **Port Number Range** | **Designation** |
|---:|---|
| 0–1023 | System/Known (Well-Known) |
| 1024–49151 | User/Registered (Registered) |
| 49152–65535 | Dynamic/Private |

**Protocol Status** is recorded separately for each transport protocol because the same numeric port can have different registrations or statuses under TCP, UDP, SCTP, and DCCP. A row therefore represents a **port/protocol/use combination**, not merely a number.

**Assigned** means the protocol/port combination is assigned or registered by an authoritative registry. **Unassigned** means that combination has no current assignment identified by the authoritative source used for the row. **Reserved** means the number or combination is intentionally held back or otherwise not available for ordinary assignment. Historical or unofficial uses are not automatically treated as IANA assignments.

### Unknown / unregistered numbers

This file does **not** include thousands of rows whose only useful fact would be that no covered source gives them a significant service. Omitting a number from the table does **not** mean that IANA has individually declared every such number unassigned, and it does not prevent software from using the number privately.

The practical rule used here is:

> **An omitted port is simply outside the aggregated set of notable, documented, historical, or registry-significant entries represented by this reference.**

This replaces the previous long lists of thousands of "unknown" numbers. The full IANA registry remains the authoritative place to check the status of a specific port/protocol combination.

### Sources and source roles

- [Wikipedia — List of TCP and UDP port numbers](https://en.wikipedia.org/wiki/List_of_TCP_and_UDP_port_numbers): broad list, common real-world uses, legacy and unofficial uses, historical context.
- [IANA — Service Name and Transport Protocol Port Number Registry](https://www.iana.org/assignments/service-names-port-numbers/service-names-port-numbers.xhtml): authoritative assignment, transport, registration and status data.
- [RFC 6335](https://www.rfc-editor.org/rfc/rfc6335): port-number ranges, assignment policy and terminology.
- [RFC Editor](https://www.rfc-editor.org/): protocol specifications and historical standardization dates.
- [Nmap `nmap-services`](https://nmap.org/book/nmap-services.html): practical service names and commonly observed port usage.
- [Microsoft — Service overview and network port requirements](https://learn.microsoft.com/en-us/troubleshoot/windows-server/networking/service-overview-and-network-port-requirements): Windows-specific ports and services.
- Vendor/project documentation is used where an application-specific port is not adequately described by the sources above.

## Port reference

| **Port Number(s)** | **Transport Protocol** | **Protocol Status** | **Designation** | **Description** | **Date Created** | **Note(s)** |
|---:|---|---|---|---|---|---|
| 1 | TCP | Assigned [TCP] | System/Known | TCPMUX, a TCP service multiplexer. | 1981 | Legacy protocol; rarely used. |
| 7 | TCP | Assigned [TCP] | System/Known | Echo Protocol. | 1983 | Legacy/testing service. |
| 7 | UDP | Assigned [UDP] | System/Known | Echo Protocol over UDP. | 1983 | Legacy/testing service. |
| 9 | TCP | Assigned [TCP] | System/Known | Discard Protocol. | 1983 | Legacy/testing service. |
| 9 | UDP | Assigned [UDP] | System/Known | Discard Protocol over UDP. | 1983 | Also widely encountered as Wake-on-LAN's destination port; that use is separate from the Discard protocol assignment. |
| 11 | TCP | Assigned [TCP] | System/Known | Active Users / SYSTAT. | 1983 | Legacy. |
| 13 | TCP | Assigned [TCP] | System/Known | Daytime Protocol. | 1983 | Legacy. |
| 13 | UDP | Assigned [UDP] | System/Known | Daytime Protocol over UDP. | 1983 | Legacy. |
| 17 | TCP | Assigned [TCP] | System/Known | Quote of the Day (QOTD). | 1983 | Legacy. |
| 19 | TCP | Assigned [TCP] | System/Known | Character Generator (CHARGEN). | 1983 | Legacy; can be abused for amplification attacks. |
| 19 | UDP | Assigned [UDP] | System/Known | Character Generator over UDP. | 1983 | Legacy; amplification risk when exposed. |
| 20 | TCP | Assigned [TCP] | System/Known | FTP data transfer. | 1971 | FTP data channel. |
| 21 | TCP | Assigned [TCP] | System/Known | FTP control connection. | 1971 | FTP control channel. |
| 21 | UDP | Assigned [UDP] | System/Known | File Service Protocol (FSP) and related historical uses. | 1980s | Do not confuse historical UDP uses with standard FTP. |
| 22 | TCP | Assigned [TCP] | System/Known | Secure Shell (SSH). | 1995 | Standard SSH transport port; SFTP and SCP commonly run through SSH on the same port. |
| 23 | TCP | Assigned [TCP] | System/Known | Telnet. | 1969 | Legacy/insecure remote terminal protocol. |
| 25 | TCP | Assigned [TCP] | System/Known | Simple Mail Transfer Protocol (SMTP). | 1982 | Server-to-server mail transport. |
| 25 | UDP | Assigned [UDP] | System/Known | Historical SMTP-related registration. | 1982 | Modern SMTP deployments overwhelmingly use TCP. |
| 37 | TCP | Assigned [TCP] | System/Known | Time Protocol. | 1983 | Legacy. |
| 37 | UDP | Assigned [UDP] | System/Known | Time Protocol over UDP. | 1983 | Legacy. |
| 43 | TCP | Assigned [TCP] | System/Known | WHOIS service. | 1985 | Legacy registry lookup protocol; RDAP is the modern replacement for many uses. |
| 49 | TCP | Assigned [TCP] | System/Known | TACACS / TACACS-related authentication service. | 1980s | TACACS+ uses a different standard port. |
| 49 | UDP | Assigned [UDP] | System/Known | Historical TACACS transport. | 1980s | Legacy. |
| 53 | TCP | Assigned [TCP] | System/Known | Domain Name System (DNS). | 1983 | Used for reliable DNS operations including zone transfers and responses requiring TCP. |
| 53 | UDP | Assigned [UDP] | System/Known | Domain Name System (DNS). | 1983 | Traditional DNS query transport. |
| 67 | UDP | Assigned [UDP] | System/Known | DHCP/BOOTP server. | 1985 | Server-side DHCP/BOOTP port. |
| 68 | UDP | Assigned [UDP] | System/Known | DHCP/BOOTP client. | 1985 | Client-side DHCP/BOOTP port. |
| 69 | UDP | Assigned [UDP] | System/Known | Trivial File Transfer Protocol (TFTP). | 1981 | Uses ephemeral UDP transfer ports after initial contact. |
| 70 | TCP | Assigned [TCP] | System/Known | Gopher protocol. | 1991 | Legacy Internet information retrieval protocol. |
| 79 | TCP | Assigned [TCP] | System/Known | Finger user-information protocol. | 1977 | Legacy. |
| 80 | TCP | Assigned [TCP] | System/Known | Hypertext Transfer Protocol (HTTP). | 1991 | Standard HTTP port. |
| 80 | UDP | Assigned [UDP] | System/Known | UDP-based HTTP/3-related deployment and other application-specific HTTP uses. | 2012 | Do not equate every UDP/80 listener with HTTP/3; QUIC is normally associated with UDP/443. |
| 88 | TCP | Assigned [TCP] | System/Known | Kerberos authentication. | 1988 | Kerberos V5. |
| 88 | UDP | Assigned [UDP] | System/Known | Kerberos authentication. | 1988 | Kerberos V5. |
| 102 | TCP | Assigned [TCP] | System/Known | ISO Transport Service on top of TCP (RFC 1006). | 1987 | Used by several OSI-derived applications. |
| 104 | TCP | Assigned [TCP] | System/Known | DICOM network communications. | 1980s | Common default for DICOM. |
| 110 | TCP | Assigned [TCP] | System/Known | Post Office Protocol version 3 (POP3). | 1988 | Legacy plaintext POP3 port; POP3S normally uses 995/TCP. |
| 111 | TCP | Assigned [TCP] | System/Known | ONC RPC portmapper / rpcbind. | 1988 | Maps RPC programs to dynamic ports. |
| 111 | UDP | Assigned [UDP] | System/Known | ONC RPC portmapper / rpcbind. | 1988 | Legacy and current RPC environments. |
| 113 | TCP | Assigned [TCP] | System/Known | Identification Protocol (ident). | 1985 | Legacy. |
| 119 | TCP | Assigned [TCP] | System/Known | Network News Transfer Protocol (NNTP). | 1986 | Usenet/news transport. |
| 123 | UDP | Assigned [UDP] | System/Known | Network Time Protocol (NTP). | 1985 | Standard NTP transport. |
| 123 | TCP | Assigned [TCP] | System/Known | NTP over TCP / TCP fallback or application-specific use. | 1985 | UDP is the normal NTP transport. |
| 135 | TCP | Assigned [TCP] | System/Known | Microsoft RPC Endpoint Mapper (EPMAP). | 1993 | Windows RPC infrastructure. |
| 135 | UDP | Assigned [UDP] | System/Known | Microsoft RPC Endpoint Mapper / legacy RPC discovery. | 1993 | Windows RPC infrastructure. |
| 137 | UDP | Assigned [UDP] | System/Known | NetBIOS Name Service. | 1983 | Legacy Windows networking. |
| 138 | UDP | Assigned [UDP] | System/Known | NetBIOS Datagram Service. | 1983 | Legacy Windows networking. |
| 139 | TCP | Assigned [TCP] | System/Known | NetBIOS Session Service. | 1983 | Legacy Windows networking; SMB commonly uses 445/TCP directly on modern systems. |
| 143 | TCP | Assigned [TCP] | System/Known | Internet Message Access Protocol (IMAP). | 1986 | Standard IMAP. |
| 161 | UDP | Assigned [UDP] | System/Known | Simple Network Management Protocol (SNMP) queries. | 1988 | SNMP management traffic. |
| 161 | TCP | Assigned [TCP] | System/Known | SNMP over TCP. | 1988 | Less common than UDP. |
| 162 | UDP | Assigned [UDP] | System/Known | SNMP Trap / Inform receiver. | 1988 | Standard trap transport. |
| 162 | TCP | Assigned [TCP] | System/Known | SNMP over TCP / application-specific trap use. | 1988 | Less common than UDP. |
| 179 | TCP | Assigned [TCP] | System/Known | Border Gateway Protocol (BGP). | 1989 | Standard BGP transport. |
| 389 | TCP | Assigned [TCP] | System/Known | Lightweight Directory Access Protocol (LDAP). | 1993 | Standard LDAP. |
| 389 | UDP | Assigned [UDP] | System/Known | LDAP over UDP / historical or specialized use. | 1993 | TCP is the normal LDAP transport. |
| 443 | TCP | Assigned [TCP] | System/Known | HTTP Secure (HTTPS), normally HTTP over TLS. | 1994 | Widely used secure web port. |
| 443 | UDP | Assigned [UDP] | System/Known | QUIC, including HTTP/3. | 2012 | Modern HTTP/3 default transport. |
| 445 | TCP | Assigned [TCP] | System/Known | Microsoft-DS / SMB directly over TCP. | 1990s | Primary modern SMB transport on Windows networks. |
| 465 | TCP | Assigned [TCP] | System/Known | SMTP submission over implicit TLS (SMTPS). | 1997 | Historically deprecated and later reassigned for message submission over TLS. |
| 500 | UDP | Assigned [UDP] | System/Known | Internet Key Exchange (IKE / ISAKMP). | 1998 | IPsec key-management traffic. |
| 514 | UDP | Assigned [UDP] | System/Known | Syslog. | 1980s | Traditional syslog transport; modern secured deployments often use 6514/TCP. |
| 514 | TCP | Assigned [TCP] | System/Known | Legacy shell / command and syslog-related uses. | 1980s | Multiple historical assignments; see IANA/RFC documentation. |
| 515 | TCP | Assigned [TCP] | System/Known | Line Printer Daemon / Line Printer Remote (LPD/LPR). | 1988 | Legacy network printing protocol. |
| 520 | UDP | Assigned [UDP] | System/Known | Routing Information Protocol (RIP). | 1988 | Legacy interior routing protocol. |
| 546 | UDP | Assigned [UDP] | System/Known | DHCPv6 client. | 1998 | DHCPv6. |
| 547 | UDP | Assigned [UDP] | System/Known | DHCPv6 server/relay. | 1998 | DHCPv6. |
| 548 | TCP | Assigned [TCP] | System/Known | Apple Filing Protocol (AFP). | 1988 | Legacy on modern Apple systems. |
| 554 | TCP | Assigned [TCP] | System/Known | Real Time Streaming Protocol (RTSP). | 1998 | Media control protocol. |
| 554 | UDP | Assigned [UDP] | System/Known | RTSP / RTP-related application use. | 1998 | Implementations vary in how media streams are transported. |
| 563 | TCP | Assigned [TCP] | System/Known | NNTP over TLS (NNTPS). | 1997 | Secure NNTP. |
| 587 | TCP | Assigned [TCP] | System/Known | Message submission (SMTP submission). | 1998 | Preferred authenticated mail-submission port. |
| 631 | TCP | Assigned [TCP] | System/Known | Internet Printing Protocol (IPP). | 1999 | Widely used network-printing protocol. |
| 631 | UDP | Assigned [UDP] | System/Known | IPP-related UDP discovery/application use. | 1999 | TCP is the normal IPP transport. |
| 636 | TCP | Assigned [TCP] | System/Known | LDAP over TLS (LDAPS). | 1997 | Direct TLS LDAP connection. |
| 646 | TCP | Assigned [TCP] | System/Known | Label Distribution Protocol (LDP). | 2001 | MPLS signaling. |
| 646 | UDP | Assigned [UDP] | System/Known | LDP discovery/related UDP use. | 2001 | TCP carries the primary LDP session. |
| 853 | TCP | Assigned [TCP] | System/Known | DNS over TLS (DoT). | 2016 | Encrypted DNS. |
| 853 | UDP | Assigned [UDP] | System/Known | DNS over QUIC / encrypted DNS deployments. | 2022 | RFC-defined DNS over QUIC uses UDP/853. |
| 873 | TCP | Assigned [TCP] | System/Known | rsync file synchronization. | 1996 | Standard rsync daemon port. |
| 902 | TCP | Assigned [TCP] | System/Known | VMware server / remote management traffic. | 1998 | VMware product usage varies by version. |
| 903 | TCP | Assigned [TCP] | System/Known | VMware remote console. | 1998 | Legacy VMware remote console transport. |
| 989 | TCP | Assigned [TCP] | System/Known | FTPS data. | 1997 | FTP over TLS/SSL data channel. |
| 990 | TCP | Assigned [TCP] | System/Known | FTPS control. | 1997 | FTP over TLS/SSL control channel. |
| 992 | TCP | Assigned [TCP] | System/Known | Telnet over TLS/SSL. | 1996 | Legacy secure Telnet. |
| 993 | TCP | Assigned [TCP] | System/Known | IMAP over TLS (IMAPS). | 1996 | Secure IMAP. |
| 995 | TCP | Assigned [TCP] | System/Known | POP3 over TLS (POP3S). | 1996 | Secure POP3. |
| 1025 | TCP | Assigned [TCP] | User/Registered | Registered service port with historical Microsoft RPC/dynamic-service use. | 1980s | Windows commonly used ports beginning at 1025 dynamically; modern Windows RPC dynamic ranges are broader and configurable. |
| 1025 | UDP | Assigned [UDP] | User/Registered | Historically used registered services and dynamic application traffic. | 1980s | Also part of historical Windows dynamic-port discussions. |
| 1080 | TCP | Assigned [TCP] | User/Registered | SOCKS proxy. | 1992 | Common SOCKS proxy port. |
| 1080 | UDP | Assigned [UDP] | User/Registered | SOCKS-related UDP relay traffic. | 1992 | UDP ASSOCIATE is part of SOCKS. |
| 1099 | TCP | Assigned [TCP] | User/Registered | Java Remote Method Invocation (RMI) Registry. | 1997 | Standard RMI registry port. |
| 1194 | TCP | Assigned [TCP] | User/Registered | OpenVPN. | 2002 | Common OpenVPN default. |
| 1194 | UDP | Assigned [UDP] | User/Registered | OpenVPN. | 2002 | Common OpenVPN default and generally preferred transport. |
| 1352 | TCP | Assigned [TCP] | User/Registered | IBM Notes / Lotus Domino. | 1993 | Common Domino server port. |
| 1433 | TCP | Assigned [TCP] | User/Registered | Microsoft SQL Server database service. | 1993 | Default SQL Server instance port. |
| 1434 | UDP | Assigned [UDP] | User/Registered | SQL Server Browser. | 1998 | Helps clients locate named SQL Server instances. |
| 1521 | TCP | Assigned [TCP] | User/Registered | Oracle Net Listener. | 1980s | Common Oracle Database listener port. |
| 1701 | UDP | Assigned [UDP] | User/Registered | Layer 2 Tunneling Protocol (L2TP). | 1999 | L2TP commonly pairs with IPsec. |
| 1723 | TCP | Assigned [TCP] | User/Registered | Point-to-Point Tunneling Protocol (PPTP). | 1996 | Legacy/insecure VPN protocol. |
| 1812 | UDP | Assigned [UDP] | User/Registered | RADIUS authentication/authorization. | 1997 | Standard RADIUS authentication port. |
| 1812 | TCP | Assigned [TCP] | User/Registered | RADIUS over TCP. | 2017 | Modern RADIUS-over-TCP/related deployments; UDP remains common. |
| 1813 | UDP | Assigned [UDP] | User/Registered | RADIUS accounting. | 1997 | Standard accounting port. |
| 1883 | TCP | Assigned [TCP] | User/Registered | MQTT. | 1999 | Standard non-TLS MQTT port. |
| 1900 | UDP | Assigned [UDP] | User/Registered | Simple Service Discovery Protocol (SSDP), used by UPnP. | 1999 | Local-network discovery; generally not intended for Internet exposure. |
| 2049 | TCP | Assigned [TCP] | User/Registered | Network File System (NFS). | 1984 | NFS versions vary in transport behavior. |
| 2049 | UDP | Assigned [UDP] | User/Registered | NFS over UDP. | 1984 | Legacy/common in older deployments. |
| 2375 | TCP | Assigned [TCP] | User/Registered | Docker daemon API without TLS. | 2013 | Dangerous if exposed to untrusted networks; use TLS or a local socket. |
| 2376 | TCP | Assigned [TCP] | User/Registered | Docker daemon API with TLS. | 2013 | Secure Docker daemon TCP port. |
| 2181 | TCP | Assigned [TCP] | User/Registered | Apache ZooKeeper client/server connection. | 2010 | Default ZooKeeper client port. |
| 3000 | TCP | Assigned [TCP] | User/Registered | HTTP alternate/development services; widely used by applications such as Grafana. | 1990s | Common real-world port; not synonymous with one service. |
| 3128 | TCP | Assigned [TCP] | User/Registered | Squid HTTP proxy. | 1996 | Default Squid proxy port. |
| 3260 | TCP | Assigned [TCP] | User/Registered | iSCSI target. | 2000 | Standard iSCSI transport. |
| 3268 | TCP | Assigned [TCP] | User/Registered | Microsoft Global Catalog. | 1999 | Active Directory Global Catalog. |
| 3269 | TCP | Assigned [TCP] | User/Registered | Microsoft Global Catalog over SSL/TLS. | 1999 | Secure Global Catalog. |
| 3306 | TCP | Assigned [TCP] | User/Registered | MySQL/MariaDB database server. | 1995 | Common default database port. |
| 3389 | TCP | Assigned [TCP] | User/Registered | Microsoft Remote Desktop Protocol (RDP). | 1998 | Standard RDP TCP transport. |
| 3389 | UDP | Assigned [UDP] | User/Registered | Microsoft RDP UDP transport. | 2012 | Modern RDP can use UDP alongside TCP. |
| 3478 | TCP | Assigned [TCP] | User/Registered | STUN/TURN server traffic. | 2003 | NAT traversal and media relay. |
| 3478 | UDP | Assigned [UDP] | User/Registered | STUN/TURN server traffic. | 2003 | Common UDP NAT-traversal transport. |
| 3689 | TCP | Assigned [TCP] | User/Registered | DAAP (Digital Audio Access Protocol). | 2003 | Historically associated with iTunes/DAAP. |
| 3690 | TCP | Assigned [TCP] | User/Registered | Subversion (SVN) protocol. | 2000 | Standard SVN server port. |
| 4369 | TCP | Assigned [TCP] | User/Registered | Erlang Port Mapper Daemon (EPMD). | 1998 | Maps Erlang distributed-node ports. |
| 4444 | TCP | Assigned [TCP] | User/Registered | Common application-specific use; historically associated with Metasploit payload handlers and other development tools. | 1990s | Not synonymous with Metasploit; widespread unofficial use exists. |
| 4444 | UDP | Assigned [UDP] | User/Registered | Common application-specific use. | 1990s | Broad unofficial use; verify the application. |
| 4500 | UDP | Assigned [UDP] | User/Registered | IPsec NAT Traversal (NAT-T). | 2005 | Used with IKE/IPsec. |
| 5060 | TCP | Assigned [TCP] | User/Registered | Session Initiation Protocol (SIP). | 2002 | SIP signaling. |
| 5060 | UDP | Assigned [UDP] | User/Registered | Session Initiation Protocol (SIP). | 2002 | Common SIP transport. |
| 5061 | TCP | Assigned [TCP] | User/Registered | SIP over TLS. | 2002 | Secure SIP signaling. |
| 5061 | UDP | Assigned [UDP] | User/Registered | SIP over DTLS / application-specific secure signaling. | 2002 | Transport depends on implementation. |
| 5222 | TCP | Assigned [TCP] | User/Registered | XMPP client-to-server. | 1999 | Standard XMPP client connection port. |
| 5269 | TCP | Assigned [TCP] | User/Registered | XMPP server-to-server. | 1999 | Standard XMPP inter-server port. |
| 5353 | UDP | Assigned [UDP] | User/Registered | Multicast DNS (mDNS). | 2003 | Local-link discovery; uses multicast 224.0.0.251/ff02::fb. |
| 5432 | TCP | Assigned [TCP] | User/Registered | PostgreSQL. | 1996 | Default PostgreSQL server port. |
| 5432 | SCTP | Assigned [SCTP] | User/Registered | PostgreSQL/application-specific SCTP registration. | 1996 | Verify the application before assuming SCTP is in use. |
| 5555 | TCP | Assigned [TCP] | User/Registered | Common application/debugging use, including Android Debug Bridge (ADB) over TCP. | 2008 | Also used by many unrelated applications. |
| 5555 | UDP | Assigned [UDP] | User/Registered | Common application-specific use. | 1990s | Not synonymous with ADB. |
| 5671 | TCP | Assigned [TCP] | User/Registered | AMQP over TLS. | 2008 | Common RabbitMQ TLS port. |
| 5672 | TCP | Assigned [TCP] | User/Registered | Advanced Message Queuing Protocol (AMQP). | 2003 | Common RabbitMQ non-TLS port. |
| 5683 | UDP | Assigned [UDP] | User/Registered | Constrained Application Protocol (CoAP). | 2014 | Standard unsecured CoAP. |
| 5684 | UDP | Assigned [UDP] | User/Registered | CoAP over DTLS. | 2014 | Secure CoAP. |
| 5900 | TCP | Assigned [TCP] | User/Registered | Virtual Network Computing (VNC) / RFB, display :0. | 1998 | Display number normally maps to 5900 + display. |
| 5985 | TCP | Assigned [TCP] | User/Registered | Windows Remote Management (WinRM) over HTTP. | 2003 | Microsoft management protocol. |
| 5986 | TCP | Assigned [TCP] | User/Registered | WinRM over HTTPS. | 2003 | Secure WinRM. |
| 6000 | TCP | Assigned [TCP] | User/Registered | X Window System display :0. | 1984 | Traditional X11 TCP port; many modern systems disable network X11. |
| 6001 | TCP | Assigned [TCP] | User/Registered | X Window System display :1. | 1984 | X11 port = 6000 + display number. |
| 6379 | TCP | Assigned [TCP] | User/Registered | Redis. | 2009 | Default Redis server port. |
| 6443 | TCP | Assigned [TCP] | User/Registered | Kubernetes API server. | 2014 | Common Kubernetes API endpoint. |
| 6514 | TCP | Assigned [TCP] | User/Registered | Syslog over TLS. | 2008 | Secure syslog transport. |
| 6667 | TCP | Assigned [TCP] | User/Registered | Internet Relay Chat (IRC). | 1988 | Common IRC server port. |
| 6667 | UDP | Assigned [UDP] | User/Registered | Historical/implementation-specific IRC-related use. | 1988 | TCP is the normal IRC transport. |
| 6881–6889 | TCP | Assigned [TCP] | User/Registered | Common BitTorrent peer-to-peer traffic range. | 2001 | Historical/default BitTorrent range; modern clients can use arbitrary ports. |
| 6881–6889 | UDP | Assigned [UDP] | User/Registered | BitTorrent peer-to-peer traffic and DHT/related protocols. | 2001 | Modern clients can use arbitrary ports. |
| 7000 | TCP | Assigned [TCP] | User/Registered | AFS fileserver / various application services. | 1989 | AFS uses a family of ports; other applications also use 7000. |
| 8000 | TCP | Assigned [TCP] | User/Registered | Common HTTP alternate/development server port. | 1990s | No single standardized application meaning. |
| 8080 | TCP | Assigned [TCP] | User/Registered | Common HTTP alternate, proxy, and web-application port. | 1990s | Extremely common unofficial/application-specific use. |
| 8080 | UDP | Assigned [UDP] | User/Registered | Application-specific alternate HTTP/UDP use. | 1990s | Not equivalent to HTTP/TCP in every application. |
| 8443 | TCP | Assigned [TCP] | User/Registered | Common HTTPS alternate/application port. | 1990s | Widely used by web applications and administration interfaces. |
| 8888 | TCP | Assigned [TCP] | User/Registered | Common HTTP alternate; widely used by Jupyter and other development software. | 1990s | Application-specific rather than one universal service. |
| 9000 | TCP | Assigned [TCP] | User/Registered | Common application/web service port; used by various software including PHP-FPM-related and development services. | 1990s | Meaning varies substantially by application. |
| 9090 | TCP | Assigned [TCP] | User/Registered | Common HTTP/application port; widely used by Prometheus. | 2012 | Prometheus default web UI/API port. |
| 9100 | TCP | Assigned [TCP] | User/Registered | JetDirect / raw network printing. | 1990s | Common raw-printing port. |
| 9200 | TCP | Assigned [TCP] | User/Registered | Elasticsearch HTTP/REST API. | 2010 | Default Elasticsearch HTTP port. |
| 9300 | TCP | Assigned [TCP] | User/Registered | Elasticsearch node-to-node transport. | 2010 | Elasticsearch internal transport. |
| 9418 | TCP | Assigned [TCP] | User/Registered | Git native protocol. | 2005 | Unencrypted Git transport; HTTPS/SSH are now more common for many workflows. |
| 10000 | TCP | Assigned [TCP] | User/Registered | Webmin administration interface. | 1999 | Common Webmin default port. |
| 10050 | TCP | Assigned [TCP] | User/Registered | Zabbix agent. | 2001 | Default Zabbix agent port. |
| 10051 | TCP | Assigned [TCP] | User/Registered | Zabbix server/trapper. | 2001 | Default Zabbix server port. |
| 11211 | TCP | Assigned [TCP] | User/Registered | Memcached. | 2003 | Common Memcached TCP port. |
| 11211 | UDP | Assigned [UDP] | User/Registered | Memcached over UDP. | 2003 | UDP is optional; exposed UDP memcached has historically been abused for amplification. |
| 15672 | TCP | Assigned [TCP] | User/Registered | RabbitMQ Management HTTP API/UI. | 2007 | Management interface, not the AMQP data port. |
| 19132 | UDP | Assigned [UDP] | User/Registered | Minecraft Bedrock Edition server. | 2011 | Common/default Bedrock IPv4 server port. |
| 25565 | TCP | Assigned [TCP] | User/Registered | Minecraft Java Edition server protocol. | 2009 | Common/default Java Edition server port. |
| 25575 | TCP | Assigned [TCP] | User/Registered | Minecraft RCON. | 2009 | Remote console port; configurable. |
| 27015 | TCP | Assigned [TCP] | User/Registered | Steam/Source-engine game traffic and related services. | 2003 | Common Source-engine default; many games use the number differently. |
| 27015 | UDP | Assigned [UDP] | User/Registered | Steam/Source-engine game traffic and related services. | 2003 | Common Source-engine default; game-specific behavior varies. |
| 27017 | TCP | Assigned [TCP] | User/Registered | MongoDB database service. | 2009 | Default MongoDB port. |
| 32400 | TCP | Assigned [TCP] | User/Registered | Plex Media Server. | 2008 | Common/default Plex server port. |
| 51820 | UDP | Assigned [UDP] | Dynamic/Private | WireGuard VPN. | 2015 | Common default in examples and many deployments; WireGuard can use any UDP port. |
| 51821 | UDP | Assigned [UDP] | Dynamic/Private | Common alternate WireGuard deployment. | 2015 | Not the universal WireGuard port. |
| 54321 | TCP | Unassigned [TCP] | Dynamic/Private | Commonly reused by unrelated applications and development software. | — | Widely recognized application port number, but not a single universal service. |
| 54321 | UDP | Unassigned [UDP] | Dynamic/Private | Commonly reused by unrelated applications. | — | Application-specific/unofficial use. |

## Reading the table

- A port number may appear several times because different applications can share a number, and because TCP, UDP, SCTP, and DCCP registrations are independent.
- **Protocol Status** describes the specific transport protocol in that row, not all protocols using the same number.
- **Designation** follows the traditional IANA numeric ranges; it does not by itself mean that the service is still commonly deployed.
- **Date Created** is the earliest reliable date associated with the protocol/service when reasonably established. It is not automatically the IANA registration date. `—` means a reliable creation date could not be established without making a misleading guess.
- **Note(s)** is used for legacy status, obsolete protocols, unofficial/common application uses, security concerns, configurable ports, and other distinctions that would otherwise be lost in a compact table.

## Important distinction: assigned vs. commonly used

A port being commonly used by an application does not necessarily mean the application is the service officially associated with that port. Likewise, an IANA assignment does not guarantee that the service is still popular or even actively deployed. This reference intentionally preserves both kinds of information instead of collapsing them into a single service-name column.

## Primary references

1. **IANA.** [Service Name and Transport Protocol Port Number Registry](https://www.iana.org/assignments/service-names-port-numbers/service-names-port-numbers.xhtml)
2. **Wikipedia.** [List of TCP and UDP port numbers](https://en.wikipedia.org/wiki/List_of_TCP_and_UDP_port_numbers)
3. **RFC 6335.** [Service Name and Transport Protocol Port Number Registry](https://www.rfc-editor.org/rfc/rfc6335)
4. **Nmap.** [nmap-services](https://nmap.org/book/nmap-services.html)
5. **Microsoft Learn.** [Service overview and network port requirements](https://learn.microsoft.com/en-us/troubleshoot/windows-server/networking/service-overview-and-network-port-requirements)
