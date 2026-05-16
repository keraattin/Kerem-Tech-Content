# HTTP Security Headers

> 10 headers. Every pentest report checks these. Most sites are missing half of them.

A pentester's cheatsheet for the HTTP response headers that show up in every
web security audit — what they do, what to set them to, and what to remove.

**PDF:** [HTTP_Security_Headers.pdf](HTTP_Security_Headers.pdf)
**Instagram:** [@kerem.tech post](https://www.instagram.com/p/DYO8-8ajJb8)

## Headers covered

1. `Strict-Transport-Security` (HSTS)
2. `X-Content-Type-Options`
3. `X-Frame-Options`
4. `Referrer-Policy`
5. `Permissions-Policy`
6. `Content-Security-Policy` (CSP)
7. `Cross-Origin-*` (COOP / COEP / CORP)
8. `Set-Cookie` (Secure · HttpOnly · SameSite)
9. `Clear-Site-Data`
10. Headers to **remove** (`Server`, `X-Powered-By`, etc.)

## References

- [OWASP Secure Headers Project](https://owasp.org/www-project-secure-headers/)
- [MDN — HTTP headers](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers)

## Who it's for

Web developers shipping HTTP services, pentesters writing report findings, and
ops engineers tuning reverse-proxy / CDN config.
