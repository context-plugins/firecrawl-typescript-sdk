
# Map Response

*This model accepts additional fields of type unknown.*

## Structure

`MapResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `success` | `boolean \| undefined` | Optional | - |
| `id` | `string \| undefined` | Optional | The map job id. Use this as jobId when submitting feedback. |
| `links` | `string[] \| undefined` | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { MapResponse } from 'firecrawl-apilib';

const mapResponse: MapResponse = {
  success: false,
  id: '00000d2e-0000-0000-0000-000000000000',
  links: [
    'links0',
    'links1'
  ],
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

