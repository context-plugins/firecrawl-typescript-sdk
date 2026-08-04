
# Crawl Errors 402 Error

*This model accepts additional fields of type unknown.*

## Structure

`CrawlErrors402Error`

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
  if (error instanceof CrawlErrors402Error) {
    console.log(error.result);
  }
}
```

