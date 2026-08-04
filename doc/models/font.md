
# Font

*This model accepts additional fields of type unknown.*

## Structure

`Font`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `family` | `string \| undefined` | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { Font } from 'firecrawl-apilib';

const font: Font = {
  family: 'family8',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

