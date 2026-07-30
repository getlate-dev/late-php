# # UpdateWhatsAppCallingLegacyRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **string** |  |
**forward_to** | **string** |  | [optional]
**sip_auth_username** | **string** |  | [optional]
**sip_auth_password** | **string** |  | [optional]
**recording_enabled** | **bool** |  | [optional]
**call_icon_countries** | **string[]** |  | [optional]
**max_call_duration_seconds** | **int** | Hard cap (seconds) on forwarded calls; null clears the cap. | [optional]
**forward_caller_id** | **string** | caller &#x3D; present the WhatsApp user&#39;s number to the forward destination (sip: only). | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
