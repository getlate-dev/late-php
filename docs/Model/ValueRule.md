# # ValueRule

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | Platform rule id. Echo it on &#x60;PUT&#x60; to KEEP this rule, omit it to CREATE a new one. A rule left out of the array entirely is DELETED. | [optional]
**name** | **string** |  |
**adjust_sign** | **string** | Direction of the adjustment. There is no signed value field. |
**adjust_value** | **int** | Unsigned percentage magnitude. &#x60;INCREASE&#x60; accepts 1-1000, &#x60;DECREASE&#x60; accepts 1-90. 0 is out of range on both. |
**status** | **string** | Meta returns &#x60;ACTIVE&#x60; here but documents no enum for the field. Treat it as a passthrough: echo whatever the &#x60;GET&#x60; returned, and do not synthesize values. | [optional]
**criteria** | [**\Zernio\Model\ValueRuleCriterion[]**](ValueRuleCriterion.md) | All criteria on a rule must match for the rule to fire. |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
