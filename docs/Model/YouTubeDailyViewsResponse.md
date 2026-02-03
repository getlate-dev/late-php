# # YouTubeDailyViewsResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **bool** |  | [optional]
**video_id** | **string** | The YouTube video ID | [optional]
**date_range** | [**\Late\Model\YouTubeDailyViewsResponseDateRange**](YouTubeDailyViewsResponseDateRange.md) |  | [optional]
**total_views** | **int** | Sum of views across all days in the range | [optional]
**daily_views** | [**\Late\Model\YouTubeDailyViewsResponseDailyViewsInner[]**](YouTubeDailyViewsResponseDailyViewsInner.md) |  | [optional]
**last_synced_at** | **\DateTime** | When the data was last synced from YouTube | [optional]
**scope_status** | [**\Late\Model\YouTubeDailyViewsResponseScopeStatus**](YouTubeDailyViewsResponseScopeStatus.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
