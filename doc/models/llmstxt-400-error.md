
# Llmstxt 400 Error

*This model accepts additional fields of type unknown.*

## Structure

`Llmstxt400Error`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `success` | `boolean \| undefined` | Optional | - |
| `error` | `string \| undefined` | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
try {
  // make the API call
} catch (error) {
  if (error instanceof Llmstxt400Error) {
    console.log(error.result);
  }
}
```

