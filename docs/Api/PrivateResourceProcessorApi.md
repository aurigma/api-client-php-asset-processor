# Aurigma\AssetProcessor\PrivateResourceProcessorApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**privateResourceProcessorImportResource()**](PrivateResourceProcessorApi.md#privateResourceProcessorImportResource) | **POST** /api/processor/v1/private-resources/import | Imports a resource from the source file and saves it to the private storage. |
| [**privateResourceProcessorImportResourceFromUrl()**](PrivateResourceProcessorApi.md#privateResourceProcessorImportResourceFromUrl) | **POST** /api/processor/v1/private-resources/import/from-url | Imports a resource from the remote source file and saves it to the private storage. |
| [**privateResourceProcessorUpdate()**](PrivateResourceProcessorApi.md#privateResourceProcessorUpdate) | **POST** /api/processor/v1/private-resources/{id}/update | Updates the resource file and metadata in the private storage. |


## `privateResourceProcessorImportResource()`

```php
privateResourceProcessorImportResource($source_file, $tenant_id, $owner_id, $name, $namespace, $source_id, $custom_fields, $type, $format, $anonymous_access): \Aurigma\AssetProcessor\Model\ResourceDto
```

Imports a resource from the source file and saves it to the private storage.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKey
$config = Aurigma\AssetProcessor\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Aurigma\AssetProcessor\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');

// Configure OAuth2 access token for authorization: OAuth2ClientCredentials
$config = Aurigma\AssetProcessor\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

// Configure OAuth2 access token for authorization: OAuth2Code
$config = Aurigma\AssetProcessor\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

// Configure OAuth2 access token for authorization: OAuth2Implicit
$config = Aurigma\AssetProcessor\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

// Configure API key authorization: Bearer
$config = Aurigma\AssetProcessor\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Aurigma\AssetProcessor\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new Aurigma\AssetProcessor\Api\PrivateResourceProcessorApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$source_file = "/path/to/file.txt"; // \SplFileObject | Resource source file.
$tenant_id = 56; // int | Tenant ID.
$owner_id = 'owner_id_example'; // string
$name = 'name_example'; // string | Resource name.
$namespace = 'namespace_example'; // string | Resource namespace.
$source_id = 'source_id_example'; // string | Resource source identifier.
$custom_fields = NULL; // array<string,mixed> | Resource custom fields.
$type = 'type_example'; // string | Resource type.
$format = 'format_example'; // string | Resource format.
$anonymous_access = True; // bool | Indicates if a resource should be available by link without authorization.

try {
    $result = $apiInstance->privateResourceProcessorImportResource($source_file, $tenant_id, $owner_id, $name, $namespace, $source_id, $custom_fields, $type, $format, $anonymous_access);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PrivateResourceProcessorApi->privateResourceProcessorImportResource: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **source_file** | **\SplFileObject****\SplFileObject**| Resource source file. | |
| **tenant_id** | **int**| Tenant ID. | [optional] |
| **owner_id** | **string**|  | [optional] |
| **name** | **string**| Resource name. | [optional] |
| **namespace** | **string**| Resource namespace. | [optional] |
| **source_id** | **string**| Resource source identifier. | [optional] |
| **custom_fields** | [**array<string,mixed>**](../Model/array.md)| Resource custom fields. | [optional] |
| **type** | **string**| Resource type. | [optional] |
| **format** | **string**| Resource format. | [optional] |
| **anonymous_access** | **bool**| Indicates if a resource should be available by link without authorization. | [optional] |

### Return type

[**\Aurigma\AssetProcessor\Model\ResourceDto**](../Model/ResourceDto.md)

### Authorization

[ApiKey](../../README.md#ApiKey), [OAuth2ClientCredentials](../../README.md#OAuth2ClientCredentials), [OAuth2Code](../../README.md#OAuth2Code), [OAuth2Implicit](../../README.md#OAuth2Implicit), [Bearer](../../README.md#Bearer)

### HTTP request headers

- **Content-Type**: `multipart/form-data`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `privateResourceProcessorImportResourceFromUrl()`

```php
privateResourceProcessorImportResourceFromUrl($tenant_id, $owner_id, $import_resource_from_url_model): \Aurigma\AssetProcessor\Model\ResourceDto
```

Imports a resource from the remote source file and saves it to the private storage.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKey
$config = Aurigma\AssetProcessor\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Aurigma\AssetProcessor\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');

// Configure OAuth2 access token for authorization: OAuth2ClientCredentials
$config = Aurigma\AssetProcessor\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

// Configure OAuth2 access token for authorization: OAuth2Code
$config = Aurigma\AssetProcessor\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

// Configure OAuth2 access token for authorization: OAuth2Implicit
$config = Aurigma\AssetProcessor\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

// Configure API key authorization: Bearer
$config = Aurigma\AssetProcessor\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Aurigma\AssetProcessor\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new Aurigma\AssetProcessor\Api\PrivateResourceProcessorApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenant_id = 56; // int | Tenant ID.
$owner_id = 'owner_id_example'; // string
$import_resource_from_url_model = new \Aurigma\AssetProcessor\Model\ImportResourceFromUrlModel(); // \Aurigma\AssetProcessor\Model\ImportResourceFromUrlModel | Parameters of the import operation.

try {
    $result = $apiInstance->privateResourceProcessorImportResourceFromUrl($tenant_id, $owner_id, $import_resource_from_url_model);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PrivateResourceProcessorApi->privateResourceProcessorImportResourceFromUrl: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenant_id** | **int**| Tenant ID. | [optional] |
| **owner_id** | **string**|  | [optional] |
| **import_resource_from_url_model** | [**\Aurigma\AssetProcessor\Model\ImportResourceFromUrlModel**](../Model/ImportResourceFromUrlModel.md)| Parameters of the import operation. | [optional] |

### Return type

[**\Aurigma\AssetProcessor\Model\ResourceDto**](../Model/ResourceDto.md)

### Authorization

[ApiKey](../../README.md#ApiKey), [OAuth2ClientCredentials](../../README.md#OAuth2ClientCredentials), [OAuth2Code](../../README.md#OAuth2Code), [OAuth2Implicit](../../README.md#OAuth2Implicit), [Bearer](../../README.md#Bearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `privateResourceProcessorUpdate()`

```php
privateResourceProcessorUpdate($id, $tenant_id, $owner_id, $name, $namespace, $source_id, $custom_fields, $type, $format, $anonymous_access, $file): \Aurigma\AssetProcessor\Model\ResourceDto
```

Updates the resource file and metadata in the private storage.

If the resource file is not provided, the metadata will be updated using the file from the repository.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKey
$config = Aurigma\AssetProcessor\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Aurigma\AssetProcessor\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');

// Configure OAuth2 access token for authorization: OAuth2ClientCredentials
$config = Aurigma\AssetProcessor\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

// Configure OAuth2 access token for authorization: OAuth2Code
$config = Aurigma\AssetProcessor\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

// Configure OAuth2 access token for authorization: OAuth2Implicit
$config = Aurigma\AssetProcessor\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

// Configure API key authorization: Bearer
$config = Aurigma\AssetProcessor\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Aurigma\AssetProcessor\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new Aurigma\AssetProcessor\Api\PrivateResourceProcessorApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | Resource entity ID.
$tenant_id = 56; // int | Tenant ID.
$owner_id = 'owner_id_example'; // string
$name = 'name_example'; // string | Resource name.
$namespace = 'namespace_example'; // string | Resource namespace.
$source_id = 'source_id_example'; // string | Resource source identifier.
$custom_fields = NULL; // array<string,mixed> | Resource custom fields.
$type = 'type_example'; // string | Resource type.
$format = 'format_example'; // string | Resource format.
$anonymous_access = True; // bool | Indicates if a resource should be available by link without authorization.
$file = "/path/to/file.txt"; // \SplFileObject | Resource source file.

try {
    $result = $apiInstance->privateResourceProcessorUpdate($id, $tenant_id, $owner_id, $name, $namespace, $source_id, $custom_fields, $type, $format, $anonymous_access, $file);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PrivateResourceProcessorApi->privateResourceProcessorUpdate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Resource entity ID. | |
| **tenant_id** | **int**| Tenant ID. | [optional] |
| **owner_id** | **string**|  | [optional] |
| **name** | **string**| Resource name. | [optional] |
| **namespace** | **string**| Resource namespace. | [optional] |
| **source_id** | **string**| Resource source identifier. | [optional] |
| **custom_fields** | [**array<string,mixed>**](../Model/array.md)| Resource custom fields. | [optional] |
| **type** | **string**| Resource type. | [optional] |
| **format** | **string**| Resource format. | [optional] |
| **anonymous_access** | **bool**| Indicates if a resource should be available by link without authorization. | [optional] |
| **file** | **\SplFileObject****\SplFileObject**| Resource source file. | [optional] |

### Return type

[**\Aurigma\AssetProcessor\Model\ResourceDto**](../Model/ResourceDto.md)

### Authorization

[ApiKey](../../README.md#ApiKey), [OAuth2ClientCredentials](../../README.md#OAuth2ClientCredentials), [OAuth2Code](../../README.md#OAuth2Code), [OAuth2Implicit](../../README.md#OAuth2Implicit), [Bearer](../../README.md#Bearer)

### HTTP request headers

- **Content-Type**: `multipart/form-data`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
