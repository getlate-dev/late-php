# # UpdateValueRuleSetRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **string** | Zernio SocialAccount id (posting or ads variant); its platform decides where the campaign is created. |
**name** | **string** | Required: the update replaces the whole set. |
**rules** | [**\Zernio\Model\ValueRule[]**](ValueRule.md) | The COMPLETE rule list. Omitting a rule deletes it on Meta. |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
