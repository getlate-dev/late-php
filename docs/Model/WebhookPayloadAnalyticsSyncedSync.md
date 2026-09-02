# # WebhookPayloadAnalyticsSyncedSync

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**synced_at** | **\DateTime** | When the cycle COMPLETED. Not a join key for the delta feed: the rows a cycle produces carry a &#x60;syncedAt&#x60; stamped when the cycle STARTED, which is measured at around one second earlier at the median and up to a couple of minutes earlier in the tail. Correlate on &#x60;account.accountId&#x60;. |
**posts_updated** | **int** | Post records created or modified by this cycle. Not the number of delta feed rows the cycle produced, which the syncer does not report, so a cycle with a non-zero &#x60;postsUpdated&#x60; can still yield an empty delta page. |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
