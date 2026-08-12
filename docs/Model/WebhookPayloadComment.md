# # WebhookPayloadComment

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | Stable webhook event ID |
**event** | **string** |  |
**comment** | [**\Zernio\Model\WebhookPayloadCommentComment**](WebhookPayloadCommentComment.md) |  |
**post** | [**\Zernio\Model\WebhookPayloadCommentPost**](WebhookPayloadCommentPost.md) |  |
**account** | [**\Zernio\Model\WebhookPayloadCommentAccount**](WebhookPayloadCommentAccount.md) |  |
**timestamp** | **\DateTime** | UTC time at which Zernio generated this event (set once when the event payload is built, before delivery is queued). Retries and redeliveries keep the original value, so it reflects the event, not the delivery attempt. |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
