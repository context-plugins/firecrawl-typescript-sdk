
# Llmstxt Request

*This model accepts additional fields of type unknown.*

## Structure

`LlmstxtRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `url` | `string` | Required | The URL to generate LLMs.txt from |
| `maxUrls` | `number \| undefined` | Optional | Maximum number of URLs to analyze<br><br>**Default**: `2` |
| `showFullText` | `boolean \| undefined` | Optional | Include full text content in the response<br><br>**Default**: `false` |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { LlmstxtRequest } from 'firecrawl-apilib';

const llmstxtRequest: LlmstxtRequest = {
  url: 'url8',
  maxUrls: 2,
  showFullText: false,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

