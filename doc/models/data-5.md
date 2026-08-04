
# Data 5

*This model accepts additional fields of type unknown.*

## Structure

`Data5`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `remainingTokens` | `number \| undefined` | Optional | Number of tokens remaining for the team |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { Data5 } from 'firecrawl-apilib';

const data5: Data5 = {
  remainingTokens: 1000,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

