# # Webhook

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**_id** | **string** | Unique webhook identifier | [optional]
**name** | **string** | Webhook name (for identification) | [optional]
**url** | **string** | Webhook endpoint URL | [optional]
**secret** | **string** | Secret key for HMAC-SHA256 signature verification. | [optional]
**events** | **string[]** | Events subscribed to | [optional]
**is_active** | **bool** | Whether webhook delivery is enabled | [optional]
**last_fired_at** | **\DateTime** | Timestamp of last successful webhook delivery | [optional]
**failure_count** | **int** | Consecutive terminal delivery failures (resets to 0 on any successful delivery). Auto-disable only triggers when the endpoint has had no successful delivery within a 3-day window AND either reaches 20 consecutive terminal failures or has been failing continuously for 3 days; any success within that window keeps the endpoint enabled regardless of the count. | [optional]
**custom_headers** | **array<string,string>** | Custom headers included in webhook requests | [optional]
**disabled_resource_groups** | **string[]** | Resource groups this subscription does not receive (opt-out denylist, same vocabulary and same semantics as the field on API keys). Absent or empty means the subscription receives every event listed in &#x60;events&#x60;, which is how every subscription created before this field existed behaves. An event whose group is listed here is dropped before delivery even when it is still present in &#x60;events&#x60;, and the same check runs on every replay path (test fire, redelivery, dead-letter requeue). Editing the denylist applies to every event emitted afterwards; events already queued when the edit landed can still be delivered for up to five minutes after they were enqueued. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
