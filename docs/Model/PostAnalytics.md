# # PostAnalytics

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**impressions** | **int** |  | [optional]
**reach** | **int** |  | [optional]
**likes** | **int** |  | [optional]
**comments** | **int** |  | [optional]
**shares** | **int** |  | [optional]
**saves** | **int** | Number of saves/bookmarks (Instagram, Pinterest, X/Twitter) | [optional]
**clicks** | **int** |  | [optional]
**views** | **int** |  | [optional]
**follows** | **int** | Instagram feed posts and stories only: organic accounts that started following from this post. 0 for reels and other platforms. | [optional]
**ig_reels_avg_watch_time** | **int** | Instagram Reels only: average watch time per play, in milliseconds. 0 for non-Reels media and other platforms. | [optional]
**ig_reels_video_view_total_time** | **int** | Instagram Reels only: total watch time including replays, in milliseconds. 0 for non-Reels media and other platforms. | [optional]
**video_duration_seconds** | **int** | Video length in seconds. Currently Instagram Reels only; combine with igReelsAvgWatchTime (ms) to estimate retention. Null when unknown (other platforms, non-video media, or when Instagram does not expose the media URL, e.g. reels with copyrighted audio). | [optional]
**engagement_rate** | **float** | Percentage, rounded to 2 decimals: (likes + comments + shares + saves) / (impressions or reach or views) * 100. Clicks and follows are never counted. The denominator is the FIRST of impressions, reach, views that is non-zero, so it is not the same basis on every post: a post with impressions divides by impressions, one without falls back to reach, then to views. If you need a single consistent basis (e.g. interactions / reach), compute it from the raw fields above. The engagementRate on the LinkedIn account endpoints is a different formula. | [optional]
**last_updated** | **\DateTime** |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
