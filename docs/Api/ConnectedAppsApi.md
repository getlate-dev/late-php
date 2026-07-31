# Zernio\ConnectedAppsApi



All URIs are relative to https://zernio.com/api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**listConnectedApps()**](ConnectedAppsApi.md#listConnectedApps) | **GET** /v1/me/connected-apps | List connected apps |
| [**revokeConnectedApp()**](ConnectedAppsApi.md#revokeConnectedApp) | **DELETE** /v1/me/connected-apps/{clientId} | Revoke connected app |


## `listConnectedApps()`

```php
listConnectedApps(): \Zernio\Model\ListConnectedApps200Response
```

List connected apps

Returns the OAuth clients (AI assistants and MCP connectors) the authenticated user has authorized and that still hold a live token.  Requires a session or a full-scope API key. A profile-scoped API key or an OAuth access token is rejected with 403: an app must not be able to enumerate its sibling authorizations.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Zernio\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Zernio\Api\ConnectedAppsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->listConnectedApps();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConnectedAppsApi->listConnectedApps: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\Zernio\Model\ListConnectedApps200Response**](../Model/ListConnectedApps200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `revokeConnectedApp()`

```php
revokeConnectedApp($client_id): \Zernio\Model\RevokeConnectedApp200Response
```

Revoke connected app

Ends an app's access: invalidates the client's pending authorization codes and revokes every live token it holds for the authenticated user. Takes effect on the app's next request.  Idempotent while the authorization is still on record: revoking an app that was already revoked returns 200 with `revokedTokens: 0`.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Zernio\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Zernio\Api\ConnectedAppsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$client_id = 'client_id_example'; // string | OAuth client id, as returned by GET /v1/me/connected-apps.

try {
    $result = $apiInstance->revokeConnectedApp($client_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConnectedAppsApi->revokeConnectedApp: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **client_id** | **string**| OAuth client id, as returned by GET /v1/me/connected-apps. | |

### Return type

[**\Zernio\Model\RevokeConnectedApp200Response**](../Model/RevokeConnectedApp200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
