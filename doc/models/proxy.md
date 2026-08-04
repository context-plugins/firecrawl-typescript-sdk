
# Proxy

Specifies the type of proxy to use.

- **basic**: Proxies for scraping sites with none to basic anti-bot solutions. Fast and usually works.
- **enhanced**: Enhanced proxies for scraping sites with advanced anti-bot solutions. Slower, but more reliable on certain sites. Costs up to 5 credits per request.
- **auto**: Firecrawl will automatically retry scraping with enhanced proxies if the basic proxy fails. If the retry with enhanced is successful, 5 credits will be billed for the scrape. If the first attempt with basic is successful, only the regular cost will be billed.

If you do not specify a proxy, Firecrawl will default to basic.

## Enumeration

`Proxy`

## Fields

| Name |
|  --- |
| `Basic` |
| `Enhanced` |
| `Auto` |

## Example

```ts
import { Proxy } from 'firecrawl-apilib';

const proxy = Proxy.Enhanced;
```

