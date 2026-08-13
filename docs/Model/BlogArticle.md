# # BlogArticle

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | Platform-native article id (numeric string for Shopify). | [optional]
**blog_id** | **string** | Platform-native id of the blog the article belongs to. | [optional]
**platform** | **string** |  | [optional]
**title** | **string** |  | [optional]
**body_html** | **string** | Article body as HTML. | [optional]
**handle** | **string** | URL slug of the article. | [optional]
**tags** | **string[]** |  | [optional]
**author** | **string** | Display name of the article author. | [optional]
**excerpt** | **string** | Short summary shown in blog listings. | [optional]
**image** | [**\Zernio\Model\BlogArticleImage**](BlogArticleImage.md) |  | [optional]
**is_published** | **bool** | False while the article is a draft or its publish date is still in the future. | [optional]
**published_at** | **\DateTime** | When the article was (or is scheduled to be) published; null for drafts. | [optional]
**created_at** | **\DateTime** |  | [optional]
**updated_at** | **\DateTime** |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
