# # FacebookPostEarningsResponseMetricsValue

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**total** | **float** | Lifetime earnings in \&quot;unit\&quot;, exactly as Meta returned them. Never rescaled. | [optional]
**unit** | **string** | \&quot;micro_amount\&quot;: Meta returned an object shape carrying a micro amount, and \&quot;total\&quot; is that integer, unconverted. Zernio does not publish a divisor because Meta does not document one; divide by the scale you have verified against the Page&#39;s own Meta Business Suite export. This is always content_monetization_earnings.  \&quot;unspecified\&quot;: Meta returned a bare number with no unit metadata, passed through as-is; Meta does not state whether it is major or minor currency units. This is always monetization_approximate_earnings. | [optional]
**currency** | **string** | ISO 4217 currency, or null when Meta omitted it. Always null on monetization_approximate_earnings; always present on content_monetization_earnings. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
