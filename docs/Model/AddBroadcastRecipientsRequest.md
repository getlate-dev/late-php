# # AddBroadcastRecipientsRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**contact_ids** | **string[]** | Specific contact IDs to add. Zernio contact ids (24-character hex), as returned by the list-contacts endpoint. A platform identifier such as a WhatsApp wa_id is rejected with 400; use phones for raw numbers. | [optional]
**phones** | **string[]** | Raw phone numbers (auto-creates contacts). Useful for WhatsApp/Telegram manual entry | [optional]
**use_segment** | **bool** | Auto-populate from broadcast segment filters | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
