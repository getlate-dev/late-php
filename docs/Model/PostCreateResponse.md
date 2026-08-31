# # PostCreateResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message** | **string** |  | [optional]
**post** | [**\Zernio\Model\Post**](Post.md) |  | [optional]
**warnings** | **string[]** | Advisory notices about a post that was still created: media truncated for a platform, a recycling caveat, or a field that was ignored because it sat outside platforms[].platformSpecificData. Absent when there are none. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
