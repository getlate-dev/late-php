# # ConnectionLog

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**_id** | **string** |  | [optional]
**user_id** | **string** | User who owns the connection (may be null for early OAuth failures) | [optional]
**profile_id** | **string** |  | [optional]
**account_id** | **string** | The social account ID (present on successful connections and disconnects) | [optional]
**platform** | **string** |  | [optional]
**event_type** | **string** | Type of connection event: - &#x60;connect_success&#x60; - New account connected successfully - &#x60;connect_failed&#x60; - Connection attempt failed - &#x60;disconnect&#x60; - Account was disconnected - &#x60;reconnect_success&#x60; - Existing account reconnected successfully - &#x60;reconnect_failed&#x60; - Reconnection attempt failed | [optional]
**connection_method** | **string** | How the connection was initiated | [optional]
**error** | [**\Late\Model\ConnectionLogError**](ConnectionLogError.md) |  | [optional]
**success** | [**\Late\Model\ConnectionLogSuccess**](ConnectionLogSuccess.md) |  | [optional]
**context** | [**\Late\Model\ConnectionLogContext**](ConnectionLogContext.md) |  | [optional]
**duration_ms** | **int** | How long the operation took in milliseconds | [optional]
**metadata** | **object** | Additional metadata | [optional]
**created_at** | **\DateTime** |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
