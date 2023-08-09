---
layout: ../layouts/Problem.astro
title: Business Rule Violation
description: This problem occurs when the request is deemed invalid as it fails to meet business rule expectations.
---

Your client issued a request that failed business rule validation. Please review your request to determine if you can remain within appropriate business rules. Consider validating your request against available metadata (e.g. schemas) prior to sending to the server.

| Type URI | Title | Recommended HTTP Status Code | Reference |
|----------|-------|------------------------------|-----------|
|https://problems-registry.smartbear.com/business-rule-violation|Business Rule Violation|422||

> **Note** A problem is generally **not** meant to be used for end-user input validation, but for client developer convenience. 


**Example of an `business-rule-violation` problem details:**
```yaml
{
    "type": "https://problems-registry.smartbear.com/business-rule-violation",
    "title": "Business Rule Violation",
    "detail": "The request body is invalid and not meeting business rules.",
    "status": 422,
    "code": "422-01",
    "errors": [
        {
            "detail": "maximum quantity is 999",
            "pointer": "#/quantity"
        },
        {
            "detail": "we do not offer `next-day` delivery to non EU addresses",
            "pointer": "#/shippingAddress/country"
        },
        {
            "detail": "we do not offer `next-day` delivery to non EU addresses",
            "pointer": "#/shippingOption"
        }        
     ]
}
```

