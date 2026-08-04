
# Options

The crawler options used for this crawl

*This model accepts additional fields of type unknown.*

## Structure

`Options`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `scrapeOptions` | [`ScrapeOptions \| undefined`](../../doc/models/scrape-options.md) | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { Format, Options } from 'firecrawl-apilib';

const options: Options = {
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
};
```

