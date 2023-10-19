---
layout: ../layouts/Problem.astro
title: Invalid Body Property Value
description: This problem occurs when the request body contains a invalid property value.
---

Your client issued a request that contained an invalid body property value. Please review your request and compare against the shared API definition where applicable. Consider validating your request against the published schema prior to sending to the server.

| Type URI | Title | Recommended HTTP Status Code | Reference |
|----------|-------|------------------------------|-----------|
|https://problems-registry.smartbear.com/invalid-body-property-value|Invalid Body Property Value|400||

> **Note** A problem is generally **not** meant to be used for end-user input validation, but for client developer convenience. 


**Example of an `invalid-body-property-value` problem details:**
```json
{
    "type": "https://problems-registry.smartbear.com/invalid-body-property-value",
    "title": "Invalid Body Property Value",
    "detail": "The request body contains an invalid body property value.",
    "status": 400,
    "code": "400-07",
    "errors": [
        {
            "detail": "`Never` is an invalid value. Please provide `monthly` or `quarterly`",
            "pointer": "#/marketingCommunication/frequency"
        }
     ]
}
```

