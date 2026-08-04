
# Scrape Request

*This model accepts additional fields of type unknown.*

## Structure

`ScrapeRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `url` | `string` | Required | The URL to scrape |
| `formats` | [`Format[] \| undefined`](../../doc/models/format.md) | Optional | Formats to include in the output. |
| `onlyMainContent` | `boolean \| undefined` | Optional | Only return the main content of the page excluding headers, navs, footers, etc.<br><br>**Default**: `true` |
| `includeTags` | `string[] \| undefined` | Optional | Tags to include in the output. |
| `excludeTags` | `string[] \| undefined` | Optional | Tags to exclude from the output. |
| `maxAge` | `number \| undefined` | Optional | Returns a cached version of the page if it is younger than this age in milliseconds. If a cached version of the page is older than this value, the page will be scraped. If you do not need extremely fresh data, enabling this can speed up your scrapes by 500%. Defaults to 0, which disables caching.<br><br>**Default**: `0` |
| `headers` | `unknown \| undefined` | Optional | Headers to send with the request. Can be used to send cookies, user-agent, etc. |
| `waitFor` | `number \| undefined` | Optional | Specify a delay in milliseconds before fetching the content, allowing the page sufficient time to load.<br><br>**Default**: `0` |
| `mobile` | `boolean \| undefined` | Optional | Set to true if you want to emulate scraping from a mobile device. Useful for testing responsive pages and taking mobile screenshots.<br><br>**Default**: `false` |
| `skipTlsVerification` | `boolean \| undefined` | Optional | Skip TLS certificate verification when making requests<br><br>**Default**: `false` |
| `timeout` | `number \| undefined` | Optional | Timeout in milliseconds for the request<br><br>**Default**: `30000` |
| `parsePdf` | `boolean \| undefined` | Optional | Controls how PDF files are processed during scraping. When true, the PDF content is extracted and converted to markdown format, with billing based on the number of pages (1 credit per page). When false, the PDF file is returned in base64 encoding with a flat rate of 1 credit total.<br><br>**Default**: `true` |
| `jsonOptions` | [`JsonOptions \| undefined`](../../doc/models/json-options.md) | Optional | JSON options object |
| `actions` | [`ScrapeRequestActions[] \| undefined`](../../doc/models/containers/scrape-request-actions.md) | Optional | This is Array of a container for one-of cases. |
| `location` | [`Location \| undefined`](../../doc/models/location.md) | Optional | Location settings for the request. When specified, this will use an appropriate proxy if available and emulate the corresponding language and timezone settings. Defaults to 'US' if not specified. |
| `removeBase64Images` | `boolean \| undefined` | Optional | Removes all base 64 images from the output, which may be overwhelmingly long. The image's alt text remains in the output, but the URL is replaced with a placeholder. |
| `blockAds` | `boolean \| undefined` | Optional | Enables ad-blocking and cookie popup blocking.<br><br>**Default**: `true` |
| `proxy` | [`Proxy \| undefined`](../../doc/models/proxy.md) | Optional | Specifies the type of proxy to use.<br><br>- **basic**: Proxies for scraping sites with none to basic anti-bot solutions. Fast and usually works.<br>- **enhanced**: Enhanced proxies for scraping sites with advanced anti-bot solutions. Slower, but more reliable on certain sites. Costs up to 5 credits per request.<br>- **auto**: Firecrawl will automatically retry scraping with enhanced proxies if the basic proxy fails. If the retry with enhanced is successful, 5 credits will be billed for the scrape. If the first attempt with basic is successful, only the regular cost will be billed.<br><br>If you do not specify a proxy, Firecrawl will default to basic. |
| `changeTrackingOptions` | [`ChangeTrackingOptions \| undefined`](../../doc/models/change-tracking-options.md) | Optional | Options for change tracking (Beta). Only applicable when 'changeTracking' is included in formats. The 'markdown' format must also be specified when using change tracking. |
| `storeInCache` | `boolean \| undefined` | Optional | If true, the page will be stored in the Firecrawl index and cache. Setting this to false is useful if your scraping activity may have data protection concerns. Using some parameters associated with sensitive scraping (actions, headers) will force this parameter to be false.<br><br>**Default**: `true` |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { Format, ScrapeRequest } from 'firecrawl-apilib';

const scrapeRequest: ScrapeRequest = {
  url: 'url2',
  formats: [
    Format.Markdown,
    Format.Branding
  ],
  onlyMainContent: true,
  includeTags: [
    'includeTags3'
  ],
  excludeTags: [
    'excludeTags2'
  ],
  maxAge: 0,
  waitFor: 0,
  mobile: false,
  skipTlsVerification: false,
  timeout: 30000,
  parsePdf: true,
  blockAds: true,
  storeInCache: true,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

