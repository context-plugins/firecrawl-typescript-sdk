
# Crawl Response 1

*This model accepts additional fields of type unknown.*

## Structure

`CrawlResponse1`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `status` | [`Status1 \| undefined`](../../doc/models/status-1.md) | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { CrawlResponse1, Status1 } from 'firecrawl-apilib';

const crawlResponse1: CrawlResponse1 = {
  status: Status1.Cancelled,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

