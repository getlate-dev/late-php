# # WhatsAppHeaderComponentExample

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**header_text** | **string[]** | Sample values for header text variables | [optional]
**header_text_named_params** | [**\Zernio\Model\WhatsAppNamedParamExample[]**](WhatsAppNamedParamExample.md) | Sample values for NAMED header variables (templates using {{customer_name}}-style tokens with parameter_format: NAMED). | [optional]
**header_handle** | **string[]** | When the header format is a media type (image, video, gif, document), provide a public URL here. Zernio will download and upload it to WhatsApp on your behalf, replacing it with the internal file handle before creating the template. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
