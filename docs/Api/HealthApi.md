# EcuaapiSdk\HealthApi



All URIs are relative to https://api.ecuapi.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getApiInfo()**](HealthApi.md#getApiInfo) | **GET** /health | Basic health check |
| [**getApiInfo_0()**](HealthApi.md#getApiInfo_0) | **GET** /v1/health | Basic health check |
| [**getDetailedHealth()**](HealthApi.md#getDetailedHealth) | **GET** /health/health | Detailed health check |
| [**getDetailedHealth_0()**](HealthApi.md#getDetailedHealth_0) | **GET** /v1/health/health | Detailed health check |


## `getApiInfo()`

```php
getApiInfo(): \EcuaapiSdk\Model\HealthResponse
```

Basic health check

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new EcuaapiSdk\Api\HealthApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->getApiInfo();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling HealthApi->getApiInfo: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\EcuaapiSdk\Model\HealthResponse**](../Model/HealthResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getApiInfo_0()`

```php
getApiInfo_0(): \EcuaapiSdk\Model\HealthResponse
```

Basic health check

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new EcuaapiSdk\Api\HealthApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->getApiInfo_0();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling HealthApi->getApiInfo_0: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\EcuaapiSdk\Model\HealthResponse**](../Model/HealthResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getDetailedHealth()`

```php
getDetailedHealth(): \EcuaapiSdk\Model\HealthResponse
```

Detailed health check

Comprehensive health check including database and storage status

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new EcuaapiSdk\Api\HealthApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->getDetailedHealth();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling HealthApi->getDetailedHealth: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\EcuaapiSdk\Model\HealthResponse**](../Model/HealthResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getDetailedHealth_0()`

```php
getDetailedHealth_0(): \EcuaapiSdk\Model\HealthResponse
```

Detailed health check

Comprehensive health check including database and storage status

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new EcuaapiSdk\Api\HealthApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->getDetailedHealth_0();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling HealthApi->getDetailedHealth_0: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\EcuaapiSdk\Model\HealthResponse**](../Model/HealthResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
