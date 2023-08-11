---
layout: ../layouts/Problem.astro
title: Missing Request Header
description: This problem occurs when the request sent to the API is missing an expected request header.
---

Your client issued a request that omitted an expected request header. Please review and consider validating your request against the published schema prior sending across the wire.

| Type URI | Title | Recommended HTTP Status Code | Reference |
|----------|-------|------------------------------|-----------|
|https://problems-registry.smartbear.com/missing-request-header|Missing Request Header|400||

> **Note** A problem is generally **not** meant to be used for end-user input validation, but for client developer convenience. 


**Example of an `missing-request-header` problem details:**
```yaml
{
    "type": "https://problems-registry.smartbear.com/missing-request-header",
    "title": "Missing request header",
    "detail": "The request is missing an expected HTTP request header.",
    "status": 400,
    "code": "400-02",
    "errors": [
        {
            "detail": "The header {Accept} is required",
            "header": "Accept"
        }
    ]    
}
```

