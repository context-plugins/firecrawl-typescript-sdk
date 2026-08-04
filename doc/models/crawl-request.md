
# Crawl Request

*This model accepts additional fields of type unknown.*

## Structure

`CrawlRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `url` | `string` | Required | The base URL to start crawling from |
| `excludePaths` | `string[] \| undefined` | Optional | URL pathname regex patterns that exclude matching URLs from the crawl. For example, if you set "excludePaths": ["blog/.*"] for the base URL firecrawl.dev, any results matching that pattern will be excluded, such as https://www.firecrawl.dev/blog/firecrawl-launch-week-1-recap. |
| `includePaths` | `string[] \| undefined` | Optional | URL pathname regex patterns that include matching URLs in the crawl. Only the paths that match the specified patterns will be included in the response. For example, if you set "includePaths": ["blog/.*"] for the base URL firecrawl.dev, only results matching that pattern will be included, such as https://www.firecrawl.dev/blog/firecrawl-launch-week-1-recap. |
| `maxDepth` | `number \| undefined` | Optional | Maximum depth to crawl relative to the base URL. Basically, the max number of slashes the pathname of a scraped URL may contain.<br><br>**Default**: `10` |
| `maxDiscoveryDepth` | `number \| undefined` | Optional | Maximum depth to crawl based on discovery order. The root site and sitemapped pages has a discovery depth of 0. For example, if you set it to 1, and you set ignoreSitemap, you will only crawl the entered URL and all URLs that are linked on that page. |
| `ignoreSitemap` | `boolean \| undefined` | Optional | Ignore the website sitemap when crawling<br><br>**Default**: `false` |
| `ignoreQueryParameters` | `boolean \| undefined` | Optional | Do not re-scrape the same path with different (or none) query parameters<br><br>**Default**: `false` |
| `limit` | `number \| undefined` | Optional | Maximum number of pages to crawl. Default limit is 10000.<br><br>**Default**: `10000` |
| `allowBackwardLinks` | `boolean \| undefined` | Optional | Allows the crawler to follow internal links to sibling or parent URLs, not just child paths.<br><br>false: Only crawls deeper (child) URLs.<br>→ e.g. /features/feature-1 → /features/feature-1/tips ✅<br>→ Won't follow /pricing or / ❌<br><br>true: Crawls any internal links, including siblings and parents.<br>→ e.g. /features/feature-1 → /pricing, /, etc. ✅<br><br>Use true for broader internal coverage beyond nested paths.<br><br>**Default**: `false` |
| `allowExternalLinks` | `boolean \| undefined` | Optional | Allows the crawler to follow links to external websites.<br><br>**Default**: `false` |
| `delay` | `number \| undefined` | Optional | Delay in seconds between scrapes. This helps respect website rate limits. |
| `webhook` | [`Webhook1 \| undefined`](../../doc/models/webhook-1.md) | Optional | A webhook specification object. |
| `scrapeOptions` | [`ScrapeOptions \| undefined`](../../doc/models/scrape-options.md) | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { CrawlRequest } from 'firecrawl-apilib';

const crawlRequest: CrawlRequest = {
  url: 'url4',
  excludePaths: [
    'excludePaths5',
    'excludePaths6'
  ],
  includePaths: [
    'includePaths8'
  ],
  maxDepth: 10,
  maxDiscoveryDepth: 2,
  ignoreSitemap: false,
  ignoreQueryParameters: false,
  limit: 10000,
  allowBackwardLinks: false,
  allowExternalLinks: false,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

