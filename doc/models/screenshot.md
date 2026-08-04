
# Screenshot

*This model accepts additional fields of type unknown.*

## Structure

`Screenshot`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `type` | [`Type1`](../../doc/models/type-1.md) | Required | Take a screenshot. The links will be in the response's `actions.screenshots` array. |
| `fullPage` | `boolean \| undefined` | Optional | Should the screenshot be full-page or viewport sized?<br><br>**Default**: `false` |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { Screenshot, Type1 } from 'firecrawl-apilib';

const screenshot: Screenshot = {
  type: Type1.Screenshot,
  fullPage: false,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

