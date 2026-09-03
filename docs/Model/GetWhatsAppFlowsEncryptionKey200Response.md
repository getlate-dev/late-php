# # GetWhatsAppFlowsEncryptionKey200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**public_key** | **string** | The registered RSA public key in PEM format, or null when none is registered. | [optional]
**signature_status** | **string** | VALID (key matches Meta&#39;s records) or MISMATCH (no key registered, or the key does not match); null when unknown. | [optional]
**registered** | **bool** | Whether a key is currently registered. Derived from publicKey, not signatureStatus. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
