
# Source

*This model accepts additional fields of type unknown.*

## Structure

`Source`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `url` | `string \| undefined` | Optional | - |
| `title` | `string \| undefined` | Optional | - |
| `description` | `string \| undefined` | Optional | - |
| `favicon` | `string \| undefined` | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { Source } from 'firecrawl-apilib';

const source: Source = {
  url: 'url8',
  title: 'title0',
  description: 'description4',
  favicon: 'favicon4',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

