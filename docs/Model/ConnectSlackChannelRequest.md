# # ConnectSlackChannelRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**profile_id** | **string** |  |
**channel_id** | **string** | Slack channel id, C... or G... |
**pending_data_token** | **string** | Nonce from the OAuth redirect. Required unless accountId is sent. | [optional]
**account_id** | **string** | Existing Slack account whose workspace token is reused. Required unless pendingDataToken is sent. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
