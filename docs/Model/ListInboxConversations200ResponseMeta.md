# # ListInboxConversations200ResponseMeta

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**accounts_queried** | **int** |  | [optional]
**accounts_failed** | **int** |  | [optional]
**failed_accounts** | [**\Zernio\Model\ListInboxConversations200ResponseMetaFailedAccountsInner[]**](ListInboxConversations200ResponseMetaFailedAccountsInner.md) |  | [optional]
**last_updated** | **\DateTime** |  | [optional]
**accounts_skipped** | [**\Zernio\Model\ListInboxConversations200ResponseMetaAccountsSkippedInner[]**](ListInboxConversations200ResponseMetaAccountsSkippedInner.md) | Connected accounts that were not queried: their platform does not support this feature, or the account is not enabled for it | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
