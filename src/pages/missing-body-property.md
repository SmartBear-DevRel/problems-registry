---
layout: ../layouts/Problem.astro
title: Missing Body Property
description: This problem occurs when the request sent to the API is missing an expected body property.
---

Your client issued a request that omitted an expected body property. Please review and consider validating your request against the published schema prior sending across the wire.

| Type URI | Title | Recommended HTTP Status Code | Reference |
|----------|-------|------------------------------|-----------|
|https://problems-registry.smartbear.com/missing-body-property|Missing Body Property|400||

> **Note** A problem is generally **not** meant to be used for end-user input validation, but for client developer convenience. 


**Example of an `missing-body-property` problem details:**
```json
{
    "type": "https://problems-registry.smartbear.com/missing-body-property",
    "title": "Missing body property",
    "detail": "The request is missing an expected body property.",
    "status": 400,
    "code": "400-09",
    "errors": [
        {
            "detail": "The body property {name} is required",
            "pointer": "#/name"
        }
     ]        
}
```

