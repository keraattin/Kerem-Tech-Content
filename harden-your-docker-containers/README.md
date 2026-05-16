# Harden your Docker containers

> 16 commands · production tested · CI ready

A practical Docker container hardening cheatsheet — what to actually run when
you ship containers to production, grouped by intent.

**PDF:** [docker_container_security.pdf](docker_container_security.pdf)
**Instagram:** [@kerem.tech post](https://www.instagram.com/p/DYW46WtjO-h)

## What's inside

- **Scanning (3)** — `docker scout cves`, `quickview`, `recommendations`
- **Hardening (5)** — `--read-only`, `--cap-drop`, `--security-opt no-new-privileges`, seccomp profiles
- **User & resources (3)** — non-root user, `--pids-limit`, `--memory`, `--cpus`
- **Isolation (2)** — internal networks, Swarm secrets
- **Audit (3)** — `docker history`, `docker inspect`, image trust / signing

## Who it's for

Developers shipping containers to production, SREs reviewing Dockerfiles, and
security engineers writing baseline policies for image builds.
