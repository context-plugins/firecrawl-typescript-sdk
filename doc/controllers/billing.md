# Billing

```ts
const billingApi = new BillingApi(client);
```

## Class Name

`BillingApi`

## Methods

* [Get Credit Usage](../../doc/controllers/billing.md#get-credit-usage)
* [Get Token Usage](../../doc/controllers/billing.md#get-token-usage)


# Get Credit Usage

```ts
async getCreditUsage(
  requestOptions?: RequestOptions
): Promise<ApiResponse<TeamCreditUsageResponse>>
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

**200**: Successful response

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`TeamCreditUsageResponse`](../../doc/models/team-credit-usage-response.md).

## Example Usage

```ts
try {
  const response = await billingApi.getCreditUsage();

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
    if (error instanceof TeamCreditUsage404Error) {
      console.log(error.result);
    } else if (error instanceof TeamCreditUsage500Error) {
      console.log(error.result);
    }
  }
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 404 | Credit usage information not found | [`TeamCreditUsage404Error`](../../doc/models/team-credit-usage-404-error.md) |
| 500 | Server error | [`TeamCreditUsage500Error`](../../doc/models/team-credit-usage-500-error.md) |


# Get Token Usage

```ts
async getTokenUsage(
  requestOptions?: RequestOptions
): Promise<ApiResponse<TeamTokenUsageResponse>>
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

**200**: Successful response

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`TeamTokenUsageResponse`](../../doc/models/team-token-usage-response.md).

## Example Usage

```ts
try {
  const response = await billingApi.getTokenUsage();

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
    if (error instanceof TeamTokenUsage404Error) {
      console.log(error.result);
    } else if (error instanceof TeamTokenUsage500Error) {
      console.log(error.result);
    }
  }
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 404 | Token usage information not found | [`TeamTokenUsage404Error`](../../doc/models/team-token-usage-404-error.md) |
| 500 | Server error | [`TeamTokenUsage500Error`](../../doc/models/team-token-usage-500-error.md) |

