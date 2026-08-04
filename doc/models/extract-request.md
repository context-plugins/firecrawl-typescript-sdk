
# Extract Request

*This model accepts additional fields of type unknown.*

## Structure

`ExtractRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `urls` | `string[]` | Required | - |
| `prompt` | `string \| undefined` | Optional | Prompt to guide the extraction process |
| `schema` | `unknown \| undefined` | Optional | Schema to define the structure of the extracted data. Must conform to [JSON Schema](https://json-schema.org/). |
| `enableWebSearch` | `boolean \| undefined` | Optional | When true, the extraction will use web search to find additional data<br><br>**Default**: `false` |
| `ignoreSitemap` | `boolean \| undefined` | Optional | When true, sitemap.xml files will be ignored during website scanning<br><br>**Default**: `false` |
| `includeSubdomains` | `boolean \| undefined` | Optional | When true, subdomains of the provided URLs will also be scanned<br><br>**Default**: `true` |
| `showSources` | `boolean \| undefined` | Optional | When true, the sources used to extract the data will be included in the response as `sources` key<br><br>**Default**: `false` |
| `scrapeOptions` | [`ScrapeOptions \| undefined`](../../doc/models/scrape-options.md) | Optional | - |
| `ignoreInvalidUrLs` | `boolean \| undefined` | Optional | If invalid URLs are specified in the urls array, they will be ignored. Instead of them failing the entire request, an extract using the remaining valid URLs will be performed, and the invalid URLs will be returned in the invalidURLs field of the response.<br><br>**Default**: `false` |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { ExtractRequest } from 'firecrawl-apilib';

const extractRequest: ExtractRequest = {
  urls: [
    'urls5',
    'urls4'
  ],
  prompt: 'prompt4',
  schema: { 'key1': 'val1', 'key2': 'val2' },
  enableWebSearch: false,
  ignoreSitemap: false,
  includeSubdomains: true,
  showSources: false,
  ignoreInvalidUrLs: false,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

