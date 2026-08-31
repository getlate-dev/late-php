# # WebhookPayloadMessageSentMessageSender

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | The Zernio account id of the connected account that sent the message, not a contact id. |
**contact_id** | **string** | Always omitted on this event: the sender is the business, not a contact. Use conversation.contactId to join back to the CRM Contact. | [optional]
**name** | **string** | Display name of your connected account. | [optional]
**username** | **string** | Username of your connected account. | [optional]
**picture** | **string** | Profile picture of your connected account. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
