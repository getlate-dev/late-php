# # GetMediaPresignedUrl200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**upload_url** | **string** | Presigned URL to PUT your file to (expires in 1 hour) | [optional]
**public_url** | **string** | Public URL where the file will be accessible after upload. Served from the temp/ prefix by default (expires 7 days after upload) or from media/ when permanent is true. | [optional]
**key** | **string** | Storage key/path of the file. Prefixed temp/ by default, media/ when permanent is true. | [optional]
**expires_in** | **int** | Seconds until the presigned uploadUrl expires (always 3600) | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
