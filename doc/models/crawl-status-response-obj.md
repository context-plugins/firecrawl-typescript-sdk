
# Crawl Status Response Obj

*This model accepts additional fields of type unknown.*

## Structure

`CrawlStatusResponseObj`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `status` | `string \| undefined` | Optional | The current status of the crawl. Can be `scraping`, `completed`, or `failed`. |
| `total` | `number \| undefined` | Optional | The total number of pages that were attempted to be crawled. |
| `completed` | `number \| undefined` | Optional | The number of pages that have been successfully crawled. |
| `creditsUsed` | `number \| undefined` | Optional | The number of credits used for the crawl. |
| `expiresAt` | `string \| undefined` | Optional | The date and time when the crawl will expire. |
| `createdAt` | `string \| undefined` | Optional | The date and time when the crawl was started. |
| `completedAt` | `string \| undefined` | Optional | The date and time when the crawl finished. Present only when the crawl is in a terminal state (`completed`, `failed`, or `cancelled`). |
| `duration` | `number \| undefined` | Optional | Crawl duration in seconds. For terminal crawls, this is the elapsed time from `createdAt` to `completedAt`. For in-progress crawls, it is the elapsed time from `createdAt` to now. |
| `next` | `string \| null \| undefined` | Optional | The URL to retrieve the next 10MB of data. Returned if the crawl is not completed or if the response is larger than 10MB. |
| `data` | [`Data1[] \| undefined`](../../doc/models/data-1.md) | Optional | The data of the crawl. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { CrawlStatusResponseObj } from 'firecrawl-apilib';

const crawlStatusResponseObj: CrawlStatusResponseObj = {
  status: 'status6',
  total: 156,
  completed: 6,
  creditsUsed: 190,
  expiresAt: '2016-03-13T12:52:32.123Z',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

