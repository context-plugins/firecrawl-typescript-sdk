
# Batch Scrape Response Obj

*This model accepts additional fields of type unknown.*

## Structure

`BatchScrapeResponseObj`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `success` | `boolean \| undefined` | Optional | - |
| `id` | `string \| undefined` | Optional | - |
| `url` | `string \| undefined` | Optional | - |
| `invalidUrLs` | `string[] \| null \| undefined` | Optional | If ignoreInvalidURLs is true, this is an array containing the invalid URLs that were specified in the request. If there were no invalid URLs, this will be an empty array. If ignoreInvalidURLs is false, this field will be undefined. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { BatchScrapeResponseObj } from 'firecrawl-apilib';

const batchScrapeResponseObj: BatchScrapeResponseObj = {
  success: false,
  id: 'id4',
  url: 'url8',
  invalidUrLs: [
    'invalidURLs6',
    'invalidURLs7',
    'invalidURLs8'
  ],
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

