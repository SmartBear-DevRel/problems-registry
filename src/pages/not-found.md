---
layout: ../layouts/Problem.astro
title: Not Found
description: This problem occurs when the requested resource could not be found.
---

Your client application tried to access a resource that does not exist (or could not be found). Perhaps review how your users initiated such a request.

> **Note** A problem is generally **not** meant to be used for end-user input validation, but for client developer convenience. 

**Example of an `not-found` problem details:**

```yaml
{
    "type": "https://problems-registry.smartbear.com/problems/not-found",
    "title": "Not Found",
    "detail": "The requested resource was not found",
    "status": 404,
    "code": "404-01"    
}
```


