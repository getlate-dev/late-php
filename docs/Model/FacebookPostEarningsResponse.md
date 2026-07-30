# # FacebookPostEarningsResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **bool** |  | [optional]
**account_id** | **string** |  | [optional]
**post_id** | **string** | The platform post ID that was queried, echoed back. | [optional]
**platform** | **string** |  | [optional]
**period** | **string** | Always \&quot;lifetime\&quot;: the total is cumulative since publication and must not be summed across dates or across posts. | [optional]
**metrics** | [**array<string,\Zernio\Model\FacebookPostEarningsResponseMetricsValue>**](FacebookPostEarningsResponseMetricsValue.md) | One entry per served metric. A metric reported here with \&quot;total\&quot;: 0 genuinely earned nothing (or its Page is not enrolled, which Meta reports identically). | [optional]
**unavailable_metrics** | [**\Zernio\Model\FacebookPostEarningsResponseUnavailableMetricsInner[]**](FacebookPostEarningsResponseUnavailableMetricsInner.md) | Requested metrics Meta could not serve. Present only when at least one metric is unavailable, and absent otherwise. Each listed metric is OMITTED from \&quot;metrics\&quot; rather than reported as 0. The request itself still succeeds with HTTP 200. | [optional]
**data_delay** | **string** |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
