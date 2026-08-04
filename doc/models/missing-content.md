
# Missing Content

*This model accepts additional fields of type unknown.*

## Structure

`MissingContent`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `topic` | `string` | Required | **Constraints**: *Maximum Length*: `200` |
| `description` | `string \| undefined` | Optional | **Constraints**: *Maximum Length*: `2000` |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { MissingContent } from 'firecrawl-apilib';

const missingContent: MissingContent = {
  topic: 'topic6',
  description: 'description2',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

