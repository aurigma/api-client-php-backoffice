# Aurigma\BackOffice\ProjectStatusesManagementApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**projectStatusesManagementCreate()**](ProjectStatusesManagementApi.md#projectStatusesManagementCreate) | **POST** /api/backoffice/v1/projects-statuses | Creates a new project status and returns its description. |
| [**projectStatusesManagementDelete()**](ProjectStatusesManagementApi.md#projectStatusesManagementDelete) | **DELETE** /api/backoffice/v1/projects-statuses/{id} | Deletes an existing project status and returns its description. |
| [**projectStatusesManagementGet()**](ProjectStatusesManagementApi.md#projectStatusesManagementGet) | **GET** /api/backoffice/v1/projects-statuses/{id} | Returns a project status by its identifier. |
| [**projectStatusesManagementGetAll()**](ProjectStatusesManagementApi.md#projectStatusesManagementGetAll) | **GET** /api/backoffice/v1/projects-statuses | Returns a list of all existing project statuses. |
| [**projectStatusesManagementUpdate()**](ProjectStatusesManagementApi.md#projectStatusesManagementUpdate) | **PUT** /api/backoffice/v1/projects-statuses/{id} | Updates an existing project status and returns its description. |


## `projectStatusesManagementCreate()`

```php
projectStatusesManagementCreate($tenant_id, $project_statuses_management_create_request): \Aurigma\BackOffice\Model\ProjectStatusDto
```

Creates a new project status and returns its description.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKey
$config = Aurigma\BackOffice\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Aurigma\BackOffice\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');

// Configure OAuth2 access token for authorization: OAuth2ClientCredentials
$config = Aurigma\BackOffice\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

// Configure OAuth2 access token for authorization: OAuth2Implicit
$config = Aurigma\BackOffice\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

// Configure API key authorization: Bearer
$config = Aurigma\BackOffice\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Aurigma\BackOffice\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new Aurigma\BackOffice\Api\ProjectStatusesManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenant_id = 56; // int | Tenant identifier.
$project_statuses_management_create_request = new \Aurigma\BackOffice\Model\ProjectStatusesManagementCreateRequest(); // \Aurigma\BackOffice\Model\ProjectStatusesManagementCreateRequest | Status creation parameters.

try {
    $result = $apiInstance->projectStatusesManagementCreate($tenant_id, $project_statuses_management_create_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProjectStatusesManagementApi->projectStatusesManagementCreate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenant_id** | **int**| Tenant identifier. | [optional] |
| **project_statuses_management_create_request** | [**\Aurigma\BackOffice\Model\ProjectStatusesManagementCreateRequest**](../Model/ProjectStatusesManagementCreateRequest.md)| Status creation parameters. | [optional] |

### Return type

[**\Aurigma\BackOffice\Model\ProjectStatusDto**](../Model/ProjectStatusDto.md)

### Authorization

[ApiKey](../../README.md#ApiKey), [OAuth2ClientCredentials](../../README.md#OAuth2ClientCredentials), [OAuth2Implicit](../../README.md#OAuth2Implicit), [Bearer](../../README.md#Bearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `projectStatusesManagementDelete()`

```php
projectStatusesManagementDelete($id, $tenant_id): \Aurigma\BackOffice\Model\ProjectStatusDto
```

Deletes an existing project status and returns its description.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKey
$config = Aurigma\BackOffice\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Aurigma\BackOffice\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');

// Configure OAuth2 access token for authorization: OAuth2ClientCredentials
$config = Aurigma\BackOffice\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

// Configure OAuth2 access token for authorization: OAuth2Implicit
$config = Aurigma\BackOffice\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

// Configure API key authorization: Bearer
$config = Aurigma\BackOffice\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Aurigma\BackOffice\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new Aurigma\BackOffice\Api\ProjectStatusesManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | Status identifier.
$tenant_id = 56; // int | Tenant identifier.

try {
    $result = $apiInstance->projectStatusesManagementDelete($id, $tenant_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProjectStatusesManagementApi->projectStatusesManagementDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **int**| Status identifier. | |
| **tenant_id** | **int**| Tenant identifier. | [optional] |

### Return type

[**\Aurigma\BackOffice\Model\ProjectStatusDto**](../Model/ProjectStatusDto.md)

### Authorization

[ApiKey](../../README.md#ApiKey), [OAuth2ClientCredentials](../../README.md#OAuth2ClientCredentials), [OAuth2Implicit](../../README.md#OAuth2Implicit), [Bearer](../../README.md#Bearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `projectStatusesManagementGet()`

```php
projectStatusesManagementGet($id, $tenant_id): \Aurigma\BackOffice\Model\ProjectStatusDto
```

Returns a project status by its identifier.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKey
$config = Aurigma\BackOffice\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Aurigma\BackOffice\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');

// Configure OAuth2 access token for authorization: OAuth2ClientCredentials
$config = Aurigma\BackOffice\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

// Configure OAuth2 access token for authorization: OAuth2Implicit
$config = Aurigma\BackOffice\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

// Configure API key authorization: Bearer
$config = Aurigma\BackOffice\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Aurigma\BackOffice\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new Aurigma\BackOffice\Api\ProjectStatusesManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | Status identifier.
$tenant_id = 56; // int | Tenant identifier.

try {
    $result = $apiInstance->projectStatusesManagementGet($id, $tenant_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProjectStatusesManagementApi->projectStatusesManagementGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **int**| Status identifier. | |
| **tenant_id** | **int**| Tenant identifier. | [optional] |

### Return type

[**\Aurigma\BackOffice\Model\ProjectStatusDto**](../Model/ProjectStatusDto.md)

### Authorization

[ApiKey](../../README.md#ApiKey), [OAuth2ClientCredentials](../../README.md#OAuth2ClientCredentials), [OAuth2Implicit](../../README.md#OAuth2Implicit), [Bearer](../../README.md#Bearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `projectStatusesManagementGetAll()`

```php
projectStatusesManagementGetAll($tenant_id): \Aurigma\BackOffice\Model\PagedOfProjectStatusDto
```

Returns a list of all existing project statuses.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKey
$config = Aurigma\BackOffice\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Aurigma\BackOffice\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');

// Configure OAuth2 access token for authorization: OAuth2ClientCredentials
$config = Aurigma\BackOffice\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

// Configure OAuth2 access token for authorization: OAuth2Implicit
$config = Aurigma\BackOffice\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

// Configure API key authorization: Bearer
$config = Aurigma\BackOffice\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Aurigma\BackOffice\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new Aurigma\BackOffice\Api\ProjectStatusesManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenant_id = 56; // int | Tenant identifier.

try {
    $result = $apiInstance->projectStatusesManagementGetAll($tenant_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProjectStatusesManagementApi->projectStatusesManagementGetAll: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenant_id** | **int**| Tenant identifier. | [optional] |

### Return type

[**\Aurigma\BackOffice\Model\PagedOfProjectStatusDto**](../Model/PagedOfProjectStatusDto.md)

### Authorization

[ApiKey](../../README.md#ApiKey), [OAuth2ClientCredentials](../../README.md#OAuth2ClientCredentials), [OAuth2Implicit](../../README.md#OAuth2Implicit), [Bearer](../../README.md#Bearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `projectStatusesManagementUpdate()`

```php
projectStatusesManagementUpdate($id, $tenant_id, $project_statuses_management_update_request): \Aurigma\BackOffice\Model\ProjectStatusDto
```

Updates an existing project status and returns its description.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKey
$config = Aurigma\BackOffice\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Aurigma\BackOffice\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');

// Configure OAuth2 access token for authorization: OAuth2ClientCredentials
$config = Aurigma\BackOffice\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

// Configure OAuth2 access token for authorization: OAuth2Implicit
$config = Aurigma\BackOffice\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

// Configure API key authorization: Bearer
$config = Aurigma\BackOffice\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Aurigma\BackOffice\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new Aurigma\BackOffice\Api\ProjectStatusesManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | Status identifier.
$tenant_id = 56; // int | Tenant identifier.
$project_statuses_management_update_request = new \Aurigma\BackOffice\Model\ProjectStatusesManagementUpdateRequest(); // \Aurigma\BackOffice\Model\ProjectStatusesManagementUpdateRequest | Status update parameters.

try {
    $result = $apiInstance->projectStatusesManagementUpdate($id, $tenant_id, $project_statuses_management_update_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProjectStatusesManagementApi->projectStatusesManagementUpdate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **int**| Status identifier. | |
| **tenant_id** | **int**| Tenant identifier. | [optional] |
| **project_statuses_management_update_request** | [**\Aurigma\BackOffice\Model\ProjectStatusesManagementUpdateRequest**](../Model/ProjectStatusesManagementUpdateRequest.md)| Status update parameters. | [optional] |

### Return type

[**\Aurigma\BackOffice\Model\ProjectStatusDto**](../Model/ProjectStatusDto.md)

### Authorization

[ApiKey](../../README.md#ApiKey), [OAuth2ClientCredentials](../../README.md#OAuth2ClientCredentials), [OAuth2Implicit](../../README.md#OAuth2Implicit), [Bearer](../../README.md#Bearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
