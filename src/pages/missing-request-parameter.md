---
layout: ../layouts/Problem.astro
title: Missing Request Parameter
description: This problem occurs when the request sent to the API is missing an query or path parameter.
---

Your client issued a request that omitted an expected query or path par. Please review and consider validating your request against the published schema prior sending across the API endpoint.

| Type URI | Title | Recommended HTTP Status Code | Reference |
|----------|-------|------------------------------|-----------|
|https://problems-registry.smartbear.com/missing-request-parameter|Missing Request Parameter|400||

> **Note** A problem is generally **not** meant to be used for end-user input validation, but for client developer convenience. 


**Example of an `missing-request-parameter` problem details:**
```yaml
{
    "type": "https://problems-registry.smartbear.com/missing-request-parameter",
    "title": "Missing request parameter",
    "detail": "The request is missing an expected query or path parameter.",
    "status": 400,
    "code": "400-03",
    "errors": [
        {
            "detail": "The query parameter {name} is required",
            "parameter": "name"
        }
     ]    
}
```

