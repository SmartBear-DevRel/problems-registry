---
layout: ../layouts/Problem.astro
title: Server Error
description: This problem occurs when the server encounters an unexpected condition that prevents it from fulfilling the request.
---

Your client application did everything correct. Unfortunately our API encountered a condition that resulted in this problem.

> **Note** A problem is generally **not** meant to be used for end-user input validation, but for client developer convenience. 


**Example of a `server-error` problem details:**
```yaml
{
    "type": "https://problems-registry.smartbear.com/problems/server-error",
    "title": "Server Error",
    "detail": "The server encountered an unexpected error",
    "status": 500,
    "code": "500-01"    
}
```

