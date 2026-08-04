
# Write Text

*This model accepts additional fields of type unknown.*

## Structure

`WriteText`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `type` | [`Type3`](../../doc/models/type-3.md) | Required | Write text into an input field, text area, or contenteditable element. Note: You must first focus the element using a 'click' action before writing. The text will be typed character by character to simulate keyboard input. |
| `text` | `string` | Required | Text to type |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { Type3, WriteText } from 'firecrawl-apilib';

const writeText: WriteText = {
  type: Type3.Write,
  text: 'Hello, world!',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

