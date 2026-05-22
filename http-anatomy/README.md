# HTTP Anatomy

> Every developer uses it · few read it. What's actually in an HTTP request — the wire format that powers the entire web, line by line.

A line-by-line walkthrough of HTTP messages: how requests and responses are
built, what each slot means, and which methods, status codes, and headers
actually show up in real traffic.

**PDF:** [http_anatomy.pdf](http_anatomy.pdf)
**Instagram:** [@kerem.tech post](https://www.instagram.com/p/DYoqkE3DGoU)

## What's inside

**Message shape (slides 02–03)**
- The 4-part structure: start-line · headers · empty line (CRLF) · body
- Request line decoded: method · target (request-URI) · HTTP version

**Methods (slide 04)**
- `GET` · `POST` · `PUT` · `PATCH` · `DELETE`
- Each method's safety, idempotency, body-carrying, and intent

**Status line & codes (slides 05–09)**
- The three slots: version · 3-digit code · reason phrase
- **2xx success** — `200 OK`, `201 Created`, `204 No Content`
- **3xx redirect** — `301 Moved Permanently`, `302 Found`, `304 Not Modified`
- **4xx client error** — `401 Unauthorized`, `403 Forbidden`, `404 Not Found`
- **5xx server error** — `500 Internal Error`, `502 Bad Gateway`, `504 Gateway Timeout`

**Headers (slides 10–11)**
- **Request headers** — `Host`, `User-Agent`, `Accept`, `Authorization`, `Cookie`, `Content-Type`
- **Response headers** — `Content-Type`, `Content-Length`, `Set-Cookie`, `Cache-Control`, `Location`, `Server`

**Body encodings (slide 12)**
- `application/json` — APIs, modern web
- `application/x-www-form-urlencoded` — HTML forms, OAuth token endpoints
- `multipart/form-data` — file uploads, mixed data

**Real example (slide 13)** — one full `POST /api/login` request and its response, both shown end-to-end so the four parts line up across the round-trip.

## Who it's for

Backend and frontend developers who want a mental model of what `curl -v`
prints, students learning the web stack, and security folks who need the
baseline before reading the [HTTP Security Headers](../http-security-headers/)
cheatsheet.
