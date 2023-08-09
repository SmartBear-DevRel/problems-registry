---
layout: ../layouts/Problem.astro
title: Service unavailable
description: This problem occurs when the service requested is currently unavailable and the server is not ready to handle the request
---

Your client application did everything correct. Unfortunately our API is currently unavailable.

| Type URI | Title | Recommended HTTP Status Code | Reference |
|----------|-------|------------------------------|-----------|
|about:blank|See HTTP Status Code|N/A|[RFC9457](https://www.iana.org/go/rfc9457)|


> **Note** A problem is generally **not** meant to be used for end-user input validation, but for client developer convenience. 


**Examples of a `service-unavailable` problem details:**
```yaml
{
    "type": "https://problems-registry.smartbear.com/problems/service-unavailable",
    "title": "Service Unavailable",
    "detail": "The service is currently unavailable",
    "status": 503,
    "code": "503-01"    
}
```

```yaml
{
    "type": "about:blank",
    "title": "Service Unavailable",
    "detail": "The service is currently unavailable",
    "status": 503,
    "code": "503-01"    
}
```

