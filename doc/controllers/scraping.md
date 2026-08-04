# Scraping

```ts
const scrapingApi = new ScrapingApi(client);
```

## Class Name

`ScrapingApi`

## Methods

* [Scrape and Extract from Url](../../doc/controllers/scraping.md#scrape-and-extract-from-url)
* [Scrape and Extract from Urls](../../doc/controllers/scraping.md#scrape-and-extract-from-urls)
* [Get Batch Scrape Status](../../doc/controllers/scraping.md#get-batch-scrape-status)
* [Cancel Batch Scrape](../../doc/controllers/scraping.md#cancel-batch-scrape)
* [Get Batch Scrape Errors](../../doc/controllers/scraping.md#get-batch-scrape-errors)


# Scrape and Extract from Url

```ts
async scrapeAndExtractFromUrl(
  body: ScrapeRequest,
  requestOptions?: RequestOptions
): Promise<ApiResponse<ScrapeResponse>>
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`ScrapeRequest`](../../doc/models/scrape-request.md) | Body, Required | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

**200**: Successful response

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`ScrapeResponse`](../../doc/models/scrape-response.md).

## Example Usage

```ts
const body: ScrapeRequest = {
  url: 'url0',
  onlyMainContent: true,
  maxAge: 0,
  waitFor: 0,
  mobile: false,
  skipTlsVerification: false,
  timeout: 30000,
  parsePdf: true,
  blockAds: true,
  storeInCache: true,
};

try {
  const response = await scrapingApi.scrapeAndExtractFromUrl(body);

  // Extracting fully parsed response body.
  console.log(response.result);

  // Extracting response status code.
  console.log(response.statusCode);
  // Extracting response headers.
  console.log(response.headers);
  // Extracting response body of type `string | Stream`
  console.log(response.body);
} catch (error) {
  if (error instanceof ApiError) {
    // Extracting response error status code.
    console.log(error.statusCode);
    // Extracting response error headers.
    console.log(error.headers);
    // Extracting response error body of type `string | Stream`.
    console.log(error.body);
    if (error instanceof Scrape402Error) {
      console.log(error.result);
    } else if (error instanceof Scrape429Error) {
      console.log(error.result);
    } else if (error instanceof Scrape500Error) {
      console.log(error.result);
    }
  }
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 402 | Payment required | [`Scrape402Error`](../../doc/models/scrape-402-error.md) |
| 429 | Too many requests | [`Scrape429Error`](../../doc/models/scrape-429-error.md) |
| 500 | Server error | [`Scrape500Error`](../../doc/models/scrape-500-error.md) |


# Scrape and Extract from Urls

```ts
async scrapeAndExtractFromUrls(
  body: BatchScrapeRequest,
  requestOptions?: RequestOptions
): Promise<ApiResponse<BatchScrapeResponseObj>>
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`BatchScrapeRequest`](../../doc/models/batch-scrape-request.md) | Body, Required | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

**200**: Successful response

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`BatchScrapeResponseObj`](../../doc/models/batch-scrape-response-obj.md).

## Example Usage

```ts
const body: BatchScrapeRequest = {
  urls: [
    'urls3',
    'urls4'
  ],
  ignoreInvalidUrLs: false,
  onlyMainContent: true,
  maxAge: 0,
  waitFor: 0,
  mobile: false,
  skipTlsVerification: false,
  timeout: 30000,
  parsePdf: true,
  blockAds: true,
  storeInCache: true,
};

try {
  const response = await scrapingApi.scrapeAndExtractFromUrls(body);

  // Extracting fully parsed response body.
  console.log(response.result);

  // Extracting response status code.
  console.log(response.statusCode);
  // Extracting response headers.
  console.log(response.headers);
  // Extracting response body of type `string | Stream`
  console.log(response.body);
} catch (error) {
  if (error instanceof ApiError) {
    // Extracting response error status code.
    console.log(error.statusCode);
    // Extracting response error headers.
    console.log(error.headers);
    // Extracting response error body of type `string | Stream`.
    console.log(error.body);
    if (error instanceof BatchScrape402Error) {
      console.log(error.result);
    } else if (error instanceof BatchScrape429Error) {
      console.log(error.result);
    } else if (error instanceof BatchScrape500Error) {
      console.log(error.result);
    }
  }
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 402 | Payment required | [`BatchScrape402Error`](../../doc/models/batch-scrape-402-error.md) |
| 429 | Too many requests | [`BatchScrape429Error`](../../doc/models/batch-scrape-429-error.md) |
| 500 | Server error | [`BatchScrape500Error`](../../doc/models/batch-scrape-500-error.md) |


# Get Batch Scrape Status

```ts
async getBatchScrapeStatus(
  id: string,
  requestOptions?: RequestOptions
): Promise<ApiResponse<BatchScrapeStatusResponseObj>>
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `string` | Template, Required | The ID of the batch scrape job |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

**200**: Successful response

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`BatchScrapeStatusResponseObj`](../../doc/models/batch-scrape-status-response-obj.md).

## Example Usage

```ts
const id = '00001770-0000-0000-0000-000000000000';

try {
  const response = await scrapingApi.getBatchScrapeStatus(id);

  // Extracting fully parsed response body.
  console.log(response.result);

  // Extracting response status code.
  console.log(response.statusCode);
  // Extracting response headers.
  console.log(response.headers);
  // Extracting response body of type `string | Stream`
  console.log(response.body);
} catch (error) {
  if (error instanceof ApiError) {
    // Extracting response error status code.
    console.log(error.statusCode);
    // Extracting response error headers.
    console.log(error.headers);
    // Extracting response error body of type `string | Stream`.
    console.log(error.body);
    if (error instanceof BatchScrape402Error) {
      console.log(error.result);
    } else if (error instanceof BatchScrape429Error) {
      console.log(error.result);
    } else if (error instanceof BatchScrape500Error) {
      console.log(error.result);
    }
  }
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 402 | Payment required | [`BatchScrape402Error`](../../doc/models/batch-scrape-402-error.md) |
| 429 | Too many requests | [`BatchScrape429Error`](../../doc/models/batch-scrape-429-error.md) |
| 500 | Server error | [`BatchScrape500Error`](../../doc/models/batch-scrape-500-error.md) |


# Cancel Batch Scrape

```ts
async cancelBatchScrape(
  id: string,
  requestOptions?: RequestOptions
): Promise<ApiResponse<BatchScrapeResponse>>
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `string` | Template, Required | The ID of the batch scrape job |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

**200**: Successful cancellation

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`BatchScrapeResponse`](../../doc/models/batch-scrape-response.md).

## Example Usage

```ts
const id = '00001770-0000-0000-0000-000000000000';

try {
  const response = await scrapingApi.cancelBatchScrape(id);

  // Extracting fully parsed response body.
  console.log(response.result);

  // Extracting response status code.
  console.log(response.statusCode);
  // Extracting response headers.
  console.log(response.headers);
  // Extracting response body of type `string | Stream`
  console.log(response.body);
} catch (error) {
  if (error instanceof ApiError) {
    // Extracting response error status code.
    console.log(error.statusCode);
    // Extracting response error headers.
    console.log(error.headers);
    // Extracting response error body of type `string | Stream`.
    console.log(error.body);
    if (error instanceof BatchScrape404Error) {
      console.log(error.result);
    } else if (error instanceof BatchScrape500Error) {
      console.log(error.result);
    }
  }
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 404 | Batch scrape job not found | [`BatchScrape404Error`](../../doc/models/batch-scrape-404-error.md) |
| 500 | Server error | [`BatchScrape500Error`](../../doc/models/batch-scrape-500-error.md) |


# Get Batch Scrape Errors

```ts
async getBatchScrapeErrors(
  id: string,
  requestOptions?: RequestOptions
): Promise<ApiResponse<CrawlErrorsResponseObj>>
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `string` | Template, Required | The ID of the batch scrape job |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

**200**: Successful response

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`CrawlErrorsResponseObj`](../../doc/models/crawl-errors-response-obj.md).

## Example Usage

```ts
const id = '00001770-0000-0000-0000-000000000000';

try {
  const response = await scrapingApi.getBatchScrapeErrors(id);

  // Extracting fully parsed response body.
  console.log(response.result);

  // Extracting response status code.
  console.log(response.statusCode);
  // Extracting response headers.
  console.log(response.headers);
  // Extracting response body of type `string | Stream`
  console.log(response.body);
} catch (error) {
  if (error instanceof ApiError) {
    // Extracting response error status code.
    console.log(error.statusCode);
    // Extracting response error headers.
    console.log(error.headers);
    // Extracting response error body of type `string | Stream`.
    console.log(error.body);
    if (error instanceof BatchScrapeErrors402Error) {
      console.log(error.result);
    } else if (error instanceof BatchScrapeErrors429Error) {
      console.log(error.result);
    } else if (error instanceof BatchScrapeErrors500Error) {
      console.log(error.result);
    }
  }
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 402 | Payment required | [`BatchScrapeErrors402Error`](../../doc/models/batch-scrape-errors-402-error.md) |
| 429 | Too many requests | [`BatchScrapeErrors429Error`](../../doc/models/batch-scrape-errors-429-error.md) |
| 500 | Server error | [`BatchScrapeErrors500Error`](../../doc/models/batch-scrape-errors-500-error.md) |

