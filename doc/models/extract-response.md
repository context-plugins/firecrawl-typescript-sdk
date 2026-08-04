
# Extract Response

*This model accepts additional fields of type unknown.*

## Structure

`ExtractResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `success` | `boolean \| undefined` | Optional | - |
| `id` | `string \| undefined` | Optional | - |
| `invalidUrLs` | `string[] \| null \| undefined` | Optional | If ignoreInvalidURLs is true, this is an array containing the invalid URLs that were specified in the request. If there were no invalid URLs, this will be an empty array. If ignoreInvalidURLs is false, this field will be undefined. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { ExtractResponse } from 'firecrawl-apilib';

const extractResponse: ExtractResponse = {
  success: false,
  id: 'id0',
  invalidUrLs: [
    'invalidURLs2',
    'invalidURLs3',
    'invalidURLs4'
  ],
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

