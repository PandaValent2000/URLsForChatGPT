# Port Status Key

Use these indicators anywhere the port-reference tables show **Protocol Status**:

| **Indicator** | **Meaning** |
|---|---|
| 🟢 | **Assigned** — the port/protocol combination has an authoritative assignment or registration. |
| 🟡 | **Reserved** — intentionally held back or otherwise reserved rather than normally assignable. |
| 🔴 | **Unassigned** — no current assignment identified for that specific transport protocol. |

### Important

These indicators describe the **specific transport protocol in the row**. A single numeric port can therefore have different statuses for TCP, UDP, SCTP, and DCCP.

For example:

| **Port Number(s)** | **Transport Protocol** | **Protocol Status** |
|---:|---|---|
| 443 | TCP | 🟢 Assigned [TCP] |
| 443 | UDP | 🟢 Assigned [UDP] |
| 000 | TCP | 🟡 Reserved [TCP] |
| 000 | DCCP | 🔴 Unassigned [DCCP] |

The status indicator is intended as a quick visual aid; the written status remains authoritative.