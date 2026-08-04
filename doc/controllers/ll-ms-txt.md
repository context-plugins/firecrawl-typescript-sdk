# LL Ms Txt

```ts
const llMsTxtApi = new LlMsTxtApi(client);
```

## Class Name

`LlMsTxtApi`

## Methods

* [Generate LL Ms Txt](../../doc/controllers/ll-ms-txt.md#generate-ll-ms-txt)
* [Get LL Ms Txt Status](../../doc/controllers/ll-ms-txt.md#get-ll-ms-txt-status)


# Generate LL Ms Txt

```ts
async generateLlMsTxt(
  body: LlmstxtRequest,
  requestOptions?: RequestOptions
): Promise<ApiResponse<LlmstxtResponse>>
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`LlmstxtRequest`](../../doc/models/llmstxt-request.md) | Body, Required | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

**200**: LLMs.txt generation job started successfully

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`LlmstxtResponse`](../../doc/models/llmstxt-response.md).

## Example Usage

```ts
const body: LlmstxtRequest = {
  url: 'url0',
  maxUrls: 2,
  showFullText: false,
};

try {
  const response = await llMsTxtApi.generateLlMsTxt(body);

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
    if (error instanceof Llmstxt400Error) {
      console.log(error.result);
    }
  }
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Invalid request parameters | [`Llmstxt400Error`](../../doc/models/llmstxt-400-error.md) |


# Get LL Ms Txt Status

```ts
async getLlMsTxtStatus(
  id: string,
  requestOptions?: RequestOptions
): Promise<ApiResponse<LlmstxtResponse1>>
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `string` | Template, Required | The ID of the LLMs.txt generation job |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

**200**: Successful response

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`LlmstxtResponse1`](../../doc/models/llmstxt-response-1.md).

## Example Usage

```ts
const id = '00001770-0000-0000-0000-000000000000';

try {
  const response = await llMsTxtApi.getLlMsTxtStatus(id);

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
    if (error instanceof Llmstxt404Error) {
      console.log(error.result);
    }
  }
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 404 | LLMs.txt generation job not found | [`Llmstxt404Error`](../../doc/models/llmstxt-404-error.md) |

