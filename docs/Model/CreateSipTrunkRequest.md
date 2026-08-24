# # CreateSipTrunkRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**label** | **string** | Display name for the trunk. |
**sip_host** | **string** | Fully-qualified hostname inbound calls are delivered to (e.g. sip.rtc.elevenlabs.io, sip.retellai.com). |
**sip_port** | **int** | Defaults to 5061 for tls, 5060 otherwise. | [optional]
**transport** | **string** | Signaling transport toward sipHost. Default tls (with SRTP media). | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
