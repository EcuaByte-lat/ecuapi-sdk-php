# EcuaapiSdk\InvoicesApi



All URIs are relative to https://api.ecuapi.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**authorizeInvoice()**](InvoicesApi.md#authorizeInvoice) | **POST** /v1/invoices/{id}/authorize | Authorize invoice |
| [**createInvoice()**](InvoicesApi.md#createInvoice) | **POST** /v1/invoices | Create invoice |
| [**getInvoice()**](InvoicesApi.md#getInvoice) | **GET** /v1/invoices/{id} | Get invoice by ID |
| [**getInvoicePdf()**](InvoicesApi.md#getInvoicePdf) | **GET** /v1/invoices/{id}/pdf | Download RIDE PDF |
| [**getInvoiceXml()**](InvoicesApi.md#getInvoiceXml) | **GET** /v1/invoices/{id}/xml | Download signed XML |
| [**listInvoices()**](InvoicesApi.md#listInvoices) | **GET** /v1/invoices | List invoices |
| [**sendInvoice()**](InvoicesApi.md#sendInvoice) | **POST** /v1/invoices/{id}/send | Send invoice to SRI |
| [**voidInvoice()**](InvoicesApi.md#voidInvoice) | **DELETE** /v1/invoices/{id} | Void invoice |


## `authorizeInvoice()`

```php
authorizeInvoice($id): \EcuaapiSdk\Model\AuthorizeInvoiceResponse
```

Authorize invoice

Check authorization status with SRI after sending

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new EcuaapiSdk\Api\InvoicesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = inv_abc123; // string

try {
    $result = $apiInstance->authorizeInvoice($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InvoicesApi->authorizeInvoice: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**|  | |

### Return type

[**\EcuaapiSdk\Model\AuthorizeInvoiceResponse**](../Model/AuthorizeInvoiceResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `createInvoice()`

```php
createInvoice($create_invoice_request): \EcuaapiSdk\Model\CreateInvoiceResponse
```

Create invoice

Create a new invoice in draft status

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new EcuaapiSdk\Api\InvoicesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$create_invoice_request = new \EcuaapiSdk\Model\CreateInvoiceRequest(); // \EcuaapiSdk\Model\CreateInvoiceRequest

try {
    $result = $apiInstance->createInvoice($create_invoice_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InvoicesApi->createInvoice: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **create_invoice_request** | [**\EcuaapiSdk\Model\CreateInvoiceRequest**](../Model/CreateInvoiceRequest.md)|  | [optional] |

### Return type

[**\EcuaapiSdk\Model\CreateInvoiceResponse**](../Model/CreateInvoiceResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getInvoice()`

```php
getInvoice($id): \EcuaapiSdk\Model\InvoiceDetailResponse
```

Get invoice by ID

Retrieve a single invoice with all its items

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new EcuaapiSdk\Api\InvoicesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = inv_abc123; // string

try {
    $result = $apiInstance->getInvoice($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InvoicesApi->getInvoice: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**|  | |

### Return type

[**\EcuaapiSdk\Model\InvoiceDetailResponse**](../Model/InvoiceDetailResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getInvoicePdf()`

```php
getInvoicePdf($id): mixed
```

Download RIDE PDF

Generate and download the RIDE PDF for an invoice

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new EcuaapiSdk\Api\InvoicesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = inv_abc123; // string

try {
    $result = $apiInstance->getInvoicePdf($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InvoicesApi->getInvoicePdf: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**|  | |

### Return type

**mixed**

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/pdf`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getInvoiceXml()`

```php
getInvoiceXml($id): mixed
```

Download signed XML

Download the signed XML document for an invoice

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new EcuaapiSdk\Api\InvoicesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = inv_abc123; // string

try {
    $result = $apiInstance->getInvoiceXml($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InvoicesApi->getInvoiceXml: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**|  | |

### Return type

**mixed**

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/xml`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listInvoices()`

```php
listInvoices($status, $page, $limit): \EcuaapiSdk\Model\InvoiceListResponse
```

List invoices

Retrieve a paginated list of invoices for the organization

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new EcuaapiSdk\Api\InvoicesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$status = authorized; // string
$page = 1; // int
$limit = 20; // int

try {
    $result = $apiInstance->listInvoices($status, $page, $limit);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InvoicesApi->listInvoices: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **status** | **string**|  | [optional] |
| **page** | **int**|  | [optional] [default to 1] |
| **limit** | **int**|  | [optional] [default to 20] |

### Return type

[**\EcuaapiSdk\Model\InvoiceListResponse**](../Model/InvoiceListResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `sendInvoice()`

```php
sendInvoice($id): \EcuaapiSdk\Model\SendInvoiceResponse
```

Send invoice to SRI

Sign and send the invoice to SRI for processing

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new EcuaapiSdk\Api\InvoicesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = inv_abc123; // string

try {
    $result = $apiInstance->sendInvoice($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InvoicesApi->sendInvoice: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**|  | |

### Return type

[**\EcuaapiSdk\Model\SendInvoiceResponse**](../Model/SendInvoiceResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `voidInvoice()`

```php
voidInvoice($id)
```

Void invoice

Void/cancel an invoice (not yet implemented)

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new EcuaapiSdk\Api\InvoicesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = inv_abc123; // string

try {
    $apiInstance->voidInvoice($id);
} catch (Exception $e) {
    echo 'Exception when calling InvoicesApi->voidInvoice: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**|  | |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
