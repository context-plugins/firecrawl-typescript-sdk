
# Batch Scrape Status Response Obj

*This model accepts additional fields of type unknown.*

## Structure

`BatchScrapeStatusResponseObj`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `status` | `string \| undefined` | Optional | The current status of the batch scrape. Can be `scraping`, `completed`, or `failed`. |
| `total` | `number \| undefined` | Optional | The total number of pages that were attempted to be scraped. |
| `completed` | `number \| undefined` | Optional | The number of pages that have been successfully scraped. |
| `creditsUsed` | `number \| undefined` | Optional | The number of credits used for the batch scrape. |
| `expiresAt` | `string \| undefined` | Optional | The date and time when the batch scrape will expire. |
| `next` | `string \| null \| undefined` | Optional | The URL to retrieve the next 10MB of data. Returned if the batch scrape is not completed or if the response is larger than 10MB. |
| `data` | [`Data1[] \| undefined`](../../doc/models/data-1.md) | Optional | The data of the batch scrape. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { BatchScrapeStatusResponseObj } from 'firecrawl-apilib';

const batchScrapeStatusResponseObj: BatchScrapeStatusResponseObj = {
  status: 'status4',
  total: 90,
  completed: 252,
  creditsUsed: 180,
  expiresAt: '2016-03-13T12:52:32.123Z',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

