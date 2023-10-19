---
layout: ../layouts/Problem.astro
title: License Cancelled
description: This problem occurs when the license associated with the client has been cancelled thus rendering the service unavailable.
---

The license associated with your client/organization has been cancelled. Please contact your SmartBear account manager or representative.

| Type URI | Title | Recommended HTTP Status Code | Reference |
|----------|-------|------------------------------|-----------|
|https://problems-registry.smartbear.com/license-cancelled|License Cancelled|503||

> **Note** A problem is generally **not** meant to be used for end-user input validation, but for client developer convenience. 


**Example of an `license-expired` problem details:**
```json
{
    "type": "https://problems-registry.smartbear.com/license-cancelled",
    "title": "License Cancelled",
    "detail": "The service is unavailable as the license associated with your client or organization has been cancelled. Please contact your SmartBear account manager or representative",
    "status": 503
}
```

