
# Actions

Results of the actions specified in the `actions` parameter. Only present if the `actions` parameter was provided in the request

*This model accepts additional fields of type unknown.*

## Structure

`Actions`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `screenshots` | `string[] \| undefined` | Optional | Screenshot URLs, in the same order as the screenshot actions provided. |
| `scrapes` | [`Scrape1[] \| undefined`](../../doc/models/scrape-1.md) | Optional | Scrape contents, in the same order as the scrape actions provided. |
| `javascriptReturns` | [`JavascriptReturn[] \| undefined`](../../doc/models/javascript-return.md) | Optional | JavaScript return values, in the same order as the executeJavascript actions provided. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { Actions } from 'firecrawl-apilib';

const actions: Actions = {
  screenshots: [
    'screenshots3',
    'screenshots4',
    'screenshots5'
  ],
  scrapes: [
    {
      url: 'url0',
      html: 'html6',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    }
  ],
  javascriptReturns: [
    {
      type: 'type4',
      value: { 'key1': 'val1', 'key2': 'val2' },
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    {
      type: 'type4',
      value: { 'key1': 'val1', 'key2': 'val2' },
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    }
  ],
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

