
# Data 4

*This model accepts additional fields of type unknown.*

## Structure

`Data4`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `remainingCredits` | `number \| undefined` | Optional | Number of credits remaining for the team |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { Data4 } from 'firecrawl-apilib';

const data4: Data4 = {
  remainingCredits: 1000,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

