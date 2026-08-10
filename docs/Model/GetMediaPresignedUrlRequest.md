# # GetMediaPresignedUrlRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**filename** | **string** | Name of the file to upload |
**content_type** | **string** | MIME type of the file |
**size** | **int** | Optional file size in bytes for pre-validation (max 5GB) | [optional]
**permanent** | **bool** | Write the file to permanent storage instead of temporary storage. Temporary files auto-delete 7 days after upload; permanent files never expire. | [optional] [default to false]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
