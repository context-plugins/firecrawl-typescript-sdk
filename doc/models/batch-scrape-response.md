
# Batch Scrape Response

*This model accepts additional fields of type unknown.*

## Structure

`BatchScrapeResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `success` | `boolean \| undefined` | Optional | - |
| `message` | `string \| undefined` | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { BatchScrapeResponse } from 'firecrawl-apilib';

const batchScrapeResponse: BatchScrapeResponse = {
  success: true,
  message: 'Batch scrape job successfully cancelled.',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

