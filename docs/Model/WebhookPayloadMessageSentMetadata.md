# # WebhookPayloadMessageSentMetadata

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**quoted_message_id** | **string** | platformMessageId of the message this send is a quote-reply to. Set when the reply was sent through Zernio with &#x60;replyTo&#x60; on the inbox send API (WhatsApp and Telegram), and when the operator replied from the native WhatsApp Business, Instagram or Messenger app. WhatsApp API sends carry it on the event fired from the delivery status, so it arrives on the same &#x60;message.sent&#x60; as any other WhatsApp send. | [optional]
**thread_ts** | **string** | Slack only. Parent thread ts of the sent message. Pass it back as &#x60;replyTo&#x60; on the inbox send API to keep replying inside the thread. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
