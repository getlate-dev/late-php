# # GetInboxConversation200ResponseDataMetadata

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**meta_ad_id** | **string** | The Meta ad ID the user clicked. Always present when a referral was captured. | [optional]
**meta_ad_source** | **string** | Meta-supplied source identifier, for example ADS. | [optional]
**meta_ad_type** | **string** | Meta-supplied referral type, for example OPEN_THREAD. | [optional]
**meta_ad_ref** | **string** | The ref parameter passed through from the ad creative. | [optional]
**meta_ad_title** | **string** | Title of the ad creative at click time. | [optional]
**meta_ad_photo_url** | **string** | Image of the ad creative at click time. | [optional]
**meta_ad_video_url** | **string** | Video of the ad creative at click time. | [optional]
**meta_ad_post_id** | **string** | The organic post the ad promoted, when the ad was a boosted post. | [optional]
**meta_ad_product_id** | **string** | The catalogue product the user clicked, for product ads. | [optional]
**meta_ad_flow_id** | **string** | The Meta flow the ad launched, for flow ads. | [optional]
**meta_ad_captured_at** | **\DateTime** | When Zernio stored this referral. Always present when a referral was captured. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
