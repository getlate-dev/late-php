# # WebhookPayloadWhatsAppTemplateCategoryUpdatedTemplate

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**template_id** | **string** | Meta&#39;s &#x60;message_template_id&#x60;, returned as a string. |
**name** | **string** | Meta&#39;s &#x60;message_template_name&#x60;. |
**language** | **string** | Meta&#39;s &#x60;message_template_language&#x60; (e.g. &#x60;en_US&#x60;). |
**change_type** | **string** | &#x60;scheduled&#x60; is Meta&#39;s 24h advance notice of an upcoming reclassification; &#x60;applied&#x60; is the change taking effect. |
**category** | **string** | The category right now, regardless of changeType. |
**previous_category** | **string** | Present only when changeType is &#x60;applied&#x60;. The category before this change. | [optional]
**scheduled_category** | **string** | Present only when changeType is &#x60;scheduled&#x60;. The category that will take effect at &#x60;effectiveAt&#x60;. | [optional]
**effective_at** | **\DateTime** | Present only when changeType is &#x60;scheduled&#x60;. ISO-8601 timestamp when the scheduled category takes effect. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
