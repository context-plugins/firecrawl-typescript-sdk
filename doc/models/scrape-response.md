
# Scrape Response

*This model accepts additional fields of type unknown.*

## Structure

`ScrapeResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `success` | `boolean \| undefined` | Optional | - |
| `data` | [`Data \| undefined`](../../doc/models/data.md) | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { ScrapeResponse } from 'firecrawl-apilib';

const scrapeResponse: ScrapeResponse = {
  success: false,
  data: {
    markdown: 'markdown8',
    html: 'html0',
    rawHtml: 'rawHtml6',
    screenshot: 'screenshot6',
    links: [
      'links6'
    ],
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

