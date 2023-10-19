---
layout: ../layouts/Problem.astro
title: Invalid Body Property Format
description: This problem occurs when the request body contain a malformed property.
---

Your client issued a request that contained a malformed body property. Please review your request and compare against the shared API definition. Consider validating your request against the published schema prior to sending to the server.

| Type URI | Title | Recommended HTTP Status Code | Reference |
|----------|-------|------------------------------|-----------|
|https://problems-registry.smartbear.com/invalid-body-property-format|Invalid Body Property Format|400||

> **Note** A problem is generally **not** meant to be used for end-user input validation, but for client developer convenience. 


**Example of an `invalid-body-property-format` problem details:**
```json
{
    "type": "https://problems-registry.smartbear.com/invalid-body-property-format",
    "title": "Invalid Body Property Format",
    "detail": "The request body contains a malformed property.",
    "status": 400,
    "code": "400-04",
    "errors": [
        {
            "detail": "must be a positive integer",
            "pointer": "#/quantity"
        }
     ]
}
```

