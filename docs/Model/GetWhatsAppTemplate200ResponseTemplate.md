# # GetWhatsAppTemplate200ResponseTemplate

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | Meta template id. Unique per language variant; usable on /v1/whatsapp/templates/id/{templateId}. | [optional]
**name** | **string** |  | [optional]
**status** | **string** |  | [optional]
**category** | **string** |  | [optional]
**language** | **string** | The variant actually returned. | [optional]
**components** | **object[]** |  | [optional]
**rejected_reason** | **string** | Only when status is REJECTED. | [optional]
**quality_score** | **object** | Post-approval quality (GREEN/YELLOW/RED), when Meta reports one. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
