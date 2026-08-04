
# Feedback Response

*This model accepts additional fields of type unknown.*

## Structure

`FeedbackResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `success` | `boolean` | Required | - |
| `feedbackId` | `string` | Required | - |
| `creditsRefunded` | `number` | Required | - |
| `alreadySubmitted` | `boolean \| undefined` | Optional | - |
| `dailyCapReached` | `boolean \| undefined` | Optional | - |
| `creditsRefundedToday` | `number \| undefined` | Optional | - |
| `dailyRefundCap` | `number \| undefined` | Optional | - |
| `warning` | `string \| undefined` | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { FeedbackResponse } from 'firecrawl-apilib';

const feedbackResponse: FeedbackResponse = {
  success: true,
  feedbackId: '00000b46-0000-0000-0000-000000000000',
  creditsRefunded: 35.38,
  alreadySubmitted: false,
  dailyCapReached: false,
  creditsRefundedToday: 152.72,
  dailyRefundCap: 99.36,
  warning: 'warning2',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

