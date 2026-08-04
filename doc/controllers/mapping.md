# Mapping

```ts
const mappingApi = new MappingApi(client);
```

## Class Name

`MappingApi`


# Map Urls

```ts
async mapUrls(
  body: MapRequest,
  requestOptions?: RequestOptions
): Promise<ApiResponse<MapResponse>>
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`MapRequest`](../../doc/models/map-request.md) | Body, Required | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

**200**: Successful response

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`MapResponse`](../../doc/models/map-response.md).

## Example Usage

```ts
const body: MapRequest = {
  url: 'url0',
  ignoreSitemap: true,
  sitemapOnly: false,
  includeSubdomains: true,
  limit: 5000,
};

try {
  const response = await mappingApi.mapUrls(body);

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
    if (error instanceof Map402Error) {
      console.log(error.result);
    } else if (error instanceof Map429Error) {
      console.log(error.result);
    } else if (error instanceof Map500Error) {
      console.log(error.result);
    }
  }
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 402 | Payment required | [`Map402Error`](../../doc/models/map-402-error.md) |
| 429 | Too many requests | [`Map429Error`](../../doc/models/map-429-error.md) |
| 500 | Server error | [`Map500Error`](../../doc/models/map-500-error.md) |

