
# Crawl 404 Error

*This model accepts additional fields of type unknown.*

## Structure

`Crawl404Error`

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
  if (error instanceof Crawl404Error) {
    console.log(error.result);
  }
}
```

