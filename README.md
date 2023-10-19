# problems
[Problem registry](https://problems-registry.smartbear.com/) for SmartBear API responses conforming to Problem Details [RFC 9457](https://www.rfc-editor.org/info/rfc9457) (formally [RFC 7808](https://www.rfc-editor.org/info/rfc7807)).

## Contribute
If you would like to add a new problem entry to the registry, submit a PR with the following type of changes:

 - Create a new `markdown` file in the `./src/pages` directory with the problem name as the filename (e.g. `missing-body-property.md`). 
Distinct words _should_ be hyphen separated in the filename.
 - The structure of the markdown should follow other problems already defined within `./src/pages` directory.
 - When supplying examples that specify an `errors` array object, it must conform to the [JSON Schema](#errors-json-schema) specified below.
 - Add a new `card` component to the `./src/pages/index.astro` file. An example of a card component is as follows:

```HTML
    <Card
        href="./missing-body-property"
        title="Missing Body Property"
        body="The request is missing an expected body property 🔍"
    />
```

### Errors JSON Schema
When necessary, a Problem Detail response _MAY_ include additional detail on the problems that have occurred. The additional errors **MUST** be under the `errors` collection which itself follows the following schema:

```json
{
	"$schema": "https://json-schema.org/draft/2019-09/schema",
	"type": "object",
	"properties": {
		"type": {
			"type": "string",
			"description": "a string containing a URI reference that identifies the problem type. When this member is not present, its value is assumed to be `about:blank`."
		},
		"status": {
			"type": "number",
			"description": "a number indicating the HTTP status code."
		},
		"title": {
			"type": "string",
			"description": "a string containing a short, human-readable summary of the problem type."
		},
		"detail": {
			"type": "string",
			"description": "a string containing a human-readable explanation specific to this occurrence of the problem."
		},
		"instance": {
			"type": "string",
			"description": "a string containing a URI reference that identifies the specific occurrence of the problem."
		},
		"code": {
			"type": "string",
			"description": "a string containing additional provider specific codes to identify the error context."
		},
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
							"description": "a string containing the name of the query or path parameter that is the source of error"
						},
						"header": {
							"type": "string",
							"description": "a string containing the name of the header that is the source of error"
						},
						"code": {
							"type": "string",
							"description": "a string containing additional provider specific codes to identify the error context."
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
		"title"
	]
}
```
