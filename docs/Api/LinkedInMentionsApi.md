# Late\LinkedInMentionsApi



All URIs are relative to https://getlate.dev/api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getLinkedInMentions()**](LinkedInMentionsApi.md#getLinkedInMentions) | **GET** /v1/accounts/{accountId}/linkedin-mentions | Resolve a LinkedIn profile or company URL to a URN for @mentions |


## `getLinkedInMentions()`

```php
getLinkedInMentions($account_id, $url, $display_name): \Late\Model\GetLinkedInMentions200Response
```

Resolve a LinkedIn profile or company URL to a URN for @mentions

Converts a LinkedIn profile URL (person) or company page URL (organization) to a URN that can be used to @mention them in posts.  **Supports both:** - **Person mentions:** `linkedin.com/in/username` or just `username` - **Organization mentions:** `linkedin.com/company/company-name` or `company/company-name`  **⚠️ Organization Admin Required for Person Mentions Only:** Person mentions require the connected LinkedIn account to have admin access to at least one LinkedIn Organization (Company Page). Organization mentions do NOT have this requirement - any LinkedIn account can tag companies.  **IMPORTANT - Display Name Requirement:** For **person mentions** to be clickable, the display name must **exactly match** what appears on their LinkedIn profile. - Organization mentions automatically retrieve the company name from LinkedIn API - Person mentions require the exact name, so provide the `displayName` parameter  **Mention Format:** Use the returned `mentionFormat` value directly in your post content: ``` Great insights from @[Miquel Palet](urn:li:person:4qj5ox-agD) on this topic! Excited to partner with @[Microsoft](urn:li:organization:1035)! ```

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Late\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Late\Api\LinkedInMentionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string | The LinkedIn account ID
$url = miquelpalet; // string | LinkedIn profile URL, company URL, or vanity name. - Person: `miquelpalet`, `linkedin.com/in/miquelpalet` - Organization: `company/microsoft`, `linkedin.com/company/microsoft`
$display_name = Miquel Palet; // string | The exact display name as shown on LinkedIn. - **Person mentions:** Required for clickable mentions. If not provided, a name is derived from the vanity URL which may not match exactly. - **Organization mentions:** Optional. If not provided, the company name is automatically retrieved from LinkedIn.

try {
    $result = $apiInstance->getLinkedInMentions($account_id, $url, $display_name);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LinkedInMentionsApi->getLinkedInMentions: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**| The LinkedIn account ID | |
| **url** | **string**| LinkedIn profile URL, company URL, or vanity name. - Person: &#x60;miquelpalet&#x60;, &#x60;linkedin.com/in/miquelpalet&#x60; - Organization: &#x60;company/microsoft&#x60;, &#x60;linkedin.com/company/microsoft&#x60; | |
| **display_name** | **string**| The exact display name as shown on LinkedIn. - **Person mentions:** Required for clickable mentions. If not provided, a name is derived from the vanity URL which may not match exactly. - **Organization mentions:** Optional. If not provided, the company name is automatically retrieved from LinkedIn. | [optional] |

### Return type

[**\Late\Model\GetLinkedInMentions200Response**](../Model/GetLinkedInMentions200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
