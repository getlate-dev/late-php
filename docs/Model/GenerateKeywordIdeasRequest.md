# # GenerateKeywordIdeasRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **string** | Zernio googleads SocialAccount id. |
**customer_id** | **string** | Numeric Google Ads customer id (no dashes); only needed when the connection has several accounts. | [optional]
**seed_keywords** | **string[]** | Seed terms. Provide these, seedUrl, or both. | [optional]
**seed_url** | **string** | Landing page to mine for ideas. Provide this, seedKeywords, or both. | [optional]
**countries** | **string[]** | ISO 3166-1 alpha-2 country codes. Omitted &#x3D; worldwide. | [optional]
**language_constant_id** | **string** | Google languageConstant id (1000 &#x3D; English). | [optional] [default to '1000']
**network** | **string** |  | [optional] [default to 'GOOGLE_SEARCH']
**include_adult_keywords** | **bool** |  | [optional]
**page_size** | **int** |  | [optional]
**page_token** | **string** | Cursor from paging.nextPageToken of the previous page. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
