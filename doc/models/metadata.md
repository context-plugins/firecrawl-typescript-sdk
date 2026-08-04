
# Metadata

*This model accepts additional fields of type unknown.*

## Structure

`Metadata`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `title` | `string \| undefined` | Optional | - |
| `description` | `string \| undefined` | Optional | - |
| `language` | `string \| null \| undefined` | Optional | - |
| `sourceUrl` | `string \| undefined` | Optional | - |
| `mAnyOtherMetadata` | `string \| undefined` | Optional | - |
| `statusCode` | `number \| undefined` | Optional | The status code of the page |
| `timezone` | `string \| undefined` | Optional | Timezone inferred by the scraping engine, when available |
| `error` | `string \| null \| undefined` | Optional | The error message of the page |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { Metadata } from 'firecrawl-apilib';

const metadata: Metadata = {
  title: 'title2',
  description: 'description6',
  language: 'language8',
  sourceUrl: 'sourceURL8',
  mAnyOtherMetadata: '<any other metadata>4',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

