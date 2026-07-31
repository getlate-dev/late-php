# # UpdateAdCampaignRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **string** | Zernio SocialAccount id owning the ad account. Required only to update an EMPTY campaign (zero ads), which has no local Ad documents to resolve a token from. | [optional]
**platform** | **string** |  |
**budget** | [**\Zernio\Model\UpdateAdCampaignRequestBudget**](UpdateAdCampaignRequestBudget.md) |  | [optional]
**bid_strategy** | [**\Zernio\Model\BidStrategy**](BidStrategy.md) | Campaign-level default. Ad sets inherit this unless they override. | [optional]
**name** | **string** | Rename the campaign (Meta only; other platforms return 501). At least one of budget/bidStrategy/name/platformSpecificData is required. | [optional]
**platform_specific_data** | [**\Zernio\Model\UpdateAdCampaignRequestPlatformSpecificData**](UpdateAdCampaignRequestPlatformSpecificData.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
