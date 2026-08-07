# # UpdateAdCampaignRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**platform** | **string** | Required: platform campaign IDs are not globally unique. |
**account_id** | **string** | **Meta only.** Zernio SocialAccount id owning the ad account. Needed only for an EMPTY campaign (zero ads); ignored otherwise. | [optional]
**bid_strategy** | [**\Zernio\Model\BidStrategy**](BidStrategy.md) | **Meta + Google.** On Meta, the campaign default that ad sets inherit unless they override it. On Google, the campaign&#39;s own bidding strategy. | [optional]
**bid_amount** | **float** | **Google only.** Whole currency units (USD: 12 &#x3D; $12.00). Max CPC for LOWEST_COST_WITH_BID_CAP, CPA target for COST_CAP; required for both. | [optional]
**roas_average_floor** | **float** | **Google only.** Decimal ROAS multiplier (2.0 &#x3D; 2.0x), required for LOWEST_COST_WITH_MIN_ROAS. | [optional]
**budget** | [**\Zernio\Model\UpdateAdCampaignRequestBudget**](UpdateAdCampaignRequestBudget.md) |  | [optional]
**name** | **string** | **Meta only.** Rename the campaign. | [optional]
**platform_specific_data** | [**\Zernio\Model\UpdateAdCampaignRequestPlatformSpecificData**](UpdateAdCampaignRequestPlatformSpecificData.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
