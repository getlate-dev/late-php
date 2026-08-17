# # UpdateAdSet200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**budget** | [**\Zernio\Model\AdBudget**](AdBudget.md) |  | [optional]
**budget_level** | **string** |  | [optional]
**status** | **string** | The status written to the ad set. Absent when nothing was written (see statusMessage). | [optional]
**status_updated** | **int** | Number of ads whose own stored status changed alongside the ad set switch | [optional]
**status_skipped** | **int** | Number of ads whose own status was left as it was | [optional]
**status_skipped_reasons** | **string[]** | Why each group of ads was skipped | [optional]
**status_message** | **string** | Present only where the platform has no ad-set switch and no child ad was actionable; &#x60;status&#x60; is then absent because nothing was written | [optional]
**bid_strategy** | [**\Zernio\Model\BidStrategy**](BidStrategy.md) |  | [optional]
**bid_amount** | **float** |  | [optional]
**roas_average_floor** | **float** |  | [optional]
**platform_specific_data** | **object** |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
