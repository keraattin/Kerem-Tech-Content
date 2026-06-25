# Network protocols explained

> The beginner's guide. How the internet actually talks, from zero.

A ground-up tour of the protocols that move every byte you read online — what
each one does, why it exists, and how they stack together. No prior network
knowledge assumed.

**PDF:** [Network-Protocols-Explained.pdf](Network-Protocols-Explained.pdf)
**Instagram:** [@kerem.tech post](https://www.instagram.com/p/DZ9ufRTDGBL)

## What's inside

**Mental model (slides 01–02)**
- What a protocol actually is: a shared language with format, order, and meaning
- The 4-layer stack: **Application** (HTTP, DNS, SMTP, SSH) → **Transport** (TCP, UDP) → **Internet** (IP, ICMP) → **Link** (Ethernet, Wi-Fi, ARP)

**Core protocols (slides 03–10)**
- **IP** — packets, headers, routers, IPv4 vs IPv6
- **TCP** — the 3-way handshake (SYN · SYN-ACK · ACK), guaranteed delivery
- **UDP** — fire-and-forget, no handshake, no resends
- **TCP vs UDP** — side-by-side trade-offs
- **DNS** — names to IPs, how a lookup actually works
- **DHCP** — auto-addressing via the DORA exchange (Discover · Offer · Request · Ack)
- **HTTP / HTTPS** — request/response loop, methods, status code families
- **TLS** — privacy, integrity, identity

**Application protocols (slides 11–14)**
- **Email** — SMTP (send) vs IMAP (sync) vs POP3 (download)
- **File transfer** — FTP (legacy) vs SFTP (recommended) vs TFTP (local only)
- **SSH** — encrypted remote shell, key-based login
- **ICMP & ARP** — the helpers that keep the network running quietly

**Reference (slide 15)** — well-known ports cheatsheet: `80` HTTP · `443` HTTPS ·
`53` DNS · `22` SSH · `21` FTP · `25` SMTP · `143` IMAP · `110` POP3 · `67/68` DHCP

## Who it's for

Anyone learning how the internet works for the first time — students,
career-switchers, junior developers, and anyone tired of nodding along when
people say "TCP handshake" without really knowing what it means.

For a deeper dive on specific topics: see [HTTP Anatomy](../http-anatomy/) for
the HTTP wire format and [Network ports you need to memorize](../network-ports-for-memorize/)
for the full pentester-grade port reference.
