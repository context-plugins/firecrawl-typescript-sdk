
# Data 1

*This model accepts additional fields of type unknown.*

## Structure

`Data1`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `markdown` | `string \| undefined` | Optional | - |
| `html` | `string \| null \| undefined` | Optional | HTML version of the content on page if `includeHtml`  is true |
| `rawHtml` | `string \| null \| undefined` | Optional | Raw HTML content of the page if `includeRawHtml`  is true |
| `links` | `string[] \| undefined` | Optional | List of links on the page if `includeLinks` is true |
| `screenshot` | `string \| null \| undefined` | Optional | Screenshot of the page if `includeScreenshot` is true |
| `metadata` | [`Metadata \| undefined`](../../doc/models/metadata.md) | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { Data1 } from 'firecrawl-apilib';

const data1: Data1 = {
  markdown: 'markdown2',
  html: 'html4',
  rawHtml: 'rawHtml0',
  links: [
    'links0',
    'links1'
  ],
  screenshot: 'screenshot0',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

