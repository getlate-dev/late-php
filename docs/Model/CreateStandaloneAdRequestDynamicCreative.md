# # CreateStandaloneAdRequestDynamicCreative

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**image_urls** | **string[]** | Pool of image URLs (1-10). Uploaded to the ad account and referenced by hash in the asset feed. Mutually exclusive with &#x60;videoUrls&#x60;. | [optional]
**video_urls** | **string[]** | Pool of video URLs (1-10). Uploaded to the ad account and referenced by video id in the asset feed. No thumbnails are needed: Meta auto-generates a poster per video. Mutually exclusive with &#x60;imageUrls&#x60;; &#x60;adFormat&#x60; defaults to SINGLE_VIDEO. | [optional]
**bodies** | **string[]** | Primary-text variations (the body copy). | [optional]
**titles** | **string[]** | Headline variations. | [optional]
**descriptions** | **string[]** | Description (link caption) variations. | [optional]
**link_urls** | **string[]** | Destination URL variations. At least one is required unless &#x60;goal&#x60; is &#x60;lead_generation&#x60;. | [optional]
**call_to_action_types** | **string[]** | CTA-button variations. Required. | [optional]
**ad_format** | **string** | Asset-feed ad format. Must match the pool: SINGLE_IMAGE / CAROUSEL_IMAGE require &#x60;imageUrls&#x60;, SINGLE_VIDEO requires &#x60;videoUrls&#x60; (400 otherwise). Defaults to SINGLE_IMAGE with &#x60;imageUrls&#x60;, SINGLE_VIDEO with &#x60;videoUrls&#x60;. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
