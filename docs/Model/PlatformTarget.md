# # PlatformTarget

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**platform** | **string** | Supported values: twitter, threads, instagram, youtube, facebook, linkedin, pinterest, reddit, tiktok, bluesky, googlebusiness, telegram | [optional]
**account_id** | [**\Late\Model\PlatformTargetAccountId**](PlatformTargetAccountId.md) |  | [optional]
**custom_content** | **string** | Platform-specific text override. When set, this content is used instead of the top-level post content for this platform. Useful for tailoring captions per platform (e.g. keeping tweets under 280 characters). | [optional]
**custom_media** | [**\Late\Model\MediaItem[]**](MediaItem.md) |  | [optional]
**scheduled_for** | **\DateTime** | Optional per-platform scheduled time override (uses post.scheduledFor when omitted) | [optional]
**platform_specific_data** | [**\Late\Model\PlatformTargetPlatformSpecificData**](PlatformTargetPlatformSpecificData.md) |  | [optional]
**status** | **string** | Platform-specific status: pending, publishing, published, failed | [optional]
**platform_post_id** | **string** | The native post ID on the platform (populated after successful publish) | [optional]
**platform_post_url** | **string** | Public URL of the published post on the platform. Populated after successful publish. For immediate posts (publishNow&#x3D;true),  this is included in the response. For scheduled posts, fetch the post  via GET /v1/posts/{postId} after the scheduled time. | [optional]
**published_at** | **\DateTime** | Timestamp when the post was published to this platform | [optional]
**error_message** | **string** | Human-readable error message when status is &#39;failed&#39;. Contains platform-specific error details explaining why the publish failed. Examples: - \&quot;Instagram access token has expired. Please reconnect your account.\&quot; - \&quot;Post text exceeds the 500 character limit for Threads.\&quot; - \&quot;You do not have enough karma to post in this subreddit.\&quot; - \&quot;Video is too long for Reels. Facebook Reels must be 90 seconds or less.\&quot; | [optional]
**error_category** | **string** | Error category for programmatic handling: - auth_expired: Token expired or revoked, account needs reconnection - user_content: Content doesn&#39;t meet platform requirements (too long, wrong format, etc.) - user_abuse: Rate limits, spam detection, excessive posting - account_issue: Account configuration problems (missing board, inactive account) - platform_rejected: Platform rules violated (banned, suspended, policy violation) - platform_error: Platform-side issues (5xx errors, maintenance) - system_error: Late infrastructure issues (timeouts, network errors) - unknown: Unclassified error | [optional]
**error_source** | **string** | Who/what caused the error: - user: User action required (fix content, reconnect account) - platform: Platform-side issue (outage, API change) - system: Late system issue (rare) | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
