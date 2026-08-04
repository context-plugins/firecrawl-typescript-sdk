
# Search Feedback Request

For 'good', include valuableSources. For 'partial', include valuableSources or missingContent. For 'bad', include missingContent or querySuggestions.

*This model accepts additional fields of type unknown.*

## Structure

`SearchFeedbackRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `rating` | [`Rating`](../../doc/models/rating.md) | Required | - |
| `valuableSources` | [`ValuableSource[] \| undefined`](../../doc/models/valuable-source.md) | Optional | **Constraints**: *Maximum Items*: `50` |
| `missingContent` | [`MissingContent[] \| undefined`](../../doc/models/missing-content.md) | Optional | **Constraints**: *Maximum Items*: `20` |
| `querySuggestions` | `string \| undefined` | Optional | **Constraints**: *Maximum Length*: `2000` |
| `origin` | `string \| undefined` | Optional | **Default**: `'api'` |
| `integration` | `string \| null \| undefined` | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { Rating, SearchFeedbackRequest } from 'firecrawl-apilib';

const searchFeedbackRequest: SearchFeedbackRequest = {
  rating: Rating.Bad,
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

