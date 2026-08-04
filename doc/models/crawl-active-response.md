
# Crawl Active Response

*This model accepts additional fields of type unknown.*

## Structure

`CrawlActiveResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `success` | `boolean` | Required | - |
| `crawls` | [`Crawl[] \| undefined`](../../doc/models/crawl.md) | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { CrawlActiveResponse, Format } from 'firecrawl-apilib';

const crawlActiveResponse: CrawlActiveResponse = {
  success: true,
  crawls: [
    {
      id: '0000212e-0000-0000-0000-000000000000',
      teamId: 'teamId6',
      url: 'url8',
      options: {
        scrapeOptions: {
          formats: [
            Format.Html,
            Format.RawHtml,
            Format.Links
          ],
          onlyMainContent: false,
          includeTags: [
            'includeTags1',
            'includeTags0',
            'includeTags9'
          ],
          excludeTags: [
            'excludeTags0',
            'excludeTags1'
          ],
          maxAge: 190,
          additionalProperties: {
            'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
          },
        },
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    {
      id: '0000212e-0000-0000-0000-000000000000',
      teamId: 'teamId6',
      url: 'url8',
      options: {
        scrapeOptions: {
          formats: [
            Format.Html,
            Format.RawHtml,
            Format.Links
          ],
          onlyMainContent: false,
          includeTags: [
            'includeTags1',
            'includeTags0',
            'includeTags9'
          ],
          excludeTags: [
            'excludeTags0',
            'excludeTags1'
          ],
          maxAge: 190,
          additionalProperties: {
            'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
          },
        },
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    }
  ],
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

