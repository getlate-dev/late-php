# # PostLogDetail

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**_id** | **string** |  | [optional]
**post_id** | [**\Late\Model\PostLogDetailAllOfPostId**](PostLogDetailAllOfPostId.md) |  | [optional]
**user_id** | **string** |  | [optional]
**profile_id** | **string** |  | [optional]
**platform** | **string** |  | [optional]
**account_id** | [**\Late\Model\PostLogDetailAllOfAccountId**](PostLogDetailAllOfAccountId.md) |  | [optional]
**account_username** | **string** |  | [optional]
**action** | **string** | Type of action logged: - &#x60;publish&#x60; - Initial publish attempt - &#x60;retry&#x60; - Retry after failure - &#x60;media_upload&#x60; - Media upload step - &#x60;rate_limit_pause&#x60; - Account paused due to rate limits - &#x60;token_refresh&#x60; - Token was refreshed - &#x60;cancelled&#x60; - Post was cancelled | [optional]
**status** | **string** |  | [optional]
**status_code** | **int** | HTTP status code from platform API | [optional]
**endpoint** | **string** | Platform API endpoint called | [optional]
**request** | [**\Late\Model\PostLogRequest**](PostLogRequest.md) |  | [optional]
**response** | [**\Late\Model\PostLogResponse**](PostLogResponse.md) |  | [optional]
**duration_ms** | **int** | How long the operation took in milliseconds | [optional]
**attempt_number** | **int** | Attempt number (1 for first try, 2+ for retries) | [optional]
**created_at** | **\DateTime** |  | [optional]
**metadata** | **object** | Additional metadata (e.g., rate limit info) | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
