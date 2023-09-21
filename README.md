# problems
Problem registry for SmartBear API responses conforming to Problem Details RFC 9457 (formally RFC 7808).

## Contribute
If you would like to add a new problem entry to the registry, submit a PR with the following type of changes:

1. Create a new `markdown` file in the `./src/pages` directory with the problem name as the filename (e.g. `missing-body-property.md`). 
Distinct words _should_ be hyphen separated in the filename.
2. The structure of the markdown should follow other problems already defined within `./src/pages` directory.
3. When supplying examples that specify an `errors` array object, it must conform to the [JSON Schema](#errors-json-schema) specified below.
4. Add a new `card` component to the `./src/pages/index.astro` file. An example of a card component is as follows:

```HTML
    <Card
        href="./missing-body-property"
        title="Missing Body Property"
        body="The request is missing an expected body property 🔍"
    />
```

### Errors JSON Schema
When necessary, a Problem Detail response `MAY` include additional detail on the problems that have occurred. The additional errors `MUST` be under the `errors` collection which itself follows the following schema:

```json
{
  "$schema": "https://json-schema.org/draft/2019-09/schema",
  "type": "object",
  "description": "an extension object used to enrich problem details responses for SmartBear APIs",
  "properties": {
    "errors": {
      "type": "array",
      "description": "an array of error details to accompany a problem details response",
      "items": [
        {
          "type": "object",
          "description": "an error object to provide explicit details on a problem towards an API consumer",
          "properties": {
            "detail": {
              "type": "string",
              "description": "a granular description on the specific error related to a body property, query parameter, path parameters, and/or header"
            },
            "pointer": {
              "type": "string",
              "description": "a JSON Pointer to a specific request body property that is the source of error"
            },
            "parameter": {
              "type": "string",
              "description": "the name of the query or path parameter that is the source of error"
            },
            "header": {
              "type": "string",
              "description": "the name of the header that is the source of error"
            }
          },
          "required": [
            "detail"
          ]
        }
      ]
    }
  },
  "required": [
    "errors"
  ]
}
```
