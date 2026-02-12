# Late\ConnectApi



All URIs are relative to https://getlate.dev/api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**completeTelegramConnect()**](ConnectApi.md#completeTelegramConnect) | **PATCH** /v1/connect/telegram | Check Telegram connection status |
| [**connectBlueskyCredentials()**](ConnectApi.md#connectBlueskyCredentials) | **POST** /v1/connect/bluesky/credentials | Connect Bluesky using app password |
| [**getConnectUrl()**](ConnectApi.md#getConnectUrl) | **GET** /v1/connect/{platform} | Start OAuth connection for a platform |
| [**getFacebookPages()**](ConnectApi.md#getFacebookPages) | **GET** /v1/accounts/{accountId}/facebook-page | List available Facebook pages for a connected account |
| [**getGmbLocations()**](ConnectApi.md#getGmbLocations) | **GET** /v1/accounts/{accountId}/gmb-locations | List available Google Business Profile locations for a connected account |
| [**getLinkedInOrganizations()**](ConnectApi.md#getLinkedInOrganizations) | **GET** /v1/accounts/{accountId}/linkedin-organizations | Get available LinkedIn organizations for a connected account |
| [**getPendingOAuthData()**](ConnectApi.md#getPendingOAuthData) | **GET** /v1/connect/pending-data | Fetch pending OAuth selection data (Headless Mode) |
| [**getPinterestBoards()**](ConnectApi.md#getPinterestBoards) | **GET** /v1/accounts/{accountId}/pinterest-boards | List Pinterest boards for a connected account |
| [**getRedditFlairs()**](ConnectApi.md#getRedditFlairs) | **GET** /v1/accounts/{accountId}/reddit-flairs | List available post flairs for a Reddit subreddit |
| [**getRedditSubreddits()**](ConnectApi.md#getRedditSubreddits) | **GET** /v1/accounts/{accountId}/reddit-subreddits | List Reddit subreddits for a connected account |
| [**getTelegramConnectStatus()**](ConnectApi.md#getTelegramConnectStatus) | **GET** /v1/connect/telegram | Generate Telegram access code |
| [**handleOAuthCallback()**](ConnectApi.md#handleOAuthCallback) | **POST** /v1/connect/{platform} | Complete OAuth token exchange manually (for server-side flows) |
| [**initiateTelegramConnect()**](ConnectApi.md#initiateTelegramConnect) | **POST** /v1/connect/telegram | Direct Telegram connection (power users) |
| [**listFacebookPages()**](ConnectApi.md#listFacebookPages) | **GET** /v1/connect/facebook/select-page | List Facebook Pages after OAuth (Headless Mode) |
| [**listGoogleBusinessLocations()**](ConnectApi.md#listGoogleBusinessLocations) | **GET** /v1/connect/googlebusiness/locations | List Google Business Locations after OAuth (Headless Mode) |
| [**listLinkedInOrganizations()**](ConnectApi.md#listLinkedInOrganizations) | **GET** /v1/connect/linkedin/organizations | Fetch full LinkedIn organization details (Headless Mode) |
| [**listPinterestBoardsForSelection()**](ConnectApi.md#listPinterestBoardsForSelection) | **GET** /v1/connect/pinterest/select-board | List Pinterest Boards after OAuth (Headless Mode) |
| [**listSnapchatProfiles()**](ConnectApi.md#listSnapchatProfiles) | **GET** /v1/connect/snapchat/select-profile | List Snapchat Public Profiles after OAuth (Headless Mode) |
| [**selectFacebookPage()**](ConnectApi.md#selectFacebookPage) | **POST** /v1/connect/facebook/select-page | Select a Facebook Page to complete the connection (Headless Mode) |
| [**selectGoogleBusinessLocation()**](ConnectApi.md#selectGoogleBusinessLocation) | **POST** /v1/connect/googlebusiness/select-location | Select a Google Business location to complete the connection (Headless Mode) |
| [**selectLinkedInOrganization()**](ConnectApi.md#selectLinkedInOrganization) | **POST** /v1/connect/linkedin/select-organization | Select LinkedIn organization or personal account after OAuth |
| [**selectPinterestBoard()**](ConnectApi.md#selectPinterestBoard) | **POST** /v1/connect/pinterest/select-board | Select a Pinterest Board to complete the connection (Headless Mode) |
| [**selectSnapchatProfile()**](ConnectApi.md#selectSnapchatProfile) | **POST** /v1/connect/snapchat/select-profile | Select a Snapchat Public Profile to complete the connection (Headless Mode) |
| [**updateFacebookPage()**](ConnectApi.md#updateFacebookPage) | **PUT** /v1/accounts/{accountId}/facebook-page | Update selected Facebook page for a connected account |
| [**updateGmbLocation()**](ConnectApi.md#updateGmbLocation) | **PUT** /v1/accounts/{accountId}/gmb-locations | Update selected Google Business Profile location for a connected account |
| [**updateLinkedInOrganization()**](ConnectApi.md#updateLinkedInOrganization) | **PUT** /v1/accounts/{accountId}/linkedin-organization | Switch LinkedIn account type (personal/organization) |
| [**updatePinterestBoards()**](ConnectApi.md#updatePinterestBoards) | **PUT** /v1/accounts/{accountId}/pinterest-boards | Set default Pinterest board on the connection |
| [**updateRedditSubreddits()**](ConnectApi.md#updateRedditSubreddits) | **PUT** /v1/accounts/{accountId}/reddit-subreddits | Set default subreddit on the connection |


## `completeTelegramConnect()`

```php
completeTelegramConnect($code): \Late\Model\CompleteTelegramConnect200Response
```

Check Telegram connection status

Poll this endpoint to check if a Telegram access code has been used to connect a channel/group.  **Recommended polling interval:** 3 seconds  **Status values:** - `pending`: Code is valid, waiting for user to complete connection - `connected`: Connection successful - channel/group is now linked - `expired`: Code has expired, generate a new one

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Late\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Late\Api\ConnectApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$code = LATE-ABC123; // string | The access code to check status for

try {
    $result = $apiInstance->completeTelegramConnect($code);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConnectApi->completeTelegramConnect: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **code** | **string**| The access code to check status for | |

### Return type

[**\Late\Model\CompleteTelegramConnect200Response**](../Model/CompleteTelegramConnect200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `connectBlueskyCredentials()`

```php
connectBlueskyCredentials($connect_bluesky_credentials_request): \Late\Model\ConnectBlueskyCredentials200Response
```

Connect Bluesky using app password

Connect a Bluesky account using identifier (handle or email) and an app password.  To get your userId for the state parameter, call `GET /v1/users` - the response includes a `currentUserId` field.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Late\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Late\Api\ConnectApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$connect_bluesky_credentials_request = {"identifier":"yourhandle.bsky.social","appPassword":"xxxx-xxxx-xxxx-xxxx","state":"6507a1b2c3d4e5f6a7b8c9d0-6507a1b2c3d4e5f6a7b8c9d1","redirectUri":"https://yourapp.com/connected"}; // \Late\Model\ConnectBlueskyCredentialsRequest

try {
    $result = $apiInstance->connectBlueskyCredentials($connect_bluesky_credentials_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConnectApi->connectBlueskyCredentials: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **connect_bluesky_credentials_request** | [**\Late\Model\ConnectBlueskyCredentialsRequest**](../Model/ConnectBlueskyCredentialsRequest.md)|  | |

### Return type

[**\Late\Model\ConnectBlueskyCredentials200Response**](../Model/ConnectBlueskyCredentials200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getConnectUrl()`

```php
getConnectUrl($platform, $profile_id, $redirect_url): \Late\Model\GetConnectUrl200Response
```

Start OAuth connection for a platform

Initiate an OAuth connection flow for any supported social media platform.  **Standard Flow (Hosted UI):** For Facebook connections, Late hosts the page selection UI:  1. Call this endpoint with your API key and `redirect_url` (optional) 2. Redirect your user to the returned `authUrl` 3. After OAuth, the user is redirected to Late’s hosted page selector at      `/connect/facebook/select-page?profileId=X&tempToken=Y&userProfile=Z&redirect_url=YOUR_URL&connect_token=CT` 4. After they pick a page, Late saves the connection and finally redirects to your `redirect_url` (if provided)  **Headless/Whitelabel Mode (Facebook, LinkedIn, Pinterest & Google Business Profile):** Build your own fully branded selection UI while Late handles OAuth:  **Facebook:** 1. Call this endpoint with your API key and add `&headless=true`, e.g.      `GET /v1/connect/facebook?profileId=PROFILE_ID&redirect_url=https://yourapp.com/callback&headless=true` 2. Redirect your user to the returned `authUrl` 3. After OAuth, the user is redirected directly to **your** `redirect_url` with:    - `profileId` – your Late profile ID      - `tempToken` – temporary Facebook access token      - `userProfile` – URL‑encoded JSON user profile      - `connect_token` – short‑lived connect token (for API auth)      - `platform=facebook`      - `step=select_page` 4. Use `tempToken`, `userProfile`, and the `X-Connect-Token` header with:    - `GET /v1/connect/facebook/select-page` to fetch pages    - `POST /v1/connect/facebook/select-page` to save the selected page 5. In this mode, users never see Late's hosted page selector – only your UI.  **LinkedIn:** 1. Call this endpoint with `&headless=true`, e.g.    `GET /v1/connect/linkedin?profileId=PROFILE_ID&redirect_url=https://yourapp.com/callback&headless=true` 2. Redirect your user to the returned `authUrl` 3. After OAuth, the user is redirected directly to **your** `redirect_url` with:    - `profileId` – your Late profile ID    - `pendingDataToken` – token to fetch OAuth data via API (see step 4)    - `connect_token` – short-lived connect token (for API auth)    - `platform=linkedin`    - `step=select_organization` 4. Call `GET /v1/connect/pending-data?token=PENDING_DATA_TOKEN` to fetch the OAuth data:    - `tempToken` – temporary LinkedIn access token    - `userProfile` – JSON object with `id`, `username`, `displayName`, `profilePicture`    - `organizations` – JSON array with `id`, `urn`, `name`, `vanityName` for each org    - `refreshToken` / `expiresIn` – token metadata    This endpoint is one-time use and data expires after 10 minutes. 5. **Optional:** To fetch full organization details (logos, website, industry, description), call `GET /v1/connect/linkedin/organizations?tempToken=X&orgIds=id1,id2,...` 6. Call `POST /v1/connect/linkedin/select-organization` with the `X-Connect-Token` header to save the selection. 7. In this mode, users never see Late's hosted organization selector – only your UI. 8. Note: If the user has no organization admin access, `step=select_organization` will NOT be present,    and the account will be connected directly as a personal account.  **Pinterest:** 1. Call this endpoint with `&headless=true`, e.g.    `GET /v1/connect/pinterest?profileId=PROFILE_ID&redirect_url=https://yourapp.com/callback&headless=true` 2. Redirect your user to the returned `authUrl` 3. After OAuth, the user is redirected directly to **your** `redirect_url` with:    - `profileId` – your Late profile ID    - `tempToken` – temporary Pinterest access token    - `userProfile` – URL‑encoded JSON user profile    - `connect_token` – short‑lived connect token (for API auth)    - `platform=pinterest`    - `step=select_board` 4. Use `tempToken`, `userProfile`, and the `X-Connect-Token` header with:    - `GET /v1/connect/pinterest/select-board` to fetch boards    - `POST /v1/connect/pinterest/select-board` to save the selected board 5. In this mode, users never see Late's hosted board selector – only your UI.  **Google Business Profile:** 1. Call this endpoint with `&headless=true`, e.g.    `GET /v1/connect/googlebusiness?profileId=PROFILE_ID&redirect_url=https://yourapp.com/callback&headless=true` 2. Redirect your user to the returned `authUrl` 3. After OAuth, the user is redirected directly to **your** `redirect_url` with:    - `profileId` – your Late profile ID    - `tempToken` – temporary Google access token    - `userProfile` – URL‑encoded JSON user profile (includes refresh token info)    - `connect_token` – short‑lived connect token (for API auth)    - `platform=googlebusiness`    - `step=select_location` 4. Use `tempToken`, `userProfile`, and the `X-Connect-Token` header with:    - `GET /v1/connect/googlebusiness/locations` to fetch business locations    - `POST /v1/connect/googlebusiness/select-location` to save the selected location 5. In this mode, users never see Late's hosted location selector – only your UI.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Late\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Late\Api\ConnectApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$platform = 'platform_example'; // string | Social media platform to connect
$profile_id = 'profile_id_example'; // string | Your Late profile ID (get from /v1/profiles)
$redirect_url = 'redirect_url_example'; // string | Optional: Your custom redirect URL after connection completes.  **Standard Mode:** Omit `headless=true` to use our hosted page selection UI.   After the user selects a Facebook Page, Late redirects here with:   `?connected=facebook&profileId=X&username=Y`  **Headless Mode (Facebook, LinkedIn, Pinterest, Google Business Profile & Snapchat):** Pass `headless=true` as a query parameter on this endpoint (not inside `redirect_url`), e.g.: `GET /v1/connect/facebook?profileId=PROFILE_ID&redirect_url=https://yourapp.com/callback&headless=true` `GET /v1/connect/linkedin?profileId=PROFILE_ID&redirect_url=https://yourapp.com/callback&headless=true` `GET /v1/connect/pinterest?profileId=PROFILE_ID&redirect_url=https://yourapp.com/callback&headless=true` `GET /v1/connect/googlebusiness?profileId=PROFILE_ID&redirect_url=https://yourapp.com/callback&headless=true` `GET /v1/connect/snapchat?profileId=PROFILE_ID&redirect_url=https://yourapp.com/callback&headless=true`  After OAuth, the user is redirected directly to your `redirect_url` with OAuth data: - **Facebook:** `?profileId=X&tempToken=Y&userProfile=Z&connect_token=CT&platform=facebook&step=select_page` - **LinkedIn:** `?profileId=X&pendingDataToken=TOKEN&connect_token=CT&platform=linkedin&step=select_organization`   Use `GET /v1/connect/pending-data?token=TOKEN` to fetch tempToken, userProfile, organizations, refreshToken. - **Pinterest:** `?profileId=X&tempToken=Y&userProfile=Z&connect_token=CT&platform=pinterest&step=select_board` - **Google Business:** `?profileId=X&tempToken=Y&userProfile=Z&connect_token=CT&platform=googlebusiness&step=select_location` - **Snapchat:** `?profileId=X&tempToken=Y&userProfile=Z&publicProfiles=PROFILES&connect_token=CT&platform=snapchat&step=select_public_profile`   (publicProfiles contains `id`, `display_name`, `username`, `profile_image_url`, `subscriber_count`)  Then use the respective endpoints to build your custom UI: - Facebook: `/v1/connect/facebook/select-page` (GET to fetch, POST to save) - LinkedIn: `/v1/connect/linkedin/organizations` (GET to fetch logos), `/v1/connect/linkedin/select-organization` (POST to save) - Pinterest: `/v1/connect/pinterest/select-board` (GET to fetch, POST to save) - Google Business: `/v1/connect/googlebusiness/locations` (GET) and `/v1/connect/googlebusiness/select-location` (POST) - Snapchat: `/v1/connect/snapchat/select-profile` (POST to save selected public profile)  Example: `https://yourdomain.com/integrations/callback`

try {
    $result = $apiInstance->getConnectUrl($platform, $profile_id, $redirect_url);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConnectApi->getConnectUrl: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **platform** | **string**| Social media platform to connect | |
| **profile_id** | **string**| Your Late profile ID (get from /v1/profiles) | |
| **redirect_url** | **string**| Optional: Your custom redirect URL after connection completes.  **Standard Mode:** Omit &#x60;headless&#x3D;true&#x60; to use our hosted page selection UI.   After the user selects a Facebook Page, Late redirects here with:   &#x60;?connected&#x3D;facebook&amp;profileId&#x3D;X&amp;username&#x3D;Y&#x60;  **Headless Mode (Facebook, LinkedIn, Pinterest, Google Business Profile &amp; Snapchat):** Pass &#x60;headless&#x3D;true&#x60; as a query parameter on this endpoint (not inside &#x60;redirect_url&#x60;), e.g.: &#x60;GET /v1/connect/facebook?profileId&#x3D;PROFILE_ID&amp;redirect_url&#x3D;https://yourapp.com/callback&amp;headless&#x3D;true&#x60; &#x60;GET /v1/connect/linkedin?profileId&#x3D;PROFILE_ID&amp;redirect_url&#x3D;https://yourapp.com/callback&amp;headless&#x3D;true&#x60; &#x60;GET /v1/connect/pinterest?profileId&#x3D;PROFILE_ID&amp;redirect_url&#x3D;https://yourapp.com/callback&amp;headless&#x3D;true&#x60; &#x60;GET /v1/connect/googlebusiness?profileId&#x3D;PROFILE_ID&amp;redirect_url&#x3D;https://yourapp.com/callback&amp;headless&#x3D;true&#x60; &#x60;GET /v1/connect/snapchat?profileId&#x3D;PROFILE_ID&amp;redirect_url&#x3D;https://yourapp.com/callback&amp;headless&#x3D;true&#x60;  After OAuth, the user is redirected directly to your &#x60;redirect_url&#x60; with OAuth data: - **Facebook:** &#x60;?profileId&#x3D;X&amp;tempToken&#x3D;Y&amp;userProfile&#x3D;Z&amp;connect_token&#x3D;CT&amp;platform&#x3D;facebook&amp;step&#x3D;select_page&#x60; - **LinkedIn:** &#x60;?profileId&#x3D;X&amp;pendingDataToken&#x3D;TOKEN&amp;connect_token&#x3D;CT&amp;platform&#x3D;linkedin&amp;step&#x3D;select_organization&#x60;   Use &#x60;GET /v1/connect/pending-data?token&#x3D;TOKEN&#x60; to fetch tempToken, userProfile, organizations, refreshToken. - **Pinterest:** &#x60;?profileId&#x3D;X&amp;tempToken&#x3D;Y&amp;userProfile&#x3D;Z&amp;connect_token&#x3D;CT&amp;platform&#x3D;pinterest&amp;step&#x3D;select_board&#x60; - **Google Business:** &#x60;?profileId&#x3D;X&amp;tempToken&#x3D;Y&amp;userProfile&#x3D;Z&amp;connect_token&#x3D;CT&amp;platform&#x3D;googlebusiness&amp;step&#x3D;select_location&#x60; - **Snapchat:** &#x60;?profileId&#x3D;X&amp;tempToken&#x3D;Y&amp;userProfile&#x3D;Z&amp;publicProfiles&#x3D;PROFILES&amp;connect_token&#x3D;CT&amp;platform&#x3D;snapchat&amp;step&#x3D;select_public_profile&#x60;   (publicProfiles contains &#x60;id&#x60;, &#x60;display_name&#x60;, &#x60;username&#x60;, &#x60;profile_image_url&#x60;, &#x60;subscriber_count&#x60;)  Then use the respective endpoints to build your custom UI: - Facebook: &#x60;/v1/connect/facebook/select-page&#x60; (GET to fetch, POST to save) - LinkedIn: &#x60;/v1/connect/linkedin/organizations&#x60; (GET to fetch logos), &#x60;/v1/connect/linkedin/select-organization&#x60; (POST to save) - Pinterest: &#x60;/v1/connect/pinterest/select-board&#x60; (GET to fetch, POST to save) - Google Business: &#x60;/v1/connect/googlebusiness/locations&#x60; (GET) and &#x60;/v1/connect/googlebusiness/select-location&#x60; (POST) - Snapchat: &#x60;/v1/connect/snapchat/select-profile&#x60; (POST to save selected public profile)  Example: &#x60;https://yourdomain.com/integrations/callback&#x60; | [optional] |

### Return type

[**\Late\Model\GetConnectUrl200Response**](../Model/GetConnectUrl200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getFacebookPages()`

```php
getFacebookPages($account_id): \Late\Model\GetFacebookPages200Response
```

List available Facebook pages for a connected account

Returns all Facebook pages the connected account has access to, including the currently selected page.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Late\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Late\Api\ConnectApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string

try {
    $result = $apiInstance->getFacebookPages($account_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConnectApi->getFacebookPages: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**|  | |

### Return type

[**\Late\Model\GetFacebookPages200Response**](../Model/GetFacebookPages200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getGmbLocations()`

```php
getGmbLocations($account_id): \Late\Model\GetGmbLocations200Response
```

List available Google Business Profile locations for a connected account

Returns all Google Business Profile locations the connected account has access to, including the currently selected location.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Late\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Late\Api\ConnectApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string

try {
    $result = $apiInstance->getGmbLocations($account_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConnectApi->getGmbLocations: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**|  | |

### Return type

[**\Late\Model\GetGmbLocations200Response**](../Model/GetGmbLocations200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getLinkedInOrganizations()`

```php
getLinkedInOrganizations($account_id): \Late\Model\GetLinkedInOrganizations200Response
```

Get available LinkedIn organizations for a connected account

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Late\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Late\Api\ConnectApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string

try {
    $result = $apiInstance->getLinkedInOrganizations($account_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConnectApi->getLinkedInOrganizations: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**|  | |

### Return type

[**\Late\Model\GetLinkedInOrganizations200Response**](../Model/GetLinkedInOrganizations200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getPendingOAuthData()`

```php
getPendingOAuthData($token): \Late\Model\GetPendingOAuthData200Response
```

Fetch pending OAuth selection data (Headless Mode)

**Fetch Pending OAuth Data for Headless Mode**  In headless mode, platforms like LinkedIn store OAuth selection data (organizations, pages, etc.) in the database instead of passing it via URL parameters. This prevents URI_TOO_LONG errors when users have many organizations/pages to select from.  After OAuth redirect, use the `pendingDataToken` from the URL to fetch the stored data.  **Important:** - This endpoint is one-time use: data is deleted after being fetched - Data expires automatically after 10 minutes if not fetched - No authentication required, just the token from the redirect URL

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Late\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Late\Api\ConnectApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$token = 'token_example'; // string | The pending data token from the OAuth redirect URL (`pendingDataToken` parameter)

try {
    $result = $apiInstance->getPendingOAuthData($token);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConnectApi->getPendingOAuthData: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **token** | **string**| The pending data token from the OAuth redirect URL (&#x60;pendingDataToken&#x60; parameter) | |

### Return type

[**\Late\Model\GetPendingOAuthData200Response**](../Model/GetPendingOAuthData200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getPinterestBoards()`

```php
getPinterestBoards($account_id): \Late\Model\GetPinterestBoards200Response
```

List Pinterest boards for a connected account

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Late\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Late\Api\ConnectApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string

try {
    $result = $apiInstance->getPinterestBoards($account_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConnectApi->getPinterestBoards: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**|  | |

### Return type

[**\Late\Model\GetPinterestBoards200Response**](../Model/GetPinterestBoards200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getRedditFlairs()`

```php
getRedditFlairs($account_id, $subreddit): \Late\Model\GetRedditFlairs200Response
```

List available post flairs for a Reddit subreddit

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Late\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Late\Api\ConnectApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string
$subreddit = 'subreddit_example'; // string | Subreddit name (without \"r/\" prefix) to fetch flairs for

try {
    $result = $apiInstance->getRedditFlairs($account_id, $subreddit);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConnectApi->getRedditFlairs: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**|  | |
| **subreddit** | **string**| Subreddit name (without \&quot;r/\&quot; prefix) to fetch flairs for | |

### Return type

[**\Late\Model\GetRedditFlairs200Response**](../Model/GetRedditFlairs200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getRedditSubreddits()`

```php
getRedditSubreddits($account_id): \Late\Model\GetRedditSubreddits200Response
```

List Reddit subreddits for a connected account

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Late\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Late\Api\ConnectApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string

try {
    $result = $apiInstance->getRedditSubreddits($account_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConnectApi->getRedditSubreddits: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**|  | |

### Return type

[**\Late\Model\GetRedditSubreddits200Response**](../Model/GetRedditSubreddits200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getTelegramConnectStatus()`

```php
getTelegramConnectStatus($profile_id): \Late\Model\GetTelegramConnectStatus200Response
```

Generate Telegram access code

Generate a unique access code for connecting a Telegram channel or group.  **Connection Flow:** 1. Call this endpoint to get an access code (valid for 15 minutes) 2. Add the bot (@LateScheduleBot or your configured bot) as an administrator in your Telegram channel/group 3. Open a private chat with the bot 4. Send: `{CODE} @yourchannel` (e.g., `LATE-ABC123 @mychannel`) 5. Poll `PATCH /v1/connect/telegram?code={CODE}` to check connection status  **Alternative for private channels:** If your channel has no public username, forward any message from the channel to the bot along with the access code.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Late\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Late\Api\ConnectApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$profile_id = 'profile_id_example'; // string | The profile ID to connect the Telegram account to

try {
    $result = $apiInstance->getTelegramConnectStatus($profile_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConnectApi->getTelegramConnectStatus: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **profile_id** | **string**| The profile ID to connect the Telegram account to | |

### Return type

[**\Late\Model\GetTelegramConnectStatus200Response**](../Model/GetTelegramConnectStatus200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `handleOAuthCallback()`

```php
handleOAuthCallback($platform, $handle_o_auth_callback_request)
```

Complete OAuth token exchange manually (for server-side flows)

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Late\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Late\Api\ConnectApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$platform = 'platform_example'; // string
$handle_o_auth_callback_request = new \Late\Model\HandleOAuthCallbackRequest(); // \Late\Model\HandleOAuthCallbackRequest

try {
    $apiInstance->handleOAuthCallback($platform, $handle_o_auth_callback_request);
} catch (Exception $e) {
    echo 'Exception when calling ConnectApi->handleOAuthCallback: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **platform** | **string**|  | |
| **handle_o_auth_callback_request** | [**\Late\Model\HandleOAuthCallbackRequest**](../Model/HandleOAuthCallbackRequest.md)|  | |

### Return type

void (empty response body)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `initiateTelegramConnect()`

```php
initiateTelegramConnect($initiate_telegram_connect_request): \Late\Model\InitiateTelegramConnect200Response
```

Direct Telegram connection (power users)

Connect a Telegram channel/group directly using the chat ID.  This is an alternative to the access code flow for power users who know their Telegram chat ID. The bot must already be added as an administrator in the channel/group.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Late\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Late\Api\ConnectApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$initiate_telegram_connect_request = {"chatId":"-1001234567890","profileId":"6507a1b2c3d4e5f6a7b8c9d0"}; // \Late\Model\InitiateTelegramConnectRequest

try {
    $result = $apiInstance->initiateTelegramConnect($initiate_telegram_connect_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConnectApi->initiateTelegramConnect: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **initiate_telegram_connect_request** | [**\Late\Model\InitiateTelegramConnectRequest**](../Model/InitiateTelegramConnectRequest.md)|  | |

### Return type

[**\Late\Model\InitiateTelegramConnect200Response**](../Model/InitiateTelegramConnect200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listFacebookPages()`

```php
listFacebookPages($profile_id, $temp_token): \Late\Model\ListFacebookPages200Response
```

List Facebook Pages after OAuth (Headless Mode)

**Headless Mode for Custom UI**  After initiating Facebook OAuth via `/v1/connect/facebook`, you'll be redirected to  `/connect/facebook/select-page` with query params including `tempToken` and `userProfile`.  For a **headless/whitelabeled flow**, extract these params from the URL and call this  endpoint to retrieve the list of Facebook Pages the user can manage. Then build your  own UI to let users select a page.  **Note:** Use the `X-Connect-Token` header if you initiated the connection via API key  (rather than a browser session).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: connectToken
$config = Late\Configuration::getDefaultConfiguration()->setApiKey('X-Connect-Token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Late\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Connect-Token', 'Bearer');

// Configure Bearer (JWT) authorization: bearerAuth
$config = Late\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Late\Api\ConnectApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$profile_id = 'profile_id_example'; // string | Profile ID from your connection flow
$temp_token = 'temp_token_example'; // string | Temporary Facebook access token from the OAuth callback redirect

try {
    $result = $apiInstance->listFacebookPages($profile_id, $temp_token);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConnectApi->listFacebookPages: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **profile_id** | **string**| Profile ID from your connection flow | |
| **temp_token** | **string**| Temporary Facebook access token from the OAuth callback redirect | |

### Return type

[**\Late\Model\ListFacebookPages200Response**](../Model/ListFacebookPages200Response.md)

### Authorization

[connectToken](../../README.md#connectToken), [bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listGoogleBusinessLocations()`

```php
listGoogleBusinessLocations($profile_id, $temp_token): \Late\Model\ListGoogleBusinessLocations200Response
```

List Google Business Locations after OAuth (Headless Mode)

**Headless Mode for Custom UI**  After initiating Google Business OAuth via `/v1/connect/googlebusiness?headless=true`, you'll be redirected  to your `redirect_url` with query params including `tempToken` and `userProfile`.  For a **headless/whitelabeled flow**, extract these params from the URL and call this  endpoint to retrieve the list of Google Business locations the user can manage. Then build your  own UI to let users select a location.  **Note:** Use the `X-Connect-Token` header if you initiated the connection via API key  (rather than a browser session).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: connectToken
$config = Late\Configuration::getDefaultConfiguration()->setApiKey('X-Connect-Token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Late\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Connect-Token', 'Bearer');

// Configure Bearer (JWT) authorization: bearerAuth
$config = Late\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Late\Api\ConnectApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$profile_id = 'profile_id_example'; // string | Profile ID from your connection flow
$temp_token = 'temp_token_example'; // string | Temporary Google access token from the OAuth callback redirect

try {
    $result = $apiInstance->listGoogleBusinessLocations($profile_id, $temp_token);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConnectApi->listGoogleBusinessLocations: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **profile_id** | **string**| Profile ID from your connection flow | |
| **temp_token** | **string**| Temporary Google access token from the OAuth callback redirect | |

### Return type

[**\Late\Model\ListGoogleBusinessLocations200Response**](../Model/ListGoogleBusinessLocations200Response.md)

### Authorization

[connectToken](../../README.md#connectToken), [bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listLinkedInOrganizations()`

```php
listLinkedInOrganizations($temp_token, $org_ids): \Late\Model\ListLinkedInOrganizations200Response
```

Fetch full LinkedIn organization details (Headless Mode)

**Fetch Full Organization Details for Custom UI**  After LinkedIn OAuth in headless mode, the redirect URL contains organization data with only `id`, `urn`, and `name` fields (additional details are excluded to prevent URL length issues with many organizations).  Use this endpoint to fetch full organization details including logos, vanity names, websites, and more if you want to display them in your custom selection UI.  **Note:** This endpoint requires no authentication - just the `tempToken` from the OAuth redirect. Details are fetched directly from LinkedIn's API in parallel for fast response times.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Late\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Late\Api\ConnectApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$temp_token = 'temp_token_example'; // string | The temporary LinkedIn access token from the OAuth redirect
$org_ids = 12345678,87654321,11111111; // string | Comma-separated list of organization IDs to fetch details for (max 100)

try {
    $result = $apiInstance->listLinkedInOrganizations($temp_token, $org_ids);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConnectApi->listLinkedInOrganizations: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **temp_token** | **string**| The temporary LinkedIn access token from the OAuth redirect | |
| **org_ids** | **string**| Comma-separated list of organization IDs to fetch details for (max 100) | |

### Return type

[**\Late\Model\ListLinkedInOrganizations200Response**](../Model/ListLinkedInOrganizations200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listPinterestBoardsForSelection()`

```php
listPinterestBoardsForSelection($x_connect_token, $profile_id, $temp_token): \Late\Model\ListPinterestBoardsForSelection200Response
```

List Pinterest Boards after OAuth (Headless Mode)

**Retrieve Pinterest Boards for Selection UI**  After initiating Pinterest OAuth via `/v1/connect/pinterest` with `headless=true`, you'll be redirected to your `redirect_url` with query params including `tempToken` and `userProfile`.  If you want to build your own fully-branded board selector (instead of Late's hosted UI), call this endpoint to retrieve the list of Pinterest Boards the user can post to. Then build your UI and call `POST /v1/connect/pinterest/select-board` to save the selection.  **Authentication:** Use `X-Connect-Token` header with the `connect_token` from the redirect URL.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Late\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Late\Api\ConnectApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$x_connect_token = 'x_connect_token_example'; // string | Short-lived connect token from the OAuth redirect
$profile_id = 'profile_id_example'; // string | Your Late profile ID
$temp_token = 'temp_token_example'; // string | Temporary Pinterest access token from the OAuth callback redirect

try {
    $result = $apiInstance->listPinterestBoardsForSelection($x_connect_token, $profile_id, $temp_token);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConnectApi->listPinterestBoardsForSelection: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **x_connect_token** | **string**| Short-lived connect token from the OAuth redirect | |
| **profile_id** | **string**| Your Late profile ID | |
| **temp_token** | **string**| Temporary Pinterest access token from the OAuth callback redirect | |

### Return type

[**\Late\Model\ListPinterestBoardsForSelection200Response**](../Model/ListPinterestBoardsForSelection200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listSnapchatProfiles()`

```php
listSnapchatProfiles($x_connect_token, $profile_id, $temp_token): \Late\Model\ListSnapchatProfiles200Response
```

List Snapchat Public Profiles after OAuth (Headless Mode)

**Headless Mode for Custom UI**  After initiating Snapchat OAuth via `/v1/connect/snapchat?headless=true`, you'll be redirected to your `redirect_url` with query params including `tempToken`, `userProfile`, and `publicProfiles`.  If you want to build your own fully-branded profile selector (instead of Late's hosted UI), call this endpoint to retrieve the list of Snapchat Public Profiles the user can post to. Then build your UI and call `POST /v1/connect/snapchat/select-profile` to save the selection.  **Authentication:** Use `X-Connect-Token` header with the `connect_token` from the redirect URL.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Late\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Late\Api\ConnectApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$x_connect_token = 'x_connect_token_example'; // string | Short-lived connect token from the OAuth redirect
$profile_id = 'profile_id_example'; // string | Your Late profile ID
$temp_token = 'temp_token_example'; // string | Temporary Snapchat access token from the OAuth callback redirect

try {
    $result = $apiInstance->listSnapchatProfiles($x_connect_token, $profile_id, $temp_token);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConnectApi->listSnapchatProfiles: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **x_connect_token** | **string**| Short-lived connect token from the OAuth redirect | |
| **profile_id** | **string**| Your Late profile ID | |
| **temp_token** | **string**| Temporary Snapchat access token from the OAuth callback redirect | |

### Return type

[**\Late\Model\ListSnapchatProfiles200Response**](../Model/ListSnapchatProfiles200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `selectFacebookPage()`

```php
selectFacebookPage($select_facebook_page_request): \Late\Model\SelectFacebookPage200Response
```

Select a Facebook Page to complete the connection (Headless Mode)

**Complete the Headless Flow**  After displaying your custom UI with the list of pages from the GET endpoint, call this  endpoint to finalize the connection with the user's selected page.  The `userProfile` should be the decoded JSON object from the `userProfile` query param  in the OAuth callback redirect URL.  **Note:** Use the `X-Connect-Token` header if you initiated the connection via API key.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: connectToken
$config = Late\Configuration::getDefaultConfiguration()->setApiKey('X-Connect-Token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Late\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Connect-Token', 'Bearer');

// Configure Bearer (JWT) authorization: bearerAuth
$config = Late\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Late\Api\ConnectApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$select_facebook_page_request = {"profileId":"507f1f77bcf86cd799439011","pageId":"123456789","tempToken":"EAAxxxxx...","userProfile":{"id":"987654321","name":"John Doe","profilePicture":"https://..."},"redirect_url":"https://yourdomain.com/integrations/callback"}; // \Late\Model\SelectFacebookPageRequest

try {
    $result = $apiInstance->selectFacebookPage($select_facebook_page_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConnectApi->selectFacebookPage: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **select_facebook_page_request** | [**\Late\Model\SelectFacebookPageRequest**](../Model/SelectFacebookPageRequest.md)|  | |

### Return type

[**\Late\Model\SelectFacebookPage200Response**](../Model/SelectFacebookPage200Response.md)

### Authorization

[connectToken](../../README.md#connectToken), [bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `selectGoogleBusinessLocation()`

```php
selectGoogleBusinessLocation($select_google_business_location_request): \Late\Model\SelectGoogleBusinessLocation200Response
```

Select a Google Business location to complete the connection (Headless Mode)

**Complete the Headless Flow**  After displaying your custom UI with the list of locations from the GET `/v1/connect/googlebusiness/locations`  endpoint, call this endpoint to finalize the connection with the user's selected location.  The `userProfile` should be the decoded JSON object from the `userProfile` query param  in the OAuth callback redirect URL. It contains important token information (including refresh token).  **Note:** Use the `X-Connect-Token` header if you initiated the connection via API key.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: connectToken
$config = Late\Configuration::getDefaultConfiguration()->setApiKey('X-Connect-Token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Late\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Connect-Token', 'Bearer');

// Configure Bearer (JWT) authorization: bearerAuth
$config = Late\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Late\Api\ConnectApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$select_google_business_location_request = {"profileId":"507f1f77bcf86cd799439011","locationId":"9281089117903930794","tempToken":"ya29.xxxxx...","userProfile":{"id":"113303573364907650416","name":"John Doe","refreshToken":"1//0gxxxxx...","tokenExpiresIn":3599,"scope":"https://www.googleapis.com/auth/business.manage"},"redirect_url":"https://yourdomain.com/integrations/callback"}; // \Late\Model\SelectGoogleBusinessLocationRequest

try {
    $result = $apiInstance->selectGoogleBusinessLocation($select_google_business_location_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConnectApi->selectGoogleBusinessLocation: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **select_google_business_location_request** | [**\Late\Model\SelectGoogleBusinessLocationRequest**](../Model/SelectGoogleBusinessLocationRequest.md)|  | |

### Return type

[**\Late\Model\SelectGoogleBusinessLocation200Response**](../Model/SelectGoogleBusinessLocation200Response.md)

### Authorization

[connectToken](../../README.md#connectToken), [bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `selectLinkedInOrganization()`

```php
selectLinkedInOrganization($select_linked_in_organization_request): \Late\Model\SelectLinkedInOrganization200Response
```

Select LinkedIn organization or personal account after OAuth

**Complete the LinkedIn Connection Flow**  After OAuth, the user is redirected with `organizations` in the URL params (if they have org admin access). The organizations array contains `id`, `urn`, and `name` fields. Use this data to build your UI,  then call this endpoint to save the selection.  Set `accountType` to `personal` to connect as the user's personal LinkedIn profile, or `organization` to connect as a company page (requires `selectedOrganization` object).  **Personal Profile:** To connect a personal LinkedIn account, set `accountType` to `\"personal\"` and **omit** the `selectedOrganization` field entirely. This is the simplest flow.  **Headless Mode:** Use the `X-Connect-Token` header if you initiated the connection via API key.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Late\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Late\Api\ConnectApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$select_linked_in_organization_request = {"profileId":"64f0a1b2c3d4e5f6a7b8c9d0","tempToken":"AQX...","userProfile":{"id":"abc123","username":"johndoe","displayName":"John Doe","profilePicture":"https://media.licdn.com/dms/image/v2/..."},"accountType":"personal"}; // \Late\Model\SelectLinkedInOrganizationRequest

try {
    $result = $apiInstance->selectLinkedInOrganization($select_linked_in_organization_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConnectApi->selectLinkedInOrganization: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **select_linked_in_organization_request** | [**\Late\Model\SelectLinkedInOrganizationRequest**](../Model/SelectLinkedInOrganizationRequest.md)|  | |

### Return type

[**\Late\Model\SelectLinkedInOrganization200Response**](../Model/SelectLinkedInOrganization200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `selectPinterestBoard()`

```php
selectPinterestBoard($select_pinterest_board_request): \Late\Model\SelectPinterestBoard200Response
```

Select a Pinterest Board to complete the connection (Headless Mode)

**Complete the Pinterest Connection Flow**  After OAuth, use this endpoint to save the selected board and complete the Pinterest account connection.  **Headless Mode:** Use the `X-Connect-Token` header if you initiated the connection via API key.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Late\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Late\Api\ConnectApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$select_pinterest_board_request = {"profileId":"64f0a1b2c3d4e5f6a7b8c9d0","boardId":"123456789012345678","boardName":"Marketing Ideas","tempToken":"pina_...","userProfile":{"id":"user123","username":"mybrand","displayName":"My Brand","profilePicture":"https://i.pinimg.com/..."},"redirect_url":"https://yourapp.com/callback"}; // \Late\Model\SelectPinterestBoardRequest

try {
    $result = $apiInstance->selectPinterestBoard($select_pinterest_board_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConnectApi->selectPinterestBoard: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **select_pinterest_board_request** | [**\Late\Model\SelectPinterestBoardRequest**](../Model/SelectPinterestBoardRequest.md)|  | |

### Return type

[**\Late\Model\SelectPinterestBoard200Response**](../Model/SelectPinterestBoard200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `selectSnapchatProfile()`

```php
selectSnapchatProfile($select_snapchat_profile_request, $x_connect_token): \Late\Model\SelectSnapchatProfile200Response
```

Select a Snapchat Public Profile to complete the connection (Headless Mode)

**Complete the Snapchat Connection Flow**  After OAuth, use this endpoint to save the selected Public Profile and complete the Snapchat account connection. Snapchat requires a Public Profile to publish Stories, Saved Stories, and Spotlight content.  **Headless Mode:** Use the `X-Connect-Token` header if you initiated the connection via API key.  After initiating Snapchat OAuth via `/v1/connect/snapchat?headless=true`, you'll be redirected to your `redirect_url` with query params including: - `tempToken` - Temporary access token - `userProfile` - URL-encoded JSON with user info - `publicProfiles` - URL-encoded JSON array of available public profiles - `connect_token` - Short-lived token for API authentication - `platform=snapchat` - `step=select_public_profile`  Parse `publicProfiles` to build your custom selector UI, then call this endpoint with the selected profile.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Late\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Late\Api\ConnectApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$select_snapchat_profile_request = {"profileId":"64f0a1b2c3d4e5f6a7b8c9d0","selectedPublicProfile":{"id":"abc123-def456","display_name":"My Brand","username":"mybrand","profile_image_url":"https://cf-st.sc-cdn.net/...","subscriber_count":15000},"tempToken":"eyJ...","userProfile":{"id":"user123","username":"mybrand","displayName":"My Brand","profilePicture":"https://cf-st.sc-cdn.net/..."},"redirect_url":"https://yourapp.com/callback"}; // \Late\Model\SelectSnapchatProfileRequest
$x_connect_token = 'x_connect_token_example'; // string | Short-lived connect token from the OAuth redirect (for API users)

try {
    $result = $apiInstance->selectSnapchatProfile($select_snapchat_profile_request, $x_connect_token);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConnectApi->selectSnapchatProfile: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **select_snapchat_profile_request** | [**\Late\Model\SelectSnapchatProfileRequest**](../Model/SelectSnapchatProfileRequest.md)|  | |
| **x_connect_token** | **string**| Short-lived connect token from the OAuth redirect (for API users) | [optional] |

### Return type

[**\Late\Model\SelectSnapchatProfile200Response**](../Model/SelectSnapchatProfile200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateFacebookPage()`

```php
updateFacebookPage($account_id, $update_facebook_page_request): \Late\Model\UpdateFacebookPage200Response
```

Update selected Facebook page for a connected account

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Late\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Late\Api\ConnectApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string
$update_facebook_page_request = {"selectedPageId":"123456789012345"}; // \Late\Model\UpdateFacebookPageRequest

try {
    $result = $apiInstance->updateFacebookPage($account_id, $update_facebook_page_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConnectApi->updateFacebookPage: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**|  | |
| **update_facebook_page_request** | [**\Late\Model\UpdateFacebookPageRequest**](../Model/UpdateFacebookPageRequest.md)|  | |

### Return type

[**\Late\Model\UpdateFacebookPage200Response**](../Model/UpdateFacebookPage200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateGmbLocation()`

```php
updateGmbLocation($account_id, $update_gmb_location_request): \Late\Model\UpdateGmbLocation200Response
```

Update selected Google Business Profile location for a connected account

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Late\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Late\Api\ConnectApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string
$update_gmb_location_request = {"selectedLocationId":"12345678901234567890"}; // \Late\Model\UpdateGmbLocationRequest

try {
    $result = $apiInstance->updateGmbLocation($account_id, $update_gmb_location_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConnectApi->updateGmbLocation: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**|  | |
| **update_gmb_location_request** | [**\Late\Model\UpdateGmbLocationRequest**](../Model/UpdateGmbLocationRequest.md)|  | |

### Return type

[**\Late\Model\UpdateGmbLocation200Response**](../Model/UpdateGmbLocation200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateLinkedInOrganization()`

```php
updateLinkedInOrganization($account_id, $update_linked_in_organization_request): \Late\Model\ConnectBlueskyCredentials200Response
```

Switch LinkedIn account type (personal/organization)

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Late\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Late\Api\ConnectApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string
$update_linked_in_organization_request = {"accountType":"organization","selectedOrganization":{"id":"12345678","name":"Acme Corporation","vanityName":"acme-corp"}}; // \Late\Model\UpdateLinkedInOrganizationRequest

try {
    $result = $apiInstance->updateLinkedInOrganization($account_id, $update_linked_in_organization_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConnectApi->updateLinkedInOrganization: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**|  | |
| **update_linked_in_organization_request** | [**\Late\Model\UpdateLinkedInOrganizationRequest**](../Model/UpdateLinkedInOrganizationRequest.md)|  | |

### Return type

[**\Late\Model\ConnectBlueskyCredentials200Response**](../Model/ConnectBlueskyCredentials200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updatePinterestBoards()`

```php
updatePinterestBoards($account_id, $update_pinterest_boards_request): \Late\Model\ConnectBlueskyCredentials200Response
```

Set default Pinterest board on the connection

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Late\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Late\Api\ConnectApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string
$update_pinterest_boards_request = {"defaultBoardId":"123456789012345678","defaultBoardName":"Marketing Ideas"}; // \Late\Model\UpdatePinterestBoardsRequest

try {
    $result = $apiInstance->updatePinterestBoards($account_id, $update_pinterest_boards_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConnectApi->updatePinterestBoards: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**|  | |
| **update_pinterest_boards_request** | [**\Late\Model\UpdatePinterestBoardsRequest**](../Model/UpdatePinterestBoardsRequest.md)|  | |

### Return type

[**\Late\Model\ConnectBlueskyCredentials200Response**](../Model/ConnectBlueskyCredentials200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateRedditSubreddits()`

```php
updateRedditSubreddits($account_id, $update_reddit_subreddits_request): \Late\Model\UpdateRedditSubreddits200Response
```

Set default subreddit on the connection

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Late\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Late\Api\ConnectApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string
$update_reddit_subreddits_request = {"defaultSubreddit":"marketing"}; // \Late\Model\UpdateRedditSubredditsRequest

try {
    $result = $apiInstance->updateRedditSubreddits($account_id, $update_reddit_subreddits_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConnectApi->updateRedditSubreddits: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**|  | |
| **update_reddit_subreddits_request** | [**\Late\Model\UpdateRedditSubredditsRequest**](../Model/UpdateRedditSubredditsRequest.md)|  | |

### Return type

[**\Late\Model\UpdateRedditSubreddits200Response**](../Model/UpdateRedditSubreddits200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
