---
layout: ../layouts/Problem.astro
title: Invalid Request Parameter Format
description: This problem occurs when the request contains a malformed query or path parameter.
---

Your client issued a request that contained a malformed query or path parameter. Please review your request parameters and compare against the shared API definition. Consider validating your parameters published schema prior to sending to the server.

| Type URI | Title | Recommended HTTP Status Code | Reference |
|----------|-------|------------------------------|-----------|
|https://problems-registry.smartbear.com/invalid-request-parameter-format|Invalid Request Parameter Format|400||

> **Note** A problem is generally **not** meant to be used for end-user input validation, but for client developer convenience. 


**Example of an `invalid-request-parameter-format` problem details:**
```json
{
    "type": "https://problems-registry.smartbear.com/invalid-request-parameter-format",
    "title": "Invalid Request Parameter Format",
    "detail": "The request contains a malformed query parameter.",
    "status": 400,
    "code": "400-05",
    "errors": [
        {
            "detail": "the expected string values are ASC or DSC",
            "parameter": "sort"
        }
     ]
}
```

