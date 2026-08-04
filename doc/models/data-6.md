
# Data 6

*This model accepts additional fields of type unknown.*

## Structure

`Data6`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `title` | `string \| undefined` | Optional | Title from search result |
| `description` | `string \| undefined` | Optional | Description from search result |
| `url` | `string \| undefined` | Optional | URL of the search result |
| `markdown` | `string \| null \| undefined` | Optional | Markdown content if scraping was requested |
| `html` | `string \| null \| undefined` | Optional | HTML content if requested in formats |
| `rawHtml` | `string \| null \| undefined` | Optional | Raw HTML content if requested in formats |
| `links` | `string[] \| undefined` | Optional | Links found if requested in formats |
| `screenshot` | `string \| null \| undefined` | Optional | Screenshot URL if requested in formats |
| `metadata` | [`Metadata3 \| undefined`](../../doc/models/metadata-3.md) | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { Data6 } from 'firecrawl-apilib';

const data6: Data6 = {
  title: 'title4',
  description: 'description8',
  url: 'url2',
  markdown: 'markdown6',
  html: 'html8',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

