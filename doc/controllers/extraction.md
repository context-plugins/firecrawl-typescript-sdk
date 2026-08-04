# Extraction

```ts
const extractionApi = new ExtractionApi(client);
```

## Class Name

`ExtractionApi`

## Methods

* [Extract Data](../../doc/controllers/extraction.md#extract-data)
* [Get Extract Status](../../doc/controllers/extraction.md#get-extract-status)


# Extract Data

```ts
async extractData(
  body: ExtractRequest,
  requestOptions?: RequestOptions
): Promise<ApiResponse<ExtractResponse>>
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`ExtractRequest`](../../doc/models/extract-request.md) | Body, Required | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

**200**: Successful extraction

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`ExtractResponse`](../../doc/models/extract-response.md).

## Example Usage

```ts
const body: ExtractRequest = {
  urls: [
    'urls3',
    'urls4'
  ],
  enableWebSearch: false,
  ignoreSitemap: false,
  includeSubdomains: true,
  showSources: false,
  ignoreInvalidUrLs: false,
};

try {
  const response = await extractionApi.extractData(body);

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
    if (error instanceof Extract400Error) {
      console.log(error.result);
    } else if (error instanceof Extract500Error) {
      console.log(error.result);
    }
  }
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Invalid request | [`Extract400Error`](../../doc/models/extract-400-error.md) |
| 500 | Server error | [`Extract500Error`](../../doc/models/extract-500-error.md) |


# Get Extract Status

```ts
async getExtractStatus(
  id: string,
  requestOptions?: RequestOptions
): Promise<ApiResponse<ExtractStatusResponse>>
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `string` | Template, Required | The ID of the extract job |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

**200**: Successful response

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`ExtractStatusResponse`](../../doc/models/extract-status-response.md).

## Example Usage

```ts
const id = '00001770-0000-0000-0000-000000000000';

try {
  const response = await extractionApi.getExtractStatus(id);

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
  }
}
```

