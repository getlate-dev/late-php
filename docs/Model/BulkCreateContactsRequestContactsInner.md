# # BulkCreateContactsRequestContactsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** |  |
**platform_identifier** | **string** | Required when the top-level accountId is set (channel mode). A row missing it in that mode is rejected individually and reported in errors[], not a 400 for the whole import. | [optional]
**display_identifier** | **string** |  | [optional]
**email** | **string** |  | [optional]
**company** | **string** |  | [optional]
**tags** | **string[]** |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
