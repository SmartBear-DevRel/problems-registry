---
layout: ../layouts/Problem.astro
title: Validation Error
description: This problem occurs when the request is deemed unprocessable. 
---

Your client issued a request that failed validation. Certain validation libraries return multi-errors and cannot be easily parsed into discreet types. This problem type, afforded the provider with the ability to surface all validation errors and negate the need for a trial and error workflow on your side. 

Please review your request to determine if you can remain within appropriate business rules. Consider validating your request against available metadata (e.g. schemas) prior to sending to the server.

| Type URI | Title | Recommended HTTP Status Code | Reference |
|----------|-------|------------------------------|-----------|
|https://problems-registry.smartbear.com/validation-error|Validation Error|422||

> **Note** A problem is generally **not** meant to be used for end-user input validation, but for client developer convenience. 

**Example of a `validation-error` problem details:**

```json
{
    "type": "https://problems-registry.smartbear.com/validation-error",
    "title": "Validation Error",
    "detail": "The request is not valid.",
    "status": 422,
    "code": "422-02",
    "errors": [
        {
            "detail": "Your request does not contain the required property {name}",
            "pointer": "#/name"
        },
        {
            "detail": "the path parameter does not conform to the expect format",
            "parameter": "petId"
        }       
     ]
}
```
