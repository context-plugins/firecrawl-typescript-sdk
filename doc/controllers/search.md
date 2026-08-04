# Search

```ts
const searchApi = new SearchApi(client);
```

## Class Name

`SearchApi`

## Methods

* [Search and Scrape](../../doc/controllers/search.md#search-and-scrape)
* [Submit Search Feedback](../../doc/controllers/search.md#submit-search-feedback)


# Search and Scrape

```ts
async searchAndScrape(
  body: SearchRequest,
  requestOptions?: RequestOptions
): Promise<ApiResponse<SearchResponse>>
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`SearchRequest`](../../doc/models/search-request.md) | Body, Required | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

**200**: Successful response

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`SearchResponse`](../../doc/models/search-response.md).

## Example Usage

```ts
const body: SearchRequest = {
  query: 'query6',
  limit: 5,
  timeout: 60000,
  ignoreInvalidUrLs: false,
};

try {
  const response = await searchApi.searchAndScrape(body);

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
    if (error instanceof Search408Error) {
      console.log(error.result);
    } else if (error instanceof Search500Error) {
      console.log(error.result);
    }
  }
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 408 | Request timeout | [`Search408Error`](../../doc/models/search-408-error.md) |
| 500 | Server error | [`Search500Error`](../../doc/models/search-500-error.md) |


# Submit Search Feedback

```ts
async submitSearchFeedback(
  jobId: string,
  body: SearchFeedbackRequest,
  requestOptions?: RequestOptions
): Promise<ApiResponse<FeedbackResponse>>
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `jobId` | `string` | Template, Required | Search job id returned by /search. |
| `body` | [`SearchFeedbackRequest`](../../doc/models/search-feedback-request.md) | Body, Required | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

**200**: Feedback recorded

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`FeedbackResponse`](../../doc/models/feedback-response.md).

## Example Usage

```ts
const jobId = '000011b2-0000-0000-0000-000000000000';

const body: SearchFeedbackRequest = {
  rating: Rating.Partial,
  origin: 'api',
};

try {
  const response = await searchApi.submitSearchFeedback(
    jobId,
    body
  );

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
    if (error instanceof FeedbackErrorResponseError) {
      console.log(error.result);
    }
  }
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Invalid request body | [`FeedbackErrorResponseError`](../../doc/models/feedback-error-response-error.md) |
| 403 | Feedback is not available for this team | [`FeedbackErrorResponseError`](../../doc/models/feedback-error-response-error.md) |
| 404 | Search not found for this team | [`FeedbackErrorResponseError`](../../doc/models/feedback-error-response-error.md) |
| 409 | Feedback cannot be recorded for this search | [`FeedbackErrorResponseError`](../../doc/models/feedback-error-response-error.md) |
| 500 | Server error | [`FeedbackErrorResponseError`](../../doc/models/feedback-error-response-error.md) |

