
# Data 3

*This model accepts additional fields of type unknown.*

## Structure

`Data3`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `finalAnalysis` | `string \| undefined` | Optional | - |
| `json` | `unknown \| null \| undefined` | Optional | Displayed when using JSON format |
| `activities` | [`Activity[] \| undefined`](../../doc/models/activity.md) | Optional | - |
| `sources` | [`Source[] \| undefined`](../../doc/models/source.md) | Optional | - |
| `status` | [`Status2 \| undefined`](../../doc/models/status-2.md) | Optional | - |
| `error` | `string \| undefined` | Optional | - |
| `expiresAt` | `string \| undefined` | Optional | - |
| `currentDepth` | `number \| undefined` | Optional | - |
| `maxDepth` | `number \| undefined` | Optional | - |
| `totalUrls` | `number \| undefined` | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { Data3, Status2 } from 'firecrawl-apilib';

const data3: Data3 = {
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
    },
    {
      url: 'url0',
      title: 'title2',
      description: 'description6',
      favicon: 'favicon6',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
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
  status: Status2.Processing,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

