
# Feedback Error Response Error

*This model accepts additional fields of type unknown.*

## Structure

`FeedbackErrorResponseError`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `success` | `boolean` | Required | - |
| `error` | `string` | Required | - |
| `feedbackErrorCode` | `string \| undefined` | Optional | - |
| `details` | `unknown[] \| undefined` | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
try {
  // make the API call
} catch (error) {
  if (error instanceof FeedbackErrorResponseError) {
    console.log(error.result);
  }
}
```

