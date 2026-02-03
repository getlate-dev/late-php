# # ConnectBlueskyCredentialsRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**identifier** | **string** | Your Bluesky handle (e.g. user.bsky.social) or email address |
**app_password** | **string** | App password generated from Bluesky Settings &gt; App Passwords |
**state** | **string** | Required state parameter formatted as &#x60;{userId}-{profileId}&#x60;. - &#x60;userId&#x60;: Your Late user ID (get from &#x60;GET /v1/users&#x60; → &#x60;currentUserId&#x60;) - &#x60;profileId&#x60;: The profile ID to connect the account to (get from &#x60;GET /v1/profiles&#x60;) |
**redirect_uri** | **string** | Optional URL to redirect to after successful connection | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
