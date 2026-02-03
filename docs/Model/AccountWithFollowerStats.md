# # AccountWithFollowerStats

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**_id** | **string** |  | [optional]
**platform** | **string** |  | [optional]
**profile_id** | [**\Late\Model\SocialAccountProfileId**](SocialAccountProfileId.md) |  | [optional]
**username** | **string** |  | [optional]
**display_name** | **string** |  | [optional]
**profile_url** | **string** | Full profile URL for the connected account. Available for all platforms: - Twitter/X: https://x.com/{username} - Instagram: https://instagram.com/{username} - TikTok: https://tiktok.com/@{username} - YouTube: https://youtube.com/@{handle} or https://youtube.com/channel/{id} - LinkedIn Personal: https://www.linkedin.com/in/{vanityName}/ - LinkedIn Organization: https://www.linkedin.com/company/{vanityName}/ - Threads: https://threads.net/@{username} - Pinterest: https://pinterest.com/{username} - Reddit: https://reddit.com/user/{username} - Bluesky: https://bsky.app/profile/{handle} - Facebook: https://facebook.com/{username} or https://facebook.com/{pageId} - Google Business: Google Maps URL for the business location | [optional]
**is_active** | **bool** |  | [optional]
**followers_count** | **float** | Follower count (only included if user has analytics add-on) | [optional]
**followers_last_updated** | **\DateTime** | Last time follower count was updated (only included if user has analytics add-on) | [optional]
**profile_picture** | **string** |  | [optional]
**current_followers** | **float** | Current follower count | [optional]
**last_updated** | **\DateTime** |  | [optional]
**growth** | **float** | Follower change over period | [optional]
**growth_percentage** | **float** | Percentage growth | [optional]
**data_points** | **float** | Number of historical snapshots | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
