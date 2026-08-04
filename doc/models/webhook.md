
# Webhook

A webhook specification object.

*This model accepts additional fields of type unknown.*

## Structure

`Webhook`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `url` | `string` | Required | The URL to send the webhook to. This will trigger for batch scrape started (batch_scrape.started), every page scraped (batch_scrape.page) and when the batch scrape is completed (batch_scrape.completed or batch_scrape.failed). The response will be the same as the `/scrape` endpoint. |
| `headers` | `Record<string, string> \| undefined` | Optional | Headers to send to the webhook URL. |
| `metadata` | `unknown \| undefined` | Optional | Custom metadata that will be included in all webhook payloads for this crawl |
| `events` | [`Event[] \| undefined`](../../doc/models/event.md) | Optional | Type of events that should be sent to the webhook URL. (default: all) |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { Event, Webhook } from 'firecrawl-apilib';

const webhook: Webhook = {
  url: 'url6',
  headers: {
    'key0': 'headers5',
    'key1': 'headers6'
  },
  metadata: { 'key1': 'val1', 'key2': 'val2' },
  events: [
    Event.Completed
  ],
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

