# # UpdateCommentAutomationRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** |  | [optional]
**trigger** | **string** | What fires the automation. Changing it detaches the automation from its bound post or story (a post id and a story id are different objects), unless this same request sets a new binding. &#39;story_reply&#39; is Instagram only. | [optional]
**keywords** | **string[]** |  | [optional]
**match_mode** | **string** | How a keyword is compared with the comment. &#39;contains&#39; (default) matches anywhere, even inside another word (keyword &#39;app&#39; fires on &#39;happy&#39;). &#39;word&#39; matches the keyword only as a standalone word. &#39;exact&#39; requires the whole comment to be exactly the keyword. | [optional]
**exclude_keywords** | **string[]** | Comments containing one of these never trigger the automation, even when a trigger keyword also matches. Compared using the same matchMode. | [optional]
**typo_tolerance** | **bool** | Only with matchMode&#x3D;word: also fire on close misspellings of a keyword (one edit for 4-7 character keywords, two from 8 up). Keywords shorter than 4 characters are never fuzzy-matched. | [optional]
**dm_message** | **string** |  | [optional]
**buttons** | [**\Zernio\Model\DmButton[]**](DmButton.md) | Inline DM buttons (1-3). Pass [] to clear all buttons. | [optional]
**comment_reply** | **string** |  | [optional]
**dm_message_variations** | **string[]** | Alternate DM texts for random rotation (see create). Pass [] to clear. | [optional]
**comment_reply_variations** | **string[]** | Alternate public replies for random rotation. Pass [] to clear. | [optional]
**link_tracking** | **bool** | Wrap link buttons in a tracked redirect to count clicks. Pass false to send links untouched. | [optional]
**click_tag** | **string** | Tag applied to a contact when they click a tracked link (requires linkTracking). Empty string clears it. | [optional]
**audience** | [**\Zernio\Model\CommentAutomationAudience**](CommentAutomationAudience.md) |  | [optional]
**follow_gate** | [**\Zernio\Model\CommentAutomationFollowGate**](CommentAutomationFollowGate.md) |  | [optional]
**is_active** | **bool** |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
