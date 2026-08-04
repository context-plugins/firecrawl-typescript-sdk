
# Deep Research Request

*This model accepts additional fields of type unknown.*

## Structure

`DeepResearchRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `query` | `string` | Required | The query to research |
| `maxDepth` | `number \| undefined` | Optional | Maximum depth of research iterations<br><br>**Default**: `7`<br><br>**Constraints**: `>= 1`, `<= 12` |
| `timeLimit` | `number \| undefined` | Optional | Time limit in seconds<br><br>**Default**: `300`<br><br>**Constraints**: `>= 30`, `<= 600` |
| `maxUrls` | `number \| undefined` | Optional | Maximum number of URLs to analyze<br><br>**Default**: `20`<br><br>**Constraints**: `>= 1`, `<= 1000` |
| `analysisPrompt` | `string \| undefined` | Optional | The prompt to use for the final analysis. Useful to format the final analysis markdown in a specific way. |
| `systemPrompt` | `string \| undefined` | Optional | The system prompt to use for the research agent. Useful to steer the research agent to a specific direction. |
| `formats` | [`Format1[] \| undefined`](../../doc/models/format-1.md) | Optional | - |
| `jsonOptions` | [`JsonOptions1 \| undefined`](../../doc/models/json-options-1.md) | Optional | Options for JSON output |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { DeepResearchRequest } from 'firecrawl-apilib';

const deepResearchRequest: DeepResearchRequest = {
  query: 'query4',
  maxDepth: 7,
  timeLimit: 300,
  maxUrls: 20,
  analysisPrompt: 'analysisPrompt2',
  systemPrompt: 'systemPrompt8',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

