# # UpdateAdCampaignStatus200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**status** | **string** | The status written to the campaign | [optional]
**updated** | **int** | Number of ads whose own stored status changed too. 0 is normal on a resume whose ads are all awaiting the platform. | [optional]
**skipped** | **int** | Number of ads whose own status was left as it was | [optional]
**skipped_reasons** | **string[]** | Why each group of ads was skipped | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
