# # CustomConversionResult

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ad_account_id** | **string** |  | [optional]
**custom_conversion_id** | **string** | Drops straight into promotedObject.customConversionId on POST /v1/ads/create. | [optional]
**reused** | **bool** | True when an existing conversion matched name + pixelId; the response is then a 200. | [optional]
**custom_conversion** | [**\Zernio\Model\CustomConversion**](CustomConversion.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
