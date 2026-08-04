
# Press a Key

Press a key on the page. See https://asawicki.info/nosense/doc/devices/keyboard/key_codes.html for key codes.

*This model accepts additional fields of type unknown.*

## Structure

`PressAKey`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `type` | [`Type4`](../../doc/models/type-4.md) | Required | Press a key on the page |
| `key` | `string` | Required | Key to press |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { PressAKey, Type4 } from 'firecrawl-apilib';

const pressAKey: PressAKey = {
  type: Type4.Press,
  key: 'Enter',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

