
# Team Credit Usage Response

*This model accepts additional fields of type unknown.*

## Structure

`TeamCreditUsageResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `success` | `boolean \| undefined` | Optional | - |
| `data` | [`Data4 \| undefined`](../../doc/models/data-4.md) | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { TeamCreditUsageResponse } from 'firecrawl-apilib';

const teamCreditUsageResponse: TeamCreditUsageResponse = {
  success: true,
  data: {
    remainingCredits: 22.72,
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

