# # GetCommentAutomation200ResponseLogsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** |  | [optional]
**comment_id** | **string** |  | [optional]
**commenter_id** | **string** |  | [optional]
**commenter_name** | **string** |  | [optional]
**comment_text** | **string** |  | [optional]
**status** | **string** | DM outcome. &#39;pending&#39; &#x3D; the automation has a dmDelaySeconds and the response is queued but not sent yet. &#39;gated&#39; &#x3D; the follow-gate confirmation DM went out and we are waiting for the tap; it flips to &#39;sent&#39; or &#39;skipped&#39; when they tap. | [optional]
**audience_outcome** | **string** | How the audience rule resolved. Absent on automations without one. | [optional]
**commenter_is_follower** | **bool** | Follow relationship at decision time. Absent when Instagram would not tell us (the commenter never messaged the account). | [optional]
**commenter_follower_count** | **int** |  | [optional]
**error** | **string** | DM error message if status is failed | [optional]
**comment_reply_status** | **string** | Outcome of the optional public reply on the triggering comment. &#39;skipped&#39; if no commentReply was configured or if the DM failed (the public reply is not attempted in that case). | [optional]
**comment_reply_error** | **string** | Public-reply error message if commentReplyStatus is failed | [optional]
**next_due_at** | **\DateTime** | When the next queued send fires. Present only while something is still pending. | [optional]
**created_at** | **\DateTime** |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
