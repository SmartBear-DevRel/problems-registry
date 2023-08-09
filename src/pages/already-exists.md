---
layout: ../layouts/Problem.astro
title: Already Exists
description: This problem occurs when the resource being created is found to already exist on the server.
---

Your client application tried to create a resource that already exists. Perhaps review your client logic to determine if a user should be able to send such a request.

| Type URI | Title | Recommended HTTP Status Code | Reference |
|----------|-------|------------------------------|-----------|
|https://problems-registry.smartbear.com/already-exists|Already Exists|409||

> **Note** A problem is generally **not** meant to be used for end-user input validation, but for client developer convenience. 


**Example of an `already-exists` problem details:**
```yaml
{
    "type": "https://problems-registry.smartbear.com/already-exists",
    "title": "Already exists",
    "detail": "The resource being created already exists.",
    "status": 409,
    "code": "409-01"    
}
```

