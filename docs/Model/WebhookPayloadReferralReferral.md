# # WebhookPayloadReferralReferral

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ref** | **string** | The &#x60;ref&#x60; parameter of the clicked ig.me / m.me link or ad. | [optional]
**source** | **string** | Meta-supplied source (&#x60;SHORTLINK&#x60;, &#x60;SHORTLINKS&#x60;, &#x60;IGME-SOURCE-LINK&#x60;, &#x60;ADS&#x60; - treat as opaque). | [optional]
**type** | **string** | Meta-supplied referral type (e.g. &#x60;OPEN_THREAD&#x60;). | [optional]
**referer_uri** | **string** | URI of the originating site, when Meta supplies one. Facebook Messenger only. | [optional]
**ad_id** | **string** | The Meta ad ID, on returning ad clicks. Facebook Messenger only. | [optional]
**ads_context_data** | [**\Zernio\Model\WebhookPayloadReferralReferralAdsContextData**](WebhookPayloadReferralReferralAdsContextData.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
