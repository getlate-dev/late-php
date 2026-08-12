# # WebhookPayloadAdStatusChanged

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | Stable webhook event ID |
**event** | **string** |  |
**account** | [**\Zernio\Model\WebhookPayloadAdStatusChangedAccount**](WebhookPayloadAdStatusChangedAccount.md) |  |
**ad_object** | [**\Zernio\Model\WebhookPayloadAdStatusChangedAdObject**](WebhookPayloadAdStatusChangedAdObject.md) |  |
**status** | [**\Zernio\Model\WebhookPayloadAdStatusChangedStatus**](WebhookPayloadAdStatusChangedStatus.md) |  |
**error** | [**\Zernio\Model\WebhookPayloadAdStatusChangedError**](WebhookPayloadAdStatusChangedError.md) |  | [optional]
**timestamp** | **\DateTime** | UTC time at which Zernio generated this event (set once when the event payload is built, before delivery is queued). Retries and redeliveries keep the original value, so it reflects the event, not the delivery attempt. |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
