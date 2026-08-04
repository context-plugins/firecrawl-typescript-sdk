
# Click

*This model accepts additional fields of type unknown.*

## Structure

`Click`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `type` | [`Type2`](../../doc/models/type-2.md) | Required | Click on an element |
| `selector` | `string` | Required | Query selector to find the element by |
| `all` | `boolean \| undefined` | Optional | Clicks all elements matched by the selector, not just the first one. Does not throw an error if no elements match the selector.<br><br>**Default**: `false` |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { Click, Type2 } from 'firecrawl-apilib';

const click: Click = {
  type: Type2.Click,
  selector: '#load-more-button',
  all: false,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

