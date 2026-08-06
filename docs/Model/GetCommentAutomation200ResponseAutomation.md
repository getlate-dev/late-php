# # GetCommentAutomation200ResponseAutomation

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** |  | [optional]
**name** | **string** |  | [optional]
**platform** | **string** |  | [optional]
**trigger** | **string** |  | [optional]
**account_id** | **string** |  | [optional]
**platform_post_id** | **string** |  | [optional]
**post_id** | **string** |  | [optional]
**post_title** | **string** |  | [optional]
**keywords** | **string[]** |  | [optional]
**match_mode** | **string** | How a keyword is compared with the comment. &#39;contains&#39; (default) matches anywhere, even inside another word (keyword &#39;app&#39; fires on &#39;happy&#39;). &#39;word&#39; matches the keyword only as a standalone word. &#39;exact&#39; requires the whole comment to be exactly the keyword. | [optional]
**exclude_keywords** | **string[]** | Comments containing one of these never trigger the automation, even when a trigger keyword also matches. Compared using the same matchMode. | [optional]
**typo_tolerance** | **bool** | Only with matchMode&#x3D;word: also fire on close misspellings of a keyword (one edit for 4-7 character keywords, two from 8 up). Keywords shorter than 4 characters are never fuzzy-matched. | [optional]
**dm_message** | **string** |  | [optional]
**buttons** | [**\Zernio\Model\DmButton[]**](DmButton.md) | Inline DM buttons (up to 3). Omitted when none are set. | [optional]
**comment_reply** | **string** |  | [optional]
**dm_message_variations** | **string[]** | Alternate DM texts rotated at random with dmMessage. Omitted when none. | [optional]
**comment_reply_variations** | **string[]** | Alternate public replies rotated at random with commentReply. Omitted when none. | [optional]
**link_tracking** | **bool** |  | [optional]
**click_tag** | **string** |  | [optional]
**is_active** | **bool** |  | [optional]
**stats** | [**\Zernio\Model\CreateCommentAutomation200ResponseAutomationStats**](CreateCommentAutomation200ResponseAutomationStats.md) |  | [optional]
**created_at** | **\DateTime** |  | [optional]
**updated_at** | **\DateTime** |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
