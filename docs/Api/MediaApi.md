# Late\MediaApi



All URIs are relative to https://getlate.dev/api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getMediaPresignedUrl()**](MediaApi.md#getMediaPresignedUrl) | **POST** /v1/media/presign | Get a presigned URL for direct file upload (up to 5GB) |


## `getMediaPresignedUrl()`

```php
getMediaPresignedUrl($get_media_presigned_url_request): \Late\Model\GetMediaPresignedUrl200Response
```

Get a presigned URL for direct file upload (up to 5GB)

Get a presigned URL to upload files directly to cloud storage. This is the recommended method for uploading files of any size, especially files larger than ~4MB.  **How it works:** 1. Call this endpoint with the filename and content type 2. Receive an `uploadUrl` (presigned) and `publicUrl` 3. PUT your file directly to the `uploadUrl` 4. Use the `publicUrl` in your posts  **Benefits:** - Supports files up to 5GB - Files upload directly to storage (faster, no server bottleneck) - No 413 errors from server body size limits  **Example:** ```javascript // Step 1: Get presigned URL const response = await fetch('https://getlate.dev/api/v1/media/presign', {   method: 'POST',   headers: {     'Authorization': 'Bearer YOUR_API_KEY',     'Content-Type': 'application/json'   },   body: JSON.stringify({     filename: 'my-video.mp4',     contentType: 'video/mp4'   }) }); const { uploadUrl, publicUrl } = await response.json();  // Step 2: Upload file directly to storage await fetch(uploadUrl, {   method: 'PUT',   body: file,   headers: { 'Content-Type': 'video/mp4' } });  // Step 3: Use publicUrl when creating your post // The publicUrl is ready to use immediately after upload completes ```

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Late\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Late\Api\MediaApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$get_media_presigned_url_request = new \Late\Model\GetMediaPresignedUrlRequest(); // \Late\Model\GetMediaPresignedUrlRequest

try {
    $result = $apiInstance->getMediaPresignedUrl($get_media_presigned_url_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MediaApi->getMediaPresignedUrl: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **get_media_presigned_url_request** | [**\Late\Model\GetMediaPresignedUrlRequest**](../Model/GetMediaPresignedUrlRequest.md)|  | |

### Return type

[**\Late\Model\GetMediaPresignedUrl200Response**](../Model/GetMediaPresignedUrl200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
