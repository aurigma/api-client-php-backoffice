# Aurigma\BackOffice\ProjectStatusTransitionsManagementApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**projectStatusTransitionsManagementCreate()**](ProjectStatusTransitionsManagementApi.md#projectStatusTransitionsManagementCreate) | **POST** /api/backoffice/v1/projects-transitions/transitions | Creates a new project status transition and returns its description. |
| [**projectStatusTransitionsManagementDelete()**](ProjectStatusTransitionsManagementApi.md#projectStatusTransitionsManagementDelete) | **DELETE** /api/backoffice/v1/projects-transitions/{id} | Deletes an existing project status transition and returns its description. |
| [**projectStatusTransitionsManagementGet()**](ProjectStatusTransitionsManagementApi.md#projectStatusTransitionsManagementGet) | **GET** /api/backoffice/v1/projects-transitions/{id} | Returns a project status transition by its identifier. |
| [**projectStatusTransitionsManagementGetAll()**](ProjectStatusTransitionsManagementApi.md#projectStatusTransitionsManagementGetAll) | **GET** /api/backoffice/v1/projects-transitions | Returns a list of all existing project status transitions. |
| [**projectStatusTransitionsManagementUpdate()**](ProjectStatusTransitionsManagementApi.md#projectStatusTransitionsManagementUpdate) | **PUT** /api/backoffice/v1/projects-transitions/{id} | Updates an existing project status transition and returns its description. |


## `projectStatusTransitionsManagementCreate()`

```php
projectStatusTransitionsManagementCreate($tenant_id, $project_status_transitions_management_create_request): \Aurigma\BackOffice\Model\ProjectStatusTransitionDto
```

Creates a new project status transition and returns its description.

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


$apiInstance = new Aurigma\BackOffice\Api\ProjectStatusTransitionsManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenant_id = 56; // int | Tenant identifier.
$project_status_transitions_management_create_request = new \Aurigma\BackOffice\Model\ProjectStatusTransitionsManagementCreateRequest(); // \Aurigma\BackOffice\Model\ProjectStatusTransitionsManagementCreateRequest | Status transition creation parameters.

try {
    $result = $apiInstance->projectStatusTransitionsManagementCreate($tenant_id, $project_status_transitions_management_create_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProjectStatusTransitionsManagementApi->projectStatusTransitionsManagementCreate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenant_id** | **int**| Tenant identifier. | [optional] |
| **project_status_transitions_management_create_request** | [**\Aurigma\BackOffice\Model\ProjectStatusTransitionsManagementCreateRequest**](../Model/ProjectStatusTransitionsManagementCreateRequest.md)| Status transition creation parameters. | [optional] |

### Return type

[**\Aurigma\BackOffice\Model\ProjectStatusTransitionDto**](../Model/ProjectStatusTransitionDto.md)

### Authorization

[ApiKey](../../README.md#ApiKey), [OAuth2ClientCredentials](../../README.md#OAuth2ClientCredentials), [OAuth2Implicit](../../README.md#OAuth2Implicit), [Bearer](../../README.md#Bearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `projectStatusTransitionsManagementDelete()`

```php
projectStatusTransitionsManagementDelete($id, $tenant_id): \Aurigma\BackOffice\Model\ProjectStatusTransitionDto
```

Deletes an existing project status transition and returns its description.

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


$apiInstance = new Aurigma\BackOffice\Api\ProjectStatusTransitionsManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | Status transition identifier.
$tenant_id = 56; // int | Tenant identifier.

try {
    $result = $apiInstance->projectStatusTransitionsManagementDelete($id, $tenant_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProjectStatusTransitionsManagementApi->projectStatusTransitionsManagementDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **int**| Status transition identifier. | |
| **tenant_id** | **int**| Tenant identifier. | [optional] |

### Return type

[**\Aurigma\BackOffice\Model\ProjectStatusTransitionDto**](../Model/ProjectStatusTransitionDto.md)

### Authorization

[ApiKey](../../README.md#ApiKey), [OAuth2ClientCredentials](../../README.md#OAuth2ClientCredentials), [OAuth2Implicit](../../README.md#OAuth2Implicit), [Bearer](../../README.md#Bearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `projectStatusTransitionsManagementGet()`

```php
projectStatusTransitionsManagementGet($id, $tenant_id): \Aurigma\BackOffice\Model\ProjectStatusTransitionDto
```

Returns a project status transition by its identifier.

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


$apiInstance = new Aurigma\BackOffice\Api\ProjectStatusTransitionsManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | Status transition identifier.
$tenant_id = 56; // int | Tenant identifier.

try {
    $result = $apiInstance->projectStatusTransitionsManagementGet($id, $tenant_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProjectStatusTransitionsManagementApi->projectStatusTransitionsManagementGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **int**| Status transition identifier. | |
| **tenant_id** | **int**| Tenant identifier. | [optional] |

### Return type

[**\Aurigma\BackOffice\Model\ProjectStatusTransitionDto**](../Model/ProjectStatusTransitionDto.md)

### Authorization

[ApiKey](../../README.md#ApiKey), [OAuth2ClientCredentials](../../README.md#OAuth2ClientCredentials), [OAuth2Implicit](../../README.md#OAuth2Implicit), [Bearer](../../README.md#Bearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `projectStatusTransitionsManagementGetAll()`

```php
projectStatusTransitionsManagementGetAll($tenant_id): \Aurigma\BackOffice\Model\PagedOfProjectStatusTransitionDto
```

Returns a list of all existing project status transitions.

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


$apiInstance = new Aurigma\BackOffice\Api\ProjectStatusTransitionsManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenant_id = 56; // int | Tenant identifier.

try {
    $result = $apiInstance->projectStatusTransitionsManagementGetAll($tenant_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProjectStatusTransitionsManagementApi->projectStatusTransitionsManagementGetAll: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenant_id** | **int**| Tenant identifier. | [optional] |

### Return type

[**\Aurigma\BackOffice\Model\PagedOfProjectStatusTransitionDto**](../Model/PagedOfProjectStatusTransitionDto.md)

### Authorization

[ApiKey](../../README.md#ApiKey), [OAuth2ClientCredentials](../../README.md#OAuth2ClientCredentials), [OAuth2Implicit](../../README.md#OAuth2Implicit), [Bearer](../../README.md#Bearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `projectStatusTransitionsManagementUpdate()`

```php
projectStatusTransitionsManagementUpdate($id, $tenant_id, $project_status_transitions_management_update_request): \Aurigma\BackOffice\Model\ProjectStatusTransitionDto
```

Updates an existing project status transition and returns its description.

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


$apiInstance = new Aurigma\BackOffice\Api\ProjectStatusTransitionsManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | Status transition identifier.
$tenant_id = 56; // int | Tenant identifier.
$project_status_transitions_management_update_request = new \Aurigma\BackOffice\Model\ProjectStatusTransitionsManagementUpdateRequest(); // \Aurigma\BackOffice\Model\ProjectStatusTransitionsManagementUpdateRequest | Status transition update parameters.

try {
    $result = $apiInstance->projectStatusTransitionsManagementUpdate($id, $tenant_id, $project_status_transitions_management_update_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProjectStatusTransitionsManagementApi->projectStatusTransitionsManagementUpdate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **int**| Status transition identifier. | |
| **tenant_id** | **int**| Tenant identifier. | [optional] |
| **project_status_transitions_management_update_request** | [**\Aurigma\BackOffice\Model\ProjectStatusTransitionsManagementUpdateRequest**](../Model/ProjectStatusTransitionsManagementUpdateRequest.md)| Status transition update parameters. | [optional] |

### Return type

[**\Aurigma\BackOffice\Model\ProjectStatusTransitionDto**](../Model/ProjectStatusTransitionDto.md)

### Authorization

[ApiKey](../../README.md#ApiKey), [OAuth2ClientCredentials](../../README.md#OAuth2ClientCredentials), [OAuth2Implicit](../../README.md#OAuth2Implicit), [Bearer](../../README.md#Bearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
