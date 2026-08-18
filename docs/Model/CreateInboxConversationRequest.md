# # CreateInboxConversationRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **string** | The social account ID to send from |
**participant_id** | **string** | Recipient identifier. For X this is the numeric user ID; for WhatsApp and SMS, the recipient phone number in international format (digits, country code included); for Slack, the workspace member id (e.g. U01ABCDEF). Provide either this or participantUsername. | [optional]
**participant_username** | **string** | Recipient handle/username — an X or Bluesky handle (with or without @) or a Reddit username (with or without u/). Resolved via lookup. Provide either this or participantId. | [optional]
**message** | **string** | Text content of the message. At least one of message, attachment, or (for WhatsApp) templateName is required. Required when category is set (a Direct Send utility message is a text message). | [optional]
**skip_dm_check** | **bool** | X/Twitter only. Skip the receives_your_dm eligibility check before sending. Use if you have already verified the recipient accepts DMs. | [optional] [default to false]
**template_name** | **string** | WhatsApp only. Name of the approved template to start the conversation with. Required for WhatsApp unless category is used instead (Direct Send). Cannot be combined with category. | [optional]
**category** | **string** | WhatsApp only (Meta Direct Send). Combined with message and without templateName, starts the conversation with a business-initiated UTILITY message and no pre-approved template; Meta matches or auto-creates a template asynchronously. The WhatsApp Business Account must be eligible for Direct Send, otherwise the send fails with an error telling you to use an approved message template instead. Cannot be combined with templateName (templates are already categorized at creation). Utility messages only; marketing content is not allowed under this category. Accepted on the JSON body only, not on multipart requests. | [optional]
**link_preview** | **bool** | WhatsApp only. Set false to send the Direct Send (category: &#39;utility&#39;) text message without a link-preview thumbnail for the first URL in the text. Defaults to true, which is how every WhatsApp text has been sent to date. Does not apply to template sends. Accepted on the JSON body only, not on multipart requests. | [optional] [default to true]
**template_language** | **string** | WhatsApp only. Template language code (e.g. en_US). | [optional]
**template_params** | **string[]** | WhatsApp only. Template variable values as one flat array, in the order the variables appear across the whole template: text-header variables first, then body variables, then one value per dynamic URL button (in button order). Works with positional placeholders ({{1}}, {{2}}, ...) and with named placeholders ({{name}}, {{company}} - how Meta Business Manager creates templates), where values fill the named slots in order of appearance. Example - a body with {{1}}, {{2}} plus a URL button https://example.com/{{1}} takes three values: [body1, body2, buttonSuffix]. Media headers (image, video, document) are filled automatically from the approved template and take no value here (use headerMedia to override the header asset per send). | [optional]
**header_media** | [**\Zernio\Model\CreateInboxConversationRequestHeaderMedia**](CreateInboxConversationRequestHeaderMedia.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
