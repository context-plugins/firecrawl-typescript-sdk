
# Javascript Return

*This model accepts additional fields of type unknown.*

## Structure

`JavascriptReturn`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `type` | `string \| undefined` | Optional | - |
| `value` | `unknown \| undefined` | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { JavascriptReturn } from 'firecrawl-apilib';

const javascriptReturn: JavascriptReturn = {
  type: 'type2',
  value: { 'key1': 'val1', 'key2': 'val2' },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

