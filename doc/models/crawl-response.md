
# Crawl Response

*This model accepts additional fields of type unknown.*

## Structure

`CrawlResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `success` | `boolean \| undefined` | Optional | - |
| `id` | `string \| undefined` | Optional | - |
| `url` | `string \| undefined` | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { CrawlResponse } from 'firecrawl-apilib';

const crawlResponse: CrawlResponse = {
  success: false,
  id: 'id4',
  url: 'url8',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

