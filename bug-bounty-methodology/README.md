# Bug bounty methodology

> The complete beginner's field guide. Recon → enumerate → hunt → report.

A full eight-phase methodology for going from "I want to try bug bounty" to a
paid report. Covers the mindset, the program landscape, the recon-to-report
pipeline, the bug classes worth chasing, and the toolkit per phase.

**PDF:** [Bug-Bounty-Methodology.pdf](Bug-Bounty-Methodology.pdf)
**Instagram:** [@kerem.tech post](https://www.instagram.com/p/DaAJXJGDFwI)

## What's inside

**Foundation (slides 02–05)**
- What bug bounty is, and the legal frame (scope = your contract)
- Program types: paid bounty vs VDP, public vs private
- The hunter's mindset: assume it's broken, follow curiosity, be relentless
- Why follow a method — the funnel from 100% exposed → ~3% confirmed bugs

**The 8-phase roadmap (slides 06–16)**

| # | Phase | What you actually do |
|---|-------|----------------------|
| 1 | Scope & Rules | Read the scope twice. In-scope, out-of-scope, allowed methods |
| 2 | Passive Recon | WHOIS, DNS, dorking, cert transparency, public OSINT — no packets sent |
| 3 | Subdomain Enum | Passive sources, brute force, permutations, resolve & probe |
| 4 | Fingerprinting | Port/service scan, tech detection, screenshot triage, flag old versions |
| 5 | Content Discovery | Directories & files, hidden endpoints, JS mining, parameter discovery |
| 6 | Map the Surface | Roles & permissions, data/auth flows, interesting features, take notes |
| 7 | Exploit & Validate | Minimal PoC, concrete impact, stop once confirmed — never destructive |
| 8 | The Report | Title, summary, repro steps, PoC, impact, remediation |

**Bug classes to hunt (slides 13–14)**
- **Access & logic flaws** (beginner-friendly): IDOR, broken auth, access control bypasses, business logic abuse
- **Injection & web flaws**: XSS, SQL injection, SSRF, open redirect

**The toolkit (slide 17)** — the right tool per phase:

| Phase | Tools |
|-------|-------|
| Recon & OSINT | Amass · Subfinder · crt.sh · Shodan |
| Scanning | Nmap · Naabu · Masscan · RustScan |
| Content discovery | ffuf · feroxbuster · gobuster · dirsearch |
| Intercept proxy | Burp Suite · Caido · ZAP · mitmproxy |
| Web recon | httpx · katana · gau · waybackurls |
| Vuln scanning | Nuclei · dalfox · sqlmap · nikto |

**Avoid these (slide 18)** — testing out of scope, no-impact reports, chasing
easy duplicates, messy writeups.

**Where to practice (slide 19)** — vulnerable labs, guided academies,
disclosed-report reading, starting on VDPs to build a track record.

## Who it's for

Newcomers who want a real methodology instead of just a tool list, junior
pentesters moving into bug bounty, and CTF players ready to test their skills
on real (in-scope) targets.

For deep dives on specific recon and exploitation skills, see
[NMAP — The ultimate guide](../nmap-ultimate-guide/) for scanning,
[The ultimate Wireshark guide](../wireshark-ultimate-guide/) for traffic
analysis, and [Linux privilege escalation](../linux-priv-esc/) for once you
get a foothold.

> Golden rule: no permission, no testing. The scope is your contract — never
> step outside it.
