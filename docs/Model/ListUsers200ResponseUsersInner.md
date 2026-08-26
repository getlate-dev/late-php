# # ListUsers200ResponseUsersInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**_id** | **string** |  | [optional]
**name** | **string** |  | [optional]
**email** | **string** |  | [optional]
**role** | **string** |  | [optional]
**is_root** | **bool** |  | [optional]
**profile_access** | **string[]** |  | [optional]
**created_at** | **\DateTime** |  | [optional]
**last_login_at** | **\DateTime** | Last sign-in, stamped at most once an hour, so it is accurate to within an hour rather than to the exact session. Omitted for members with no recorded sign-in since the field shipped, which does not mean they never signed in. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
