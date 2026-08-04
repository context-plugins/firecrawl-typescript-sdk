
# Data 7

*This model accepts additional fields of type unknown.*

## Structure

`Data7`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `llmstxt` | `string \| undefined` | Optional | The generated LLMs.txt content |
| `llmsfulltxt` | `string \| undefined` | Optional | The full text content when showFullText is true |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { Data7 } from 'firecrawl-apilib';

const data7: Data7 = {
  llmstxt: 'llmstxt4',
  llmsfulltxt: 'llmsfulltxt0',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

