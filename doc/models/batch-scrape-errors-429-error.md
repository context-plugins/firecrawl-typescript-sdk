
# Batch Scrape Errors 429 Error

*This model accepts additional fields of type unknown.*

## Structure

`BatchScrapeErrors429Error`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `error` | `string \| undefined` | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
try {
  // make the API call
} catch (error) {
  if (error instanceof BatchScrapeErrors429Error) {
    console.log(error.result);
  }
}
```

