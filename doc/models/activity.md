
# Activity

*This model accepts additional fields of type unknown.*

## Structure

`Activity`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `type` | `string \| undefined` | Optional | - |
| `status` | `string \| undefined` | Optional | - |
| `message` | `string \| undefined` | Optional | - |
| `timestamp` | `string \| undefined` | Optional | - |
| `depth` | `number \| undefined` | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { Activity } from 'firecrawl-apilib';

const activity: Activity = {
  type: 'type2',
  status: 'status0',
  message: 'message8',
  timestamp: '2016-03-13T12:52:32.123Z',
  depth: 174,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

