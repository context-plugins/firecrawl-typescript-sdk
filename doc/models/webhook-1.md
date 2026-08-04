
# Webhook 1

A webhook specification object.

*This model accepts additional fields of type unknown.*

## Structure

`Webhook1`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `url` | `string` | Required | The URL to send the webhook to. This will trigger for crawl started (crawl.started), every page crawled (crawl.page) and when the crawl is completed (crawl.completed or crawl.failed). The response will be the same as the `/scrape` endpoint. |
| `headers` | `Record<string, string> \| undefined` | Optional | Headers to send to the webhook URL. |
| `metadata` | `unknown \| undefined` | Optional | Custom metadata that will be included in all webhook payloads for this crawl |
| `events` | [`Event[] \| undefined`](../../doc/models/event.md) | Optional | Type of events that should be sent to the webhook URL. (default: all) |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { Event, Webhook1 } from 'firecrawl-apilib';

const webhook1: Webhook1 = {
  url: 'url2',
  headers: {
    'key0': 'headers1'
  },
  metadata: { 'key1': 'val1', 'key2': 'val2' },
  events: [
    Event.Completed,
    Event.Page
  ],
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

