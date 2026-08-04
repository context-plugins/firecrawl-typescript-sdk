
# Search Request

*This model accepts additional fields of type unknown.*

## Structure

`SearchRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `query` | `string` | Required | The search query |
| `limit` | `number \| undefined` | Optional | Maximum number of results to return<br><br>**Default**: `5`<br><br>**Constraints**: `>= 1`, `<= 100` |
| `tbs` | `string \| undefined` | Optional | Time-based search parameter |
| `location` | `string \| undefined` | Optional | Location parameter for search results |
| `timeout` | `number \| undefined` | Optional | Timeout in milliseconds<br><br>**Default**: `60000` |
| `ignoreInvalidUrLs` | `boolean \| undefined` | Optional | Excludes URLs from the search results that are invalid for other Firecrawl endpoints. This helps reduce errors if you are piping data from search into other Firecrawl API endpoints.<br><br>**Default**: `false` |
| `scrapeOptions` | [`ScrapeOptions1 \| undefined`](../../doc/models/scrape-options-1.md) | Optional | Options for scraping search results |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { SearchRequest } from 'firecrawl-apilib';

const searchRequest: SearchRequest = {
  query: 'query8',
  limit: 5,
  tbs: 'tbs6',
  location: 'location2',
  timeout: 60000,
  ignoreInvalidUrLs: false,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

