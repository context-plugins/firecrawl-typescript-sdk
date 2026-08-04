# Feedback

```ts
const feedbackApi = new FeedbackApi(client);
```

## Class Name

`FeedbackApi`


# Submit Endpoint Feedback

```ts
async submitEndpointFeedback(
  body: EndpointFeedbackRequest,
  requestOptions?: RequestOptions
): Promise<ApiResponse<FeedbackResponse>>
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`EndpointFeedbackRequest`](../../doc/models/endpoint-feedback-request.md) | Body, Required | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

**200**: Feedback recorded

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`FeedbackResponse`](../../doc/models/feedback-response.md).

## Example Usage

```ts
const body: EndpointFeedbackRequest = {
  rating: Rating.Partial,
  endpoint: Endpoint.Parse,
  jobId: '00001faa-0000-0000-0000-000000000000',
  origin: 'api',
};

try {
  const response = await feedbackApi.submitEndpointFeedback(body);

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
| 404 | Job not found for this team | [`FeedbackErrorResponseError`](../../doc/models/feedback-error-response-error.md) |
| 409 | Feedback cannot be recorded for this job | [`FeedbackErrorResponseError`](../../doc/models/feedback-error-response-error.md) |
| 500 | Server error | [`FeedbackErrorResponseError`](../../doc/models/feedback-error-response-error.md) |

