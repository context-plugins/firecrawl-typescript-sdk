
# Deep Research Response 1

*This model accepts additional fields of type unknown.*

## Structure

`DeepResearchResponse1`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `success` | `boolean \| undefined` | Optional | - |
| `data` | [`Data3 \| undefined`](../../doc/models/data-3.md) | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { DeepResearchResponse1, Status2 } from 'firecrawl-apilib';

const deepResearchResponse1: DeepResearchResponse1 = {
  success: false,
  data: {
    finalAnalysis: 'finalAnalysis2',
    json: { 'key1': 'val1', 'key2': 'val2' },
    activities: [
      {
        type: 'type8',
        status: 'status4',
        message: 'message2',
        timestamp: '2016-03-13T12:52:32.123Z',
        depth: 100,
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      {
        type: 'type8',
        status: 'status4',
        message: 'message2',
        timestamp: '2016-03-13T12:52:32.123Z',
        depth: 100,
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      {
        type: 'type8',
        status: 'status4',
        message: 'message2',
        timestamp: '2016-03-13T12:52:32.123Z',
        depth: 100,
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      }
    ],
    sources: [
      {
        url: 'url0',
        title: 'title2',
        description: 'description6',
        favicon: 'favicon6',
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      }
    ],
    status: Status2.Failed,
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

