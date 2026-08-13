# # CreateBlogArticleRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**title** | **string** |  |
**body_html** | **string** | Article body as HTML. | [optional]
**handle** | **string** | URL slug. Generated from the title when omitted. | [optional]
**tags** | **string[]** |  | [optional]
**author** | **string** | Display name of the article author. | [optional]
**excerpt** | **string** | Short summary shown in blog listings. | [optional]
**image** | [**\Zernio\Model\CreateBlogArticleRequestImage**](CreateBlogArticleRequestImage.md) |  | [optional]
**seo** | [**\Zernio\Model\CreateBlogArticleRequestSeo**](CreateBlogArticleRequestSeo.md) |  | [optional]
**is_published** | **bool** | Set false to create the article as a draft. | [optional]
**publish_date** | **\DateTime** | ISO 8601 datetime with offset (or Z). A future date schedules publication natively on the platform. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
