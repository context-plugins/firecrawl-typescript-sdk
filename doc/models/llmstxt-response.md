
# Llmstxt Response

*This model accepts additional fields of type unknown.*

## Structure

`LlmstxtResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `success` | `boolean \| undefined` | Optional | - |
| `id` | `string \| undefined` | Optional | ID of the LLMs.txt generation job |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { LlmstxtResponse } from 'firecrawl-apilib';

const llmstxtResponse: LlmstxtResponse = {
  success: true,
  id: '00000c36-0000-0000-0000-000000000000',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

