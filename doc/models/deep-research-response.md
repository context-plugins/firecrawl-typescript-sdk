
# Deep Research Response

*This model accepts additional fields of type unknown.*

## Structure

`DeepResearchResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `success` | `boolean \| undefined` | Optional | - |
| `id` | `string \| undefined` | Optional | ID of the research job |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { DeepResearchResponse } from 'firecrawl-apilib';

const deepResearchResponse: DeepResearchResponse = {
  success: true,
  id: '00000e70-0000-0000-0000-000000000000',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

