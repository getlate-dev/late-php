# # EnableWhatsAppCallingLegacyRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **string** |  |
**forward_to** | **string** | tel:+E164 / sip:... / wss://... destination |
**sip_auth_username** | **string** |  | [optional]
**sip_auth_password** | **string** | Stored encrypted, never returned by any endpoint. | [optional]
**recording_enabled** | **bool** |  | [optional] [default to false]
**call_icon_countries** | **string[]** |  | [optional]
**max_call_duration_seconds** | **int** | Hard cap (seconds) on a forwarded call; the carrier hangs up both legs when it fires. Safety valve against dead-air billing when a destination hangs up but the signal is lost. | [optional]
**forward_caller_id** | **string** | Caller ID presented to the forward destination. caller &#x3D; the WhatsApp user&#39;s number (sip: destinations only; ignored on tel: forwards). Fixes AI-agent trunks that reject seeing the business number call itself. | [optional] [default to 'business']

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
