
# Json Options

JSON options object

*This model accepts additional fields of type unknown.*

## Structure

`JsonOptions`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `schema` | `unknown \| undefined` | Optional | The schema to use for the extraction (Optional). Must conform to [JSON Schema](https://json-schema.org/). |
| `systemPrompt` | `string \| undefined` | Optional | The system prompt to use for the extraction (Optional) |
| `prompt` | `string \| undefined` | Optional | The prompt to use for the extraction without a schema (Optional) |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { JsonOptions } from 'firecrawl-apilib';

const jsonOptions: JsonOptions = {
  schema: { 'key1': 'val1', 'key2': 'val2' },
  systemPrompt: 'systemPrompt0',
  prompt: 'prompt6',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

