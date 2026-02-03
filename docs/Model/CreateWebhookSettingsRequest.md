# # CreateWebhookSettingsRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** | Webhook name (max 50 characters) | [optional]
**url** | **string** | Webhook endpoint URL (must be HTTPS in production) | [optional]
**secret** | **string** | Secret key for HMAC-SHA256 signature verification | [optional]
**events** | **string[]** | Events to subscribe to | [optional]
**is_active** | **bool** | Enable or disable webhook delivery | [optional]
**custom_headers** | **array<string,string>** | Custom headers to include in webhook requests | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
