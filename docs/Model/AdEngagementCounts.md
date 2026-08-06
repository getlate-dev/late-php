# # AdEngagementCounts

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**post_engagement** | **int** | Meta&#39;s own post-engagement total (&#x60;post_engagement&#x60;). | [optional]
**page_engagement** | **int** | Meta&#39;s own page-engagement total (&#x60;page_engagement&#x60;). | [optional]
**reactions** | **int** | Reactions on the ad&#39;s post (&#x60;post_reaction&#x60;). | [optional]
**comments** | **int** | Comments on the ad&#39;s post. | [optional]
**shares** | **int** | Shares of the ad&#39;s post. Meta reports these under the action type literally named &#x60;post&#x60;. | [optional]
**saves** | **int** | Saves of the ad&#39;s post (&#x60;onsite_conversion.post_save&#x60;). | [optional]
**page_likes** | **int** | New Page likes attributed to the ad (&#x60;like&#x60;). | [optional]
**video_views** | **int** | 3-second video views (&#x60;video_view&#x60;). For completion-based counts use &#x60;videoThruplayWatchedActions&#x60;. | [optional]
**link_clicks** | **int** | Attributed link clicks (&#x60;link_click&#x60;). This is the attribution-window count, which differs from the in-session &#x60;inline_link_clicks&#x60; reported by &#x60;GET /v1/ads/{adId}/analytics&#x60;. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
