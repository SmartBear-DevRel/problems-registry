---
layout: ../layouts/Problem.astro
title: Invalid Request Parameter Value
description: This problem occurs when the request contains a invalid query or path parameter value.
---

Your client issued a request that contained an invalid query or path parameter value. Please review your request and compare against the shared API definition where applicable. Consider validating your request against the published schema prior to sending to the server.

| Type URI | Title | Recommended HTTP Status Code | Reference |
|----------|-------|------------------------------|-----------|
|https://problems-registry.smartbear.com/invalid-request-parameter-value|Invalid Request Parameter Value|400||

> **Note** A problem is generally **not** meant to be used for end-user input validation, but for client developer convenience. 


**Example of an `invalid-request-parameter-value` problem details:**
```yaml
{
    "type": "https://problems-registry.smartbear.com/invalid-request-parameter-value",
    "title": "Invalid Request Parameter Value",
    "detail": "The request body contains an invalid request parameter value.",
    "status": 400,
    "code": "400-08",
    "errors": [
        {
            "detail": "'top-down' is not a valid sort parameter value. The expected string values are ASC or DSC",
            "parameter": "sort"
        }
     ]
}
```

