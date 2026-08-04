
# Scrape Options 1

Options for scraping search results

*This model accepts additional fields of type unknown.*

## Structure

`ScrapeOptions1`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `formats` | [`Format2[] \| undefined`](../../doc/models/format-2.md) | Optional | Formats to include in the output |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { Format2, ScrapeOptions1 } from 'firecrawl-apilib';

const scrapeOptions1: ScrapeOptions1 = {
  formats: [
    Format2.Html,
    Format2.RawHtml,
    Format2.Links
  ],
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

