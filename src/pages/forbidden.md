---
layout: ../layouts/Problem.astro
title: Forbidden
description: This problem occurs when the requested resource (and/or operation combination) is not authorized for the requesting client (and or authorization context).
---

Your client application tried to perform an operation on a resource that it's not authorized to perform in the given context.

> **Note** A problem is generally **not** meant to be used for end-user input validation, but for client developer convenience. 


**Example of a `forbidden` problem details:**
```yaml
{
    "type": "https://problems-registry.smartbear.com/problems/forbidden",
    "title": "Forbidden",
    "detail": "The resource could not be returned as the requestor is not authorized",
    "status": 403,
    "code": "403-01"    
}
```
