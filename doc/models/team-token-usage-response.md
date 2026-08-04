
# Team Token Usage Response

*This model accepts additional fields of type unknown.*

## Structure

`TeamTokenUsageResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `success` | `boolean \| undefined` | Optional | - |
| `data` | [`Data5 \| undefined`](../../doc/models/data-5.md) | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { TeamTokenUsageResponse } from 'firecrawl-apilib';

const teamTokenUsageResponse: TeamTokenUsageResponse = {
  success: true,
  data: {
    remainingTokens: 60.32,
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

