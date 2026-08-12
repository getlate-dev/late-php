# # ListLocalServicesLeads200ResponseDataInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | Lead id; pass to /v1/ads/local-services/leads/{leadId}/conversations. | [optional]
**lead_type** | **string** | PHONE_CALL / MESSAGE / BOOKING. | [optional]
**category_id** | **string** |  | [optional]
**service_id** | **string** |  | [optional]
**contact** | [**\Zernio\Model\ListLocalServicesLeads200ResponseDataInnerContact**](ListLocalServicesLeads200ResponseDataInnerContact.md) |  | [optional]
**status** | **string** |  | [optional]
**created_time** | **string** | Google datetime in the customer&#39;s timezone (YYYY-MM-DD HH:MM:SS). | [optional]
**locale** | **string** |  | [optional]
**charged** | **bool** |  | [optional]
**credit_state** | **string** |  | [optional]
**credit_state_last_update** | **string** |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
