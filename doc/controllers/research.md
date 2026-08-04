# Research

```ts
const researchApi = new ResearchApi(client);
```

## Class Name

`ResearchApi`

## Methods

* [Start Deep Research](../../doc/controllers/research.md#start-deep-research)
* [Get Deep Research Status](../../doc/controllers/research.md#get-deep-research-status)


# Start Deep Research

```ts
async startDeepResearch(
  body: DeepResearchRequest,
  requestOptions?: RequestOptions
): Promise<ApiResponse<DeepResearchResponse>>
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`DeepResearchRequest`](../../doc/models/deep-research-request.md) | Body, Required | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

**200**: Research job started successfully

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`DeepResearchResponse`](../../doc/models/deep-research-response.md).

## Example Usage

```ts
const body: DeepResearchRequest = {
  query: 'query6',
  maxDepth: 7,
  timeLimit: 300,
  maxUrls: 20,
};

try {
  const response = await researchApi.startDeepResearch(body);

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
    if (error instanceof DeepResearch400Error) {
      console.log(error.result);
    }
  }
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Invalid request parameters | [`DeepResearch400Error`](../../doc/models/deep-research-400-error.md) |


# Get Deep Research Status

```ts
async getDeepResearchStatus(
  id: string,
  requestOptions?: RequestOptions
): Promise<ApiResponse<DeepResearchResponse1>>
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `string` | Template, Required | The ID of the research job |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

**200**: Successful response

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`DeepResearchResponse1`](../../doc/models/deep-research-response-1.md).

## Example Usage

```ts
const id = '00001770-0000-0000-0000-000000000000';

try {
  const response = await researchApi.getDeepResearchStatus(id);

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
    if (error instanceof DeepResearch404Error) {
      console.log(error.result);
    }
  }
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 404 | Research job not found | [`DeepResearch404Error`](../../doc/models/deep-research-404-error.md) |

