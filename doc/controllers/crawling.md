# Crawling

```ts
const crawlingApi = new CrawlingApi(client);
```

## Class Name

`CrawlingApi`

## Methods

* [Get Crawl Status](../../doc/controllers/crawling.md#get-crawl-status)
* [Cancel Crawl](../../doc/controllers/crawling.md#cancel-crawl)
* [Get Crawl Errors](../../doc/controllers/crawling.md#get-crawl-errors)
* [Crawl Urls](../../doc/controllers/crawling.md#crawl-urls)
* [Get Active Crawls](../../doc/controllers/crawling.md#get-active-crawls)


# Get Crawl Status

```ts
async getCrawlStatus(
  id: string,
  requestOptions?: RequestOptions
): Promise<ApiResponse<CrawlStatusResponseObj>>
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `string` | Template, Required | The ID of the crawl job |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

**200**: Successful response

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`CrawlStatusResponseObj`](../../doc/models/crawl-status-response-obj.md).

## Example Usage

```ts
const id = '00001770-0000-0000-0000-000000000000';

try {
  const response = await crawlingApi.getCrawlStatus(id);

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
    if (error instanceof Crawl402Error) {
      console.log(error.result);
    } else if (error instanceof Crawl429Error) {
      console.log(error.result);
    } else if (error instanceof Crawl500Error) {
      console.log(error.result);
    }
  }
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 402 | Payment required | [`Crawl402Error`](../../doc/models/crawl-402-error.md) |
| 429 | Too many requests | [`Crawl429Error`](../../doc/models/crawl-429-error.md) |
| 500 | Server error | [`Crawl500Error`](../../doc/models/crawl-500-error.md) |


# Cancel Crawl

```ts
async cancelCrawl(
  id: string,
  requestOptions?: RequestOptions
): Promise<ApiResponse<CrawlResponse1>>
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `string` | Template, Required | The ID of the crawl job |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

**200**: Successful cancellation

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`CrawlResponse1`](../../doc/models/crawl-response-1.md).

## Example Usage

```ts
const id = '00001770-0000-0000-0000-000000000000';

try {
  const response = await crawlingApi.cancelCrawl(id);

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
    if (error instanceof Crawl404Error) {
      console.log(error.result);
    } else if (error instanceof Crawl500Error) {
      console.log(error.result);
    }
  }
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 404 | Crawl job not found | [`Crawl404Error`](../../doc/models/crawl-404-error.md) |
| 500 | Server error | [`Crawl500Error`](../../doc/models/crawl-500-error.md) |


# Get Crawl Errors

```ts
async getCrawlErrors(
  id: string,
  requestOptions?: RequestOptions
): Promise<ApiResponse<CrawlErrorsResponseObj>>
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `string` | Template, Required | The ID of the crawl job |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

**200**: Successful response

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`CrawlErrorsResponseObj`](../../doc/models/crawl-errors-response-obj.md).

## Example Usage

```ts
const id = '00001770-0000-0000-0000-000000000000';

try {
  const response = await crawlingApi.getCrawlErrors(id);

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
    if (error instanceof CrawlErrors402Error) {
      console.log(error.result);
    } else if (error instanceof CrawlErrors429Error) {
      console.log(error.result);
    } else if (error instanceof CrawlErrors500Error) {
      console.log(error.result);
    }
  }
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 402 | Payment required | [`CrawlErrors402Error`](../../doc/models/crawl-errors-402-error.md) |
| 429 | Too many requests | [`CrawlErrors429Error`](../../doc/models/crawl-errors-429-error.md) |
| 500 | Server error | [`CrawlErrors500Error`](../../doc/models/crawl-errors-500-error.md) |


# Crawl Urls

```ts
async crawlUrls(
  body: CrawlRequest,
  requestOptions?: RequestOptions
): Promise<ApiResponse<CrawlResponse>>
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`CrawlRequest`](../../doc/models/crawl-request.md) | Body, Required | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

**200**: Successful response

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`CrawlResponse`](../../doc/models/crawl-response.md).

## Example Usage

```ts
const body: CrawlRequest = {
  url: 'url0',
  maxDepth: 10,
  ignoreSitemap: false,
  ignoreQueryParameters: false,
  limit: 10000,
  allowBackwardLinks: false,
  allowExternalLinks: false,
};

try {
  const response = await crawlingApi.crawlUrls(body);

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
    if (error instanceof Crawl402Error) {
      console.log(error.result);
    } else if (error instanceof Crawl429Error) {
      console.log(error.result);
    } else if (error instanceof Crawl500Error) {
      console.log(error.result);
    }
  }
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 402 | Payment required | [`Crawl402Error`](../../doc/models/crawl-402-error.md) |
| 429 | Too many requests | [`Crawl429Error`](../../doc/models/crawl-429-error.md) |
| 500 | Server error | [`Crawl500Error`](../../doc/models/crawl-500-error.md) |


# Get Active Crawls

```ts
async getActiveCrawls(
  requestOptions?: RequestOptions
): Promise<ApiResponse<CrawlActiveResponse>>
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

**200**: Successful response

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`CrawlActiveResponse`](../../doc/models/crawl-active-response.md).

## Example Usage

```ts
try {
  const response = await crawlingApi.getActiveCrawls();

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
    if (error instanceof CrawlActive402Error) {
      console.log(error.result);
    } else if (error instanceof CrawlActive429Error) {
      console.log(error.result);
    } else if (error instanceof CrawlActive500Error) {
      console.log(error.result);
    }
  }
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 402 | Payment required | [`CrawlActive402Error`](../../doc/models/crawl-active-402-error.md) |
| 429 | Too many requests | [`CrawlActive429Error`](../../doc/models/crawl-active-429-error.md) |
| 500 | Server error | [`CrawlActive500Error`](../../doc/models/crawl-active-500-error.md) |

