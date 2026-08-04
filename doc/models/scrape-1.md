
# Scrape 1

*This model accepts additional fields of type unknown.*

## Structure

`Scrape1`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `url` | `string \| undefined` | Optional | - |
| `html` | `string \| undefined` | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { Scrape1 } from 'firecrawl-apilib';

const scrape1: Scrape1 = {
  url: 'url4',
  html: 'html0',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

