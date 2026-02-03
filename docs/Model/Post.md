# # Post

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**_id** | **string** |  | [optional]
**user_id** | [**\Late\Model\PostUserId**](PostUserId.md) |  | [optional]
**title** | **string** | YouTube: title must be ≤ 100 characters. | [optional]
**content** | **string** |  | [optional]
**media_items** | [**\Late\Model\MediaItem[]**](MediaItem.md) |  | [optional]
**platforms** | [**\Late\Model\PlatformTarget[]**](PlatformTarget.md) |  | [optional]
**scheduled_for** | **\DateTime** |  | [optional]
**timezone** | **string** |  | [optional]
**status** | **string** |  | [optional]
**tags** | **string[]** | YouTube tag constraints when targeting YouTube: - No count cap; duplicates removed. - Each tag must be ≤ 100 chars. - Combined characters across all tags ≤ 500. | [optional]
**hashtags** | **string[]** |  | [optional]
**mentions** | **string[]** |  | [optional]
**visibility** | **string** |  | [optional]
**metadata** | **array<string,mixed>** |  | [optional]
**queued_from_profile** | **string** | Profile ID if the post was scheduled via the queue | [optional]
**queue_id** | **string** | Queue ID if the post was scheduled via a specific queue | [optional]
**created_at** | **\DateTime** |  | [optional]
**updated_at** | **\DateTime** |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
