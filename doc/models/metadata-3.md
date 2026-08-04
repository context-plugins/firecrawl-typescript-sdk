
# Metadata 3

*This model accepts additional fields of type unknown.*

## Structure

`Metadata3`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `title` | `string \| undefined` | Optional | - |
| `description` | `string \| undefined` | Optional | - |
| `sourceUrl` | `string \| undefined` | Optional | - |
| `statusCode` | `number \| undefined` | Optional | - |
| `error` | `string \| null \| undefined` | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { Metadata3 } from 'firecrawl-apilib';

const metadata3: Metadata3 = {
  title: 'title2',
  description: 'description6',
  sourceUrl: 'sourceURL8',
  statusCode: 38,
  error: 'error0',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

