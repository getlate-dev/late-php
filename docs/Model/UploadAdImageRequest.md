# # UploadAdImageRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **string** | Zernio SocialAccount id (posting or ads variant); its platform decides where the campaign is created. |
**ad_account_id** | **string** | Platform ad account id (Meta act_&lt;n&gt;, Google customer id, LinkedIn account id, ...). |
**image_base64** | **string** | Raw base64 image bytes, or a full data URL (the data:image/...;base64, prefix is stripped). |
**filename** | **string** | Optional filename shown in Meta&#39;s image library. Defaults to ad_image.jpg. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
