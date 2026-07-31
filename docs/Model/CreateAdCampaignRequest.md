# # CreateAdCampaignRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **string** | Zernio SocialAccount id (posting or ads variant) used to resolve the Meta token. |
**ad_account_id** | **string** | Meta ad account id (act_&lt;n&gt;). |
**name** | **string** |  |
**goal** | **string** | Mapped to the ODAX objective (same mapping as POST /v1/ads/create). |
**special_ad_categories** | **string[]** |  | [optional]
**budget_amount** | **float** | Campaign-level (CBO) budget in whole currency units. Requires budgetType. | [optional]
**budget_type** | **string** |  | [optional]
**status** | **string** |  | [optional] [default to 'PAUSED']
**bid_strategy** | **string** | Campaign bid strategy. Meta puts &#x60;bid_strategy&#x60; where the budget lives, so this applies only alongside a campaign budget (CBO). Previously settable only via &#x60;PUT /v1/ads/campaigns/{campaignId}&#x60;. | [optional]
**bid_amount** | **float** | Whole currency units (USD: 5 &#x3D; $5.00). Required for LOWEST_COST_WITH_BID_CAP and COST_CAP; ignored otherwise. | [optional]
**roas_average_floor** | **float** | Decimal ROAS multiplier (2.0 &#x3D; 2.0x). Required for LOWEST_COST_WITH_MIN_ROAS. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
