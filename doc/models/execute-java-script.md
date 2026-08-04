
# Execute Java Script

*This model accepts additional fields of type unknown.*

## Structure

`ExecuteJavaScript`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `type` | [`Type7`](../../doc/models/type-7.md) | Required | Execute JavaScript code on the page |
| `script` | `string` | Required | JavaScript code to execute |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { ExecuteJavaScript, Type7 } from 'firecrawl-apilib';

const executeJavaScript: ExecuteJavaScript = {
  type: Type7.ExecuteJavascript,
  script: 'document.querySelector(\'.button\').click();',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

