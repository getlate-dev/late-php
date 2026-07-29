# # InstagramPlatformDataUserTagsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**username** | **string** | Instagram username (@ symbol is optional and will be removed automatically) |
**x** | **float** | X coordinate position from left edge (0.0 &#x3D; left, 0.5 &#x3D; center, 1.0 &#x3D; right). Required for photos, ignored for Reels/videos, optional for stories. | [optional]
**y** | **float** | Y coordinate position from top edge (0.0 &#x3D; top, 0.5 &#x3D; center, 1.0 &#x3D; bottom). Required for photos, ignored for Reels/videos, optional for stories. | [optional]
**media_index** | **int** | Zero-based index of the carousel item to tag. Defaults to 0. Tags on out-of-range indices are ignored. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
