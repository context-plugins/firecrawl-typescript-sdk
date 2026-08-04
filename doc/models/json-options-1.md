
# Json Options 1

Options for JSON output

*This model accepts additional fields of type unknown.*

## Structure

`JsonOptions1`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `schema` | `unknown \| undefined` | Optional | The schema to use for the JSON output. Must conform to [JSON Schema](https://json-schema.org/). |
| `systemPrompt` | `string \| undefined` | Optional | The system prompt to use for the JSON output |
| `prompt` | `string \| undefined` | Optional | The prompt to use for the JSON output |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { JsonOptions1 } from 'firecrawl-apilib';

const jsonOptions1: JsonOptions1 = {
  schema: { 'key1': 'val1', 'key2': 'val2' },
  systemPrompt: 'systemPrompt4',
  prompt: 'prompt0',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

