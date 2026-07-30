# # GetWhatsAppCallingConfig200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**phone_number_doc_id** | **string** | Phone number record ID (use on /v1/phone-numbers/{id}/whatsapp/calling) | [optional]
**phone_number** | **string** |  | [optional]
**calling_enabled** | **bool** |  | [optional]
**call_deep_link** | **string** | Public calling deep link (https://wa.me/call/&lt;number&gt;). Tapping it on a phone starts a WhatsApp voice call to this number. Embed it on websites, emails, or QR codes. Null while calling is disabled; not supported by WhatsApp desktop clients. | [optional]
**forward_to** | **string** | tel:+E164 / sip:... / wss://... destination | [optional]
**recording_enabled** | **bool** |  | [optional]
**sip_auth_username** | **string** |  | [optional]
**sip_auth_password_configured** | **bool** | True when a SIP digest password is stored. The plaintext is never returned. | [optional]
**call_icon_countries** | **string[]** |  | [optional]
**caller_id_mode** | **string** | Caller ID the forward-leg callee sees on tel: forwards. business &#x3D; this WhatsApp number; platform &#x3D; a Zernio number (customer-brought number without verified caller ID; verify via /v1/phone-numbers/{id}/whatsapp/caller-id-verification). | [optional]
**caller_id_verified** | **bool** | True once the number completed caller-ID verification. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
