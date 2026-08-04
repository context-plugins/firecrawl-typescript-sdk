
# Extract 400 Error

*This model accepts additional fields of type unknown.*

## Structure

`Extract400Error`

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
  if (error instanceof Extract400Error) {
    console.log(error.result);
  }
}
```

