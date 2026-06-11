# Linux privilege escalation

> How a normal user becomes root — 11 techniques inside.

A field guide to the eleven privilege-escalation vectors that come up over and
over on Linux boxes. Each one gets the same treatment: what the
misconfiguration is, the exact commands to find and exploit it, and the
hardening step that closes it.

**PDF:** [linux-privilege-escalation.pdf](linux-privilege-escalation.pdf)
**Instagram:** [@kerem.tech post](https://www.instagram.com/p/DZcJQPZjFmn)

## What's inside

**Foundation (slides 02–03)**
- The path to root: foothold → enumerate → find flaw → escalate → root
- Vertical vs horizontal escalation
- The enumeration mindset — `id`, `sudo -l`, `uname -a`, `find / -perm -4000`, `getcap -r /`
- Automation: `linPEAS` and `pspy`

**11 techniques (slides 04–14)**

| # | Slide | Vector | Find it with |
|---|-------|--------|--------------|
| 01 | 04 | SUID binaries | `find / -perm -4000 2>/dev/null` |
| 02 | 05 | Sudo rights (NOPASSWD, shell breakouts) | `sudo -l` |
| 03 | 06 | Linux capabilities (`cap_setuid` et al) | `getcap -r / 2>/dev/null` |
| 04 | 07 | Cron jobs (writable scripts / PATH) | `cat /etc/crontab`, `pspy` |
| 05 | 08 | PATH hijacking | scripts calling commands by name |
| 06 | 09 | Writable `/etc/passwd` | `ls -l /etc/passwd` |
| 07 | 10 | Kernel exploits (DirtyPipe / COW / PwnKit) | `uname -r` → CVE match |
| 08 | 11 | NFS `no_root_squash` | `cat /etc/exports` |
| 09 | 12 | `LD_PRELOAD` abuse via `env_keep` | `sudo -l` |
| 10 | 13 | Wildcard injection (e.g. tar `--checkpoint`) | root scripts using `*` |
| 11 | 14 | `docker` / `lxd` group membership | `id` |

Each technique slide gives a copy-paste enumeration command, the actual
exploitation steps, and a one-line **harden** recommendation.

## Who it's for

Pentesters and red teamers running the privesc checklist on engagements, CTF
players working HTB / THM boxes, blue teamers auditing their own hosts before
attackers do, and students prepping for OSCP / CRTP.

> Practice on a safe lab box. Don't try these on systems you don't own or have
> written permission to test.
