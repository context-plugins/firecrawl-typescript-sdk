
# Map Request

*This model accepts additional fields of type unknown.*

## Structure

`MapRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `url` | `string` | Required | The base URL to start crawling from |
| `search` | `string \| undefined` | Optional | Search query to use for mapping. During the Alpha phase, the 'smart' part of the search functionality is limited to 1000 search results. However, if map finds more results, there is no limit applied. |
| `ignoreSitemap` | `boolean \| undefined` | Optional | Ignore the website sitemap when crawling.<br><br>**Default**: `true` |
| `sitemapOnly` | `boolean \| undefined` | Optional | Only return links found in the website sitemap<br><br>**Default**: `false` |
| `includeSubdomains` | `boolean \| undefined` | Optional | Include subdomains of the website<br><br>**Default**: `true` |
| `limit` | `number \| undefined` | Optional | Maximum number of links to return<br><br>**Default**: `5000`<br><br>**Constraints**: `<= 30000` |
| `timeout` | `number \| undefined` | Optional | Timeout in milliseconds. There is no timeout by default. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { MapRequest } from 'firecrawl-apilib';

const mapRequest: MapRequest = {
  url: 'url8',
  search: 'search2',
  ignoreSitemap: true,
  sitemapOnly: false,
  includeSubdomains: true,
  limit: 5000,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

