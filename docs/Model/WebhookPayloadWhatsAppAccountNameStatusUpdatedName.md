# # WebhookPayloadWhatsAppAccountNameStatusUpdatedName

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**status** | **string** | Normalized from Meta&#39;s &#x60;decision&#x60; (REJECTED -&gt; DECLINED, DEFERRED -&gt; PENDING_REVIEW; the review is still open on DEFERRED, not a rejection). |
**requested_name** | **string** | The display name Meta reviewed. Null if Meta did not send one. |
**rejection_reason** | **string** | Meta&#39;s free-form decline reason. Null on approval, or when Meta sends the literal string \&quot;NONE\&quot;. |
**display_phone_number** | **string** | The phone number this review is for, as Meta reported it. |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
