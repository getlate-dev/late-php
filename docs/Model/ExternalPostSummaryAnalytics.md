# # ExternalPostSummaryAnalytics

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**likes** | **int** |  | [optional]
**comments** | **int** |  | [optional]
**shares** | **int** |  | [optional]
**saves** | **int** |  | [optional]
**sends** | **int** |  | [optional]
**clicks** | **int** |  | [optional]
**views** | **int** |  | [optional]
**reach** | **int** |  | [optional]
**impressions** | **int** |  | [optional]
**engagement_rate** | **float** | Percentage, rounded to 2 decimals. Same definition as PostAnalytics.engagementRate: (likes + comments + shares + saves) / (impressions or reach or views) * 100, where the denominator is the first of the three that is non-zero. Clicks and follows are never counted. | [optional]
**last_updated** | **\DateTime** | When these metrics were last refreshed | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
