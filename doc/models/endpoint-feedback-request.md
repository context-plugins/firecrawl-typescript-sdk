
# Endpoint Feedback Request

*This model accepts additional fields of type unknown.*

## Structure

`EndpointFeedbackRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `rating` | [`Rating`](../../doc/models/rating.md) | Required | - |
| `valuableSources` | [`ValuableSource[] \| undefined`](../../doc/models/valuable-source.md) | Optional | **Constraints**: *Maximum Items*: `50` |
| `missingContent` | [`MissingContent[] \| undefined`](../../doc/models/missing-content.md) | Optional | **Constraints**: *Maximum Items*: `20` |
| `querySuggestions` | `string \| undefined` | Optional | **Constraints**: *Maximum Length*: `2000` |
| `origin` | `string \| undefined` | Optional | **Default**: `'api'` |
| `integration` | `string \| null \| undefined` | Optional | - |
| `endpoint` | [`Endpoint`](../../doc/models/endpoint.md) | Required | - |
| `jobId` | `string` | Required | - |
| `issues` | `string[] \| undefined` | Optional | **Constraints**: *Maximum Items*: `20`, *Maximum Length*: `80`, *Pattern*: `^[a-z0-9][a-z0-9_-]*$` |
| `tags` | `string[] \| undefined` | Optional | **Constraints**: *Maximum Items*: `20`, *Maximum Length*: `80`, *Pattern*: `^[a-z0-9][a-z0-9_-]*$` |
| `note` | `string \| undefined` | Optional | **Constraints**: *Maximum Length*: `4000` |
| `url` | `string \| undefined` | Optional | - |
| `pageNumbers` | `number[] \| undefined` | Optional | **Constraints**: *Maximum Items*: `100`, `>= 1` |
| `metadata` | `unknown \| undefined` | Optional | Small endpoint-specific metadata object. Must be 8KB or smaller; do not include full endpoint results. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { Endpoint, EndpointFeedbackRequest, Rating } from 'firecrawl-apilib';

const endpointFeedbackRequest: EndpointFeedbackRequest = {
  rating: Rating.Bad,
  endpoint: Endpoint.Parse,
  jobId: '0000075e-0000-0000-0000-000000000000',
  valuableSources: [
    {
      url: 'url8',
      reason: 'reason0',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    }
  ],
  missingContent: [
    {
      topic: 'topic6',
      description: 'description2',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    {
      topic: 'topic6',
      description: 'description2',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    }
  ],
  querySuggestions: 'querySuggestions4',
  origin: 'api',
  integration: 'integration4',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

