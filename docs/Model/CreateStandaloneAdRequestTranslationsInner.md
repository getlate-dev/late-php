# # CreateStandaloneAdRequestTranslationsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**locale** | **string** | Language code, resolved to Meta&#39;s numeric locale id. Bare codes target the &#39;(All)&#39; umbrella (&#x60;es&#x60; &#x3D; every Spanish variant); region-qualified codes target the variant (&#x60;pt_BR&#x60;, &#x60;en_GB&#x60;). |
**headline** | **string** | Headline for this language. Inherits the top-level &#x60;headline&#x60; when omitted. | [optional]
**body** | **string** | Primary text for this language. Inherits the top-level &#x60;body&#x60; when omitted. | [optional]
**description** | **string** | Link description for this language. Inherits the top-level &#x60;description&#x60; when omitted. | [optional]
**image_url** | **string** | Image for this language. Inherits the ad&#39;s &#x60;imageUrl&#x60; when omitted. The feed is all-image OR all-video. | [optional]
**video_url** | **string** | Video for this language. Inherits the ad&#39;s &#x60;video.url&#x60; when omitted. The feed is all-image OR all-video. | [optional]
**thumbnail_url** | **string** | Poster frame for this language&#39;s video. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
