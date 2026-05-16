# The ultimate Wireshark guide

> Filters · tips · tricks · tshark — 20 slides, the filters you'll actually reach for in a real investigation.

A focused Wireshark reference: the four-pane UI, the difference between capture
and display filters, seven copy-paste investigation filters for real incidents,
plus the Statistics menu, `tshark`, profiles, and a one-page cheatsheet.

**PDF:** [ultimate_wireshark_guide.pdf](ultimate_wireshark_guide.pdf)
**Instagram:** [@kerem.tech post](https://www.instagram.com/p/DYZlBM0jJHG)

## What's inside

**Foundation (slides 01–05)**
- 02 — What is Wireshark? (decodes 3000+ protocols; **does not** decrypt TLS without a key)
- 03 — The UI explained: packet list, details, bytes, filter bar
- 04 — Capture vs display filters: BPF before, Wireshark syntax after
- 05 — Display filter syntax: `==`, `!=`, `contains`, `matches`, `&&`, `||`, `!`

**Investigation playbooks (slides 06–12)** — copy-paste display filters for real incidents:

| # | Use case | Filter |
|---|----------|--------|
| 06 | Noise elimination | `!(arp \|\| icmp \|\| ssdp \|\| mdns \|\| llmnr \|\| nbns)` |
| 07 | Port scan detection | `tcp.flags.syn==1 && tcp.flags.ack==0 && tcp.window_size<=1024` |
| 08 | Host isolation | `ip.addr==X.X.X.X && (tcp \|\| udp) && !dns` |
| 09 | Credential hunt | `http.request.method=="POST" && frame contains "pass"` |
| 10 | DNS anomaly / C2 | `dns.flags.response==0 && dns.qry.name && frame.len gt 80` |
| 11 | Suspicious outbound | `tcp.flags==0x002 && !(ip.dst==192.168.0.0/16) && tcp.dstport!=443` |
| 12 | Data exfiltration | `tcp.len gt 1400 && !(ip.dst==192.168.0.0/16) && tcp.flags.push==1` |

**Operations (slides 13–18)**
- 13 — Follow TCP / UDP stream (`Ctrl+Alt+Shift+T`)
- 14 — Color rules — make anomalies impossible to miss
- 15 — Export Objects (HTTP, SMB, FTP-DATA, TFTP, DICOM)
- 16 — Statistics menu: Protocol Hierarchy, Conversations, Endpoints, I/O Graph, Flow Graph
- 17 — `tshark` essentials: `-i`, `-Y`, `-r`, `-T fields -e`, `-w`
- 18 — Profiles: save column layout, color rules, filters per use case (Pentest / IR / Web Debug / DNS)

**Reference (slide 19)** — one-slide cheatsheet of all seven filters + keyboard shortcuts.

## Who it's for

Network engineers troubleshooting latency and packet loss, security analysts
doing PCAP forensics, pentesters intercepting plaintext credentials and mapping
protocols, and blue teamers hunting C2, DNS tunneling, and exfiltration.
