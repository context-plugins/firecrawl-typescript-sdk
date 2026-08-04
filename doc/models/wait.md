
# Wait

*This model accepts additional fields of type unknown.*

## Structure

`Wait`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `type` | [`Type`](../../doc/models/type.md) | Required | Wait for a specified amount of milliseconds |
| `milliseconds` | `number \| undefined` | Optional | Number of milliseconds to wait<br><br>**Constraints**: `>= 1` |
| `selector` | `string \| undefined` | Optional | Query selector to find the element by |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { Type, Wait } from 'firecrawl-apilib';

const wait: Wait = {
  type: Type.Wait,
  milliseconds: 28,
  selector: '#my-element',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

