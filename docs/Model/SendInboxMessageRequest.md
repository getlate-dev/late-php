# # SendInboxMessageRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **string** | Social account ID |
**message** | **string** | Message text | [optional]
**quick_replies** | [**\Late\Model\SendInboxMessageRequestQuickRepliesInner[]**](SendInboxMessageRequestQuickRepliesInner.md) | Quick reply buttons. Mutually exclusive with buttons. Max 13 items. | [optional]
**buttons** | [**\Late\Model\SendInboxMessageRequestButtonsInner[]**](SendInboxMessageRequestButtonsInner.md) | Action buttons. Mutually exclusive with quickReplies. Max 3 items. | [optional]
**template** | [**\Late\Model\SendInboxMessageRequestTemplate**](SendInboxMessageRequestTemplate.md) |  | [optional]
**reply_markup** | [**\Late\Model\SendInboxMessageRequestReplyMarkup**](SendInboxMessageRequestReplyMarkup.md) |  | [optional]
**messaging_type** | **string** | Facebook messaging type. Required when using messageTag. | [optional]
**message_tag** | **string** | Facebook message tag for messaging outside 24h window. Requires messagingType MESSAGE_TAG. Instagram only supports HUMAN_AGENT. | [optional]
**reply_to** | **string** | Platform message ID to reply to (Telegram only). | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
