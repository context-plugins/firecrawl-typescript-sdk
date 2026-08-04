
# Extract Status Response

*This model accepts additional fields of type unknown.*

## Structure

`ExtractStatusResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `success` | `boolean \| undefined` | Optional | - |
| `data` | `unknown \| undefined` | Optional | - |
| `status` | [`Status \| undefined`](../../doc/models/status.md) | Optional | The current status of the extract job |
| `expiresAt` | `string \| undefined` | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { ExtractStatusResponse, Status } from 'firecrawl-apilib';

const extractStatusResponse: ExtractStatusResponse = {
  success: false,
  data: { 'key1': 'val1', 'key2': 'val2' },
  status: Status.Completed,
  expiresAt: '2016-03-13T12:52:32.123Z',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

