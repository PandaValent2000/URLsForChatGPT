# Port Status Legend

These indicators are based on the **five-state legend used by Wikipedia's [List of TCP and UDP port numbers](https://en.wikipedia.org/wiki/List_of_TCP_and_UDP_port_numbers)**, adapted for this reference's separate TCP/UDP/SCTP/DCCP status model.

| **Indicator** | **Protocol Status** | **Meaning** |
|---|---|---|
| 🟢 | **Assigned — Standard/Widely Used** | The protocol is assigned this port by IANA **and** is standardized, specified, or widely used on the port. |
| 🔵 | **Unofficial — Standard/Widely Used** | The protocol is **not** assigned this port by IANA, but is standardized, specified, or widely used on the port. |
| 🟡 | **Assigned — Limited/Unused** | The protocol is assigned this port by IANA, but is **not** standardized, specified, or widely used on the port. |
| 🔴 | **Unassigned / No Known Use** | The protocol is not assigned this port by IANA and is not known to be standardized, specified, or significantly used on the port. |
| ⚪ | **Reserved** | The port/protocol combination is reserved by IANA, generally to prevent collisions after a previous assignment was withdrawn. It may become available for assignment upon request. |

### Important

The indicator describes the **specific transport protocol in the row**, not the numeric port as a whole. TCP, UDP, SCTP, and DCCP are registered independently, so the same port number can legitimately have different status indicators for different transports.

The distinction between **Assigned** and **Standard/Widely Used** is intentional. An IANA assignment alone does not necessarily mean that a protocol is standardized, currently popular, or actively deployed. Likewise, an unofficial use can be important enough to document even when IANA has not assigned the port to it.

### Example

| **Port Number(s)** | **Transport Protocol** | **Protocol Status** |
|---:|---|---|
| 443 | TCP | 🟢 Assigned — Standard/Widely Used |
| 443 | UDP | 🟢 Assigned — Standard/Widely Used |
| 12345 | TCP | 🔵 Unofficial — Standard/Widely Used |
| 12345 | UDP | 🟡 Assigned — Limited/Unused |
| 000 | TCP | ⚪ Reserved |
| 000 | DCCP | 🔴 Unassigned / No Known Use |

The written status remains authoritative; the colored indicator is a quick visual aid.