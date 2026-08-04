
# Data

*This model accepts additional fields of type unknown.*

## Structure

`Data`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `markdown` | `string \| undefined` | Optional | - |
| `html` | `string \| null \| undefined` | Optional | HTML version of the content on page if `html` is in `formats` |
| `rawHtml` | `string \| null \| undefined` | Optional | Raw HTML content of the page if `rawHtml` is in `formats` |
| `screenshot` | `string \| null \| undefined` | Optional | Screenshot of the page if `screenshot` is in `formats` |
| `links` | `string[] \| undefined` | Optional | List of links on the page if `links` is in `formats` |
| `actions` | [`Actions \| null \| undefined`](../../doc/models/actions.md) | Optional | Results of the actions specified in the `actions` parameter. Only present if the `actions` parameter was provided in the request |
| `metadata` | [`Metadata \| undefined`](../../doc/models/metadata.md) | Optional | - |
| `llmExtraction` | `unknown \| null \| undefined` | Optional | Displayed when using LLM Extraction. Extracted data from the page following the schema defined. |
| `warning` | `string \| null \| undefined` | Optional | Can be displayed when using LLM Extraction. Warning message will let you know any issues with the extraction. |
| `changeTracking` | [`ChangeTracking \| null \| undefined`](../../doc/models/change-tracking.md) | Optional | Change tracking information if `changeTracking` is in `formats`. Only present when the `changeTracking` format is requested. |
| `branding` | [`Branding \| null \| undefined`](../../doc/models/branding.md) | Optional | Brand identity information derived from executing on-page javascript. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { Data } from 'firecrawl-apilib';

const data: Data = {
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
};
```

