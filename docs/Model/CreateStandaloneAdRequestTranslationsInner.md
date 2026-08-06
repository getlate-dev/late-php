# # CreateStandaloneAdRequestTranslationsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**locale** | **string** | Language code, resolved to Meta&#39;s numeric locale id. Bare codes target the &#39;(All)&#39; umbrella (&#x60;es&#x60; &#x3D; every Spanish variant); region-qualified codes target the variant (&#x60;pt_BR&#x60;, &#x60;en_GB&#x60;). |
**headline** | **string** | Headline for this language. REQUIRED, and must differ from every other locale and from the ad&#39;s top-level headline. |
**body** | **string** | Primary text for this language. REQUIRED, and must differ from every other locale and from the ad&#39;s top-level body. |
**description** | **string** | Link description for this language. REQUIRED, and must differ from every other locale and from the ad&#39;s top-level description. |
**link_url** | **string** | Destination URL for this language. Inherits the ad&#39;s top-level &#x60;linkUrl&#x60; when omitted, and requires it to be present (400 otherwise): the top-level URL is the destination for every locale you did not override. Unlike text, identical URLs across locales are fine (they share one asset). | [optional]
**image_url** | **string** | Image for this language. Inherits the ad&#39;s &#x60;imageUrl&#x60; when omitted. The feed is all-image OR all-video. | [optional]
**video_url** | **string** | Video for this language. Inherits the ad&#39;s &#x60;video.url&#x60; when omitted. The feed is all-image OR all-video. | [optional]
**thumbnail_url** | **string** | Poster frame for this language&#39;s video. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
