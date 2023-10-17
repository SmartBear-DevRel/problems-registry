---
layout: ../layouts/Problem.astro
title: Bad Request
description: he server cannot or will not process the request due to something that is perceived to be a client error (for example, malformed request syntax, invalid request message framing, or deceptive request routing).
---

Your client application initiated a request that is malformed. Please review your client request against the defined semantics for the API.

| Type URI | Title | Recommended HTTP Status Code | Reference |
|----------|-------|------------------------------|-----------|
|about:blank|See HTTP Status Code|N/A|[RFC9457](https://www.iana.org/go/rfc9457)|


> **Note** A problem is generally **not** meant to be used for end-user input validation, but for client developer convenience. 


**Examples of a `bad-request` problem details:**
```json
{
    "type": "https://problems-registry.smartbear.com/bad-request",
    "title": "Bad Request",
    "detail": "The request is invalid or malformed",
    "status": 400,
    "code": "400-01"    
}
```

```json
{
    "type": "about:blank",
    "title": "Bad Request",
    "detail": "The request is invalid or malformed",
    "status": 400,
    "code": "400-01"    
}
```