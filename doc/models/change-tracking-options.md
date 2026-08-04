
# Change Tracking Options

Options for change tracking (Beta). Only applicable when 'changeTracking' is included in formats. The 'markdown' format must also be specified when using change tracking.

*This model accepts additional fields of type unknown.*

## Structure

`ChangeTrackingOptions`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `modes` | [`Mode[] \| undefined`](../../doc/models/mode.md) | Optional | The mode to use for change tracking. 'git-diff' provides a detailed diff, and 'json' compares extracted JSON data. |
| `schema` | `unknown \| undefined` | Optional | Schema for JSON extraction when using 'json' mode. Defines the structure of data to extract and compare. Must conform to [JSON Schema](https://json-schema.org/). |
| `prompt` | `string \| undefined` | Optional | Prompt to use for change tracking when using 'json' mode. If not provided, the default prompt will be used. |
| `tag` | `string \| null \| undefined` | Optional | Tag to use for change tracking. Tags can separate change tracking history into separate "branches", where change tracking with a specific tagwill only compare to scrapes made in the same tag. If not provided, the default tag (null) will be used. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { ChangeTrackingOptions, Mode } from 'firecrawl-apilib';

const changeTrackingOptions: ChangeTrackingOptions = {
  modes: [
    Mode.Json,
    Mode.Gitdiff,
    Mode.Json
  ],
  schema: { 'key1': 'val1', 'key2': 'val2' },
  prompt: 'prompt4',
  tag: 'tag2',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

