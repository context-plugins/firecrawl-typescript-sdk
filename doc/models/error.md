
# Error

*This model accepts additional fields of type unknown.*

## Structure

`Error`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `string \| undefined` | Optional | - |
| `timestamp` | `string \| null \| undefined` | Optional | ISO timestamp of failure |
| `url` | `string \| undefined` | Optional | Scraped URL |
| `error` | `string \| undefined` | Optional | Error message |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { Error } from 'firecrawl-apilib';

const error: Error = {
  id: 'id4',
  timestamp: 'timestamp2',
  url: 'url8',
  error: 'error8',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

