
# Crawl Errors Response Obj

*This model accepts additional fields of type unknown.*

## Structure

`CrawlErrorsResponseObj`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `errors` | [`Error[] \| undefined`](../../doc/models/error.md) | Optional | Errored scrape jobs and error details |
| `robotsBlocked` | `string[] \| undefined` | Optional | List of URLs that were attempted in scraping but were blocked by robots.txt |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { CrawlErrorsResponseObj } from 'firecrawl-apilib';

const crawlErrorsResponseObj: CrawlErrorsResponseObj = {
  errors: [
    {
      id: 'id0',
      timestamp: 'timestamp8',
      url: 'url4',
      error: 'error4',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    }
  ],
  robotsBlocked: [
    'robotsBlocked6'
  ],
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

