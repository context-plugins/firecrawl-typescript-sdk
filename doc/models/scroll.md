
# Scroll

*This model accepts additional fields of type unknown.*

## Structure

`Scroll`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `type` | [`Type5`](../../doc/models/type-5.md) | Required | Scroll the page or a specific element |
| `direction` | [`Direction \| undefined`](../../doc/models/direction.md) | Optional | Direction to scroll<br><br>**Default**: `Direction.Down` |
| `selector` | `string \| undefined` | Optional | Query selector for the element to scroll |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { Direction, Scroll, Type5 } from 'firecrawl-apilib';

const scroll: Scroll = {
  type: Type5.Scroll,
  direction: Direction.Down,
  selector: '#my-element',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

