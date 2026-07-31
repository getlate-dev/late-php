# # BulkCreateContactsRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**profile_id** | **string** |  |
**account_id** | **string** | Required when contacts carry channel data (platformIdentifier or a row-level accountId). Omit for a plain CRM import with no channels. | [optional]
**platform** | **string** | Ignored when accountId is set: the platform is derived from the resolved account. Only relevant to disambiguate accountId lookup; a mismatch 404s. | [optional]
**contacts** | [**\Zernio\Model\BulkCreateContactsRequestContactsInner[]**](BulkCreateContactsRequestContactsInner.md) |  |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
