---
layout: ../layouts/Problem.astro
title: Unauthorized
description: This problem occurs when the requested resource could not be returned as the client request lacked valid authentication credentials.
---

Your client application issued a requested to a protected resource without supplying the required auth details.

> **Note** A problem is generally **not** meant to be used for end-user input validation, but for client developer convenience. 


**Example of an `unauthorized` problem details:**
```yaml
{
    "type": "https://problems-registry.smartbear.com/problems/unauthorized",
    "title": "Unauthorized",
    "detail": "Access token not set or invalid, and the requested resource could not be returned",
    "status": 401,
    "code": "401-01"    
}
```
