
# Valuable Source

*This model accepts additional fields of type unknown.*

## Structure

`ValuableSource`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `url` | `string` | Required | - |
| `reason` | `string \| undefined` | Optional | **Constraints**: *Maximum Length*: `1000` |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { ValuableSource } from 'firecrawl-apilib';

const valuableSource: ValuableSource = {
  url: 'url8',
  reason: 'reason0',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

