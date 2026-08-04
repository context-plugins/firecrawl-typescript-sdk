
# Llmstxt Response 1

*This model accepts additional fields of type unknown.*

## Structure

`LlmstxtResponse1`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `success` | `boolean \| undefined` | Optional | - |
| `status` | [`Status2 \| undefined`](../../doc/models/status-2.md) | Optional | - |
| `data` | [`Data7 \| undefined`](../../doc/models/data-7.md) | Optional | - |
| `expiresAt` | `string \| undefined` | Optional | When the generated content will expire |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { LlmstxtResponse1, Status2 } from 'firecrawl-apilib';

const llmstxtResponse1: LlmstxtResponse1 = {
  success: false,
  status: Status2.Completed,
  data: {
    llmstxt: 'llmstxt2',
    llmsfulltxt: 'llmsfulltxt8',
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  expiresAt: '2016-03-13T12:52:32.123Z',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

