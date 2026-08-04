
# Crawl

*This model accepts additional fields of type unknown.*

## Structure

`Crawl`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `string` | Required | The unique identifier of the crawl |
| `teamId` | `string` | Required | The ID of the team that owns the crawl |
| `url` | `string` | Required | The origin URL of the crawl |
| `options` | [`Options`](../../doc/models/options.md) | Required | The crawler options used for this crawl |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { Crawl, Format } from 'firecrawl-apilib';

const crawl: Crawl = {
  id: '00001330-0000-0000-0000-000000000000',
  teamId: 'teamId4',
  url: 'url6',
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
};
```

