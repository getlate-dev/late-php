# # CreateAdCampaignRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **string** | Zernio SocialAccount id (posting or ads variant) used to resolve the Meta token. |
**ad_account_id** | **string** | Meta ad account id (act_&lt;n&gt;). |
**name** | **string** |  |
**goal** | **string** | Mapped to the ODAX objective (same mapping as POST /v1/ads/create). |
**special_ad_categories** | **string[]** |  | [optional]
**budget_amount** | **float** | Campaign-level (CBO) budget in WHOLE currency units (USD: 50 &#x3D; $50.00), NOT cents — Meta&#39;s own Marketing API takes this same number in minor units, so it is an easy and expensive mix-up. Requires budgetType. | [optional]
**budget_type** | **string** |  | [optional]
**status** | **string** |  | [optional] [default to 'PAUSED']
**bid_strategy** | **string** | Campaign bid strategy. Meta stores &#x60;bid_strategy&#x60; alongside the budget, so this REQUIRES &#x60;budgetAmount&#x60; + &#x60;budgetType&#x60; on the same request; sending it without a campaign budget is a 400. A campaign carrying a strategy without its &#x60;bid_amount&#x60; makes every ad set created under it fail with an error that names the ad set (code 100, subcode 1815857), so the bad state is rejected up front rather than accepted. To bid at ad-set level, set the strategy there instead. | [optional]
**bid_amount** | **float** | Whole currency units (USD: 5 &#x3D; $5.00). Required for LOWEST_COST_WITH_BID_CAP and COST_CAP; ignored otherwise. | [optional]
**roas_average_floor** | **float** | Decimal ROAS multiplier (2.0 &#x3D; 2.0x). Required for LOWEST_COST_WITH_MIN_ROAS. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
