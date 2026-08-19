# # ListLeads200ResponseLeadsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | Zernio lead id. | [optional]
**leadgen_id** | **string** | Meta lead id. On LinkedIn, the leadFormResponse id. | [optional]
**form_id** | **string** |  | [optional]
**form_name** | **string** |  | [optional]
**account_id** | **string** |  | [optional]
**ad_id** | **string** |  | [optional]
**adset_id** | **string** |  | [optional]
**campaign_id** | **string** | On LinkedIn, this is the LinkedIn Campaign id, which corresponds to platformAdSetId on GET /v1/ads (LinkedIn&#39;s Campaign Group is Zernio&#39;s campaign). | [optional]
**is_organic** | **bool** |  | [optional]
**created_time** | **string** | ISO 8601. | [optional]
**fields** | **array<string,string>** | Question key → answer. On LinkedIn, the key is the lowercased predefinedField, else the question name, else the numeric questionId; multiple-choice values are option labels (unlike Meta, which returns the option key). | [optional]
**field_data** | **object[]** | Raw Meta field_data. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
