# Network ports you need to memorize

> 29 ports, 12 categories. The numbers you'll see on every pentest, every audit, every Shodan query.

A categorized reference of the network ports every dev, sysadmin, and security
person eventually has to know by heart — what each one is for, what to watch
for on it, and the recon commands that get you the first finding.

**PDF:** [network_ports_for_memorize.pdf](network_ports_for_memorize.pdf)
**Instagram:** [@kerem.tech post](https://www.instagram.com/p/DYjhWeWjIJw)

## Ports covered

| Category | Ports |
|----------|-------|
| Web | `80` HTTP · `443` HTTPS |
| Remote shell | `22` SSH · `23` Telnet |
| Remote desktop | `3389` RDP · `5900` VNC |
| File transfer | `21` FTP · `69` TFTP |
| Mail · outbound | `25` SMTP · `465` SMTPS · `587` Submission |
| Mail · inbound | `110` POP3 · `995` POP3S · `143` IMAP · `993` IMAPS |
| DNS & Kerberos | `53` DNS · `88` Kerberos |
| LDAP | `389` LDAP · `636` LDAPS |
| Windows / SMB | `135` MSRPC · `139` NetBIOS · `445` SMB |
| Databases · SQL | `1433` MSSQL · `3306` MySQL · `5432` Postgres |
| Databases · NoSQL | `6379` Redis · `27017` MongoDB |
| Network management | `161` SNMP · `514` Syslog · `123` NTP |

For each category the PDF gives a three-part breakdown:

- **Used for** — what the protocol actually carries in production
- **Watch for** — the classic misconfigurations and CVEs (BlueKeep, EternalBlue,
  Zerologon, AS-REP roasting, NBT-NS poisoning, anonymous LDAP bind, default
  SNMP communities, etc.)
- **Recon** — copy-paste `nmap`, `hydra`, `crackmapexec`, `impacket`, `ssh-audit`,
  and protocol-native commands

## Who it's for

Developers shipping services, sysadmins running infrastructure, IT generalists,
security analysts and pentesters, and students prepping for OSCP / Sec+ / CTFs.
