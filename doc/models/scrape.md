
# Scrape

*This model accepts additional fields of type unknown.*

## Structure

`Scrape`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `type` | [`Type6`](../../doc/models/type-6.md) | Required | Scrape the current page content, returns the url and the html. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { Scrape, Type6 } from 'firecrawl-apilib';

const scrape: Scrape = {
  type: Type6.Scrape,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

