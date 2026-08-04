
# Search Response

*This model accepts additional fields of type unknown.*

## Structure

`SearchResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `success` | `boolean \| undefined` | Optional | - |
| `data` | [`Data6[] \| undefined`](../../doc/models/data-6.md) | Optional | - |
| `warning` | `string \| null \| undefined` | Optional | Warning message if any issues occurred |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { SearchResponse } from 'firecrawl-apilib';

const searchResponse: SearchResponse = {
  success: false,
  data: [
    {
      title: 'title6',
      description: 'description0',
      url: 'url4',
      markdown: 'markdown8',
      html: 'html0',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    {
      title: 'title6',
      description: 'description0',
      url: 'url4',
      markdown: 'markdown8',
      html: 'html0',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    }
  ],
  warning: 'warning8',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

