# Late\ProfilesApi



All URIs are relative to https://getlate.dev/api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createProfile()**](ProfilesApi.md#createProfile) | **POST** /v1/profiles | Create a new profile |
| [**deleteProfile()**](ProfilesApi.md#deleteProfile) | **DELETE** /v1/profiles/{profileId} | Delete a profile (must have no connected accounts) |
| [**getProfile()**](ProfilesApi.md#getProfile) | **GET** /v1/profiles/{profileId} | Get a profile by id |
| [**listProfiles()**](ProfilesApi.md#listProfiles) | **GET** /v1/profiles | List profiles visible to the authenticated user |
| [**updateProfile()**](ProfilesApi.md#updateProfile) | **PUT** /v1/profiles/{profileId} | Update a profile |


## `createProfile()`

```php
createProfile($create_profile_request): \Late\Model\ProfileCreateResponse
```

Create a new profile

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Late\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Late\Api\ProfilesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$create_profile_request = {"name":"Marketing Team","description":"Profile for marketing campaigns","color":"#4CAF50"}; // \Late\Model\CreateProfileRequest

try {
    $result = $apiInstance->createProfile($create_profile_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProfilesApi->createProfile: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **create_profile_request** | [**\Late\Model\CreateProfileRequest**](../Model/CreateProfileRequest.md)|  | |

### Return type

[**\Late\Model\ProfileCreateResponse**](../Model/ProfileCreateResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteProfile()`

```php
deleteProfile($profile_id): \Late\Model\DeleteAccountGroup200Response
```

Delete a profile (must have no connected accounts)

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Late\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Late\Api\ProfilesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$profile_id = 'profile_id_example'; // string

try {
    $result = $apiInstance->deleteProfile($profile_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProfilesApi->deleteProfile: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **profile_id** | **string**|  | |

### Return type

[**\Late\Model\DeleteAccountGroup200Response**](../Model/DeleteAccountGroup200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getProfile()`

```php
getProfile($profile_id): \Late\Model\GetProfile200Response
```

Get a profile by id

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Late\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Late\Api\ProfilesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$profile_id = 'profile_id_example'; // string

try {
    $result = $apiInstance->getProfile($profile_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProfilesApi->getProfile: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **profile_id** | **string**|  | |

### Return type

[**\Late\Model\GetProfile200Response**](../Model/GetProfile200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listProfiles()`

```php
listProfiles($include_over_limit): \Late\Model\ProfilesListResponse
```

List profiles visible to the authenticated user

Returns profiles within the user's plan limit. Profiles are sorted by creation date (oldest first). Use `includeOverLimit=true` to include profiles that exceed the plan limit (for management/deletion purposes).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Late\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Late\Api\ProfilesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$include_over_limit = false; // bool | When true, includes profiles that exceed the user's plan limit. Over-limit profiles will have `isOverLimit: true` in the response. Useful for managing/deleting profiles after a plan downgrade.

try {
    $result = $apiInstance->listProfiles($include_over_limit);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProfilesApi->listProfiles: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **include_over_limit** | **bool**| When true, includes profiles that exceed the user&#39;s plan limit. Over-limit profiles will have &#x60;isOverLimit: true&#x60; in the response. Useful for managing/deleting profiles after a plan downgrade. | [optional] [default to false] |

### Return type

[**\Late\Model\ProfilesListResponse**](../Model/ProfilesListResponse.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateProfile()`

```php
updateProfile($profile_id, $update_profile_request): \Late\Model\UpdateProfile200Response
```

Update a profile

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Late\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Late\Api\ProfilesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$profile_id = 'profile_id_example'; // string
$update_profile_request = {"name":"Marketing Team (Updated)","color":"#2196F3","isDefault":true}; // \Late\Model\UpdateProfileRequest

try {
    $result = $apiInstance->updateProfile($profile_id, $update_profile_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProfilesApi->updateProfile: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **profile_id** | **string**|  | |
| **update_profile_request** | [**\Late\Model\UpdateProfileRequest**](../Model/UpdateProfileRequest.md)|  | |

### Return type

[**\Late\Model\UpdateProfile200Response**](../Model/UpdateProfile200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
