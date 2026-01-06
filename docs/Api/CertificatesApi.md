# EcuaapiSdk\CertificatesApi



All URIs are relative to https://api.ecuapi.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**listCertificates()**](CertificatesApi.md#listCertificates) | **GET** /v1/certificates | List certificates |
| [**uploadCertificate()**](CertificatesApi.md#uploadCertificate) | **POST** /v1/certificates/upload | Upload P12 certificate |


## `listCertificates()`

```php
listCertificates(): \EcuaapiSdk\Model\CertificateListResponse
```

List certificates

List all certificates for the organization

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new EcuaapiSdk\Api\CertificatesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->listCertificates();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CertificatesApi->listCertificates: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\EcuaapiSdk\Model\CertificateListResponse**](../Model/CertificateListResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `uploadCertificate()`

```php
uploadCertificate($password, $file, $alias): \EcuaapiSdk\Model\CertificateUploadResponse
```

Upload P12 certificate

Upload a P12 electronic signature certificate for signing invoices

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new EcuaapiSdk\Api\CertificatesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$password = 'password_example'; // string
$file = '/path/to/file.txt'; // \SplFileObject | P12 certificate file
$alias = 'alias_example'; // string

try {
    $result = $apiInstance->uploadCertificate($password, $file, $alias);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CertificatesApi->uploadCertificate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **password** | **string**|  | |
| **file** | **\SplFileObject****\SplFileObject**| P12 certificate file | [optional] |
| **alias** | **string**|  | [optional] |

### Return type

[**\EcuaapiSdk\Model\CertificateUploadResponse**](../Model/CertificateUploadResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `multipart/form-data`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
