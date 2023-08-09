---
layout: ../layouts/Problem.astro
title: Invalid Request Header Format
description: This problem occurs when the request contains a malformed request header.
---

Your client issued a request that contained a malformed request header. Please review your request parameters and compare against the shared API definition when applicable. Consider validating your headers against the published schema or API definition metadata prior to sending to the server.

| Type URI | Title | Recommended HTTP Status Code | Reference |
|----------|-------|------------------------------|-----------|
|https://problems-registry.smartbear.com/invalid-request-header-format|Invalid Request Header Format|400||

> **Note** A problem is generally **not** meant to be used for end-user input validation, but for client developer convenience. 


**Example of an `invalid-request-header-format` problem details:**
```yaml
{
    "type": "https://problems-registry.smartbear.com/invalid-request-header-format",
    "title": "Invalid Request Header Format",
    "detail": "The request contains a malformed request header parameter.",
    "status": 400,
    "code": "400-06",
    "errors": [
        {
            "detail": "the request header was malformed",
            "header": "Accept"
        }
     ]
}
```

