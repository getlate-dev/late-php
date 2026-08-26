# # GoogleBusinessReview

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | Review ID | [optional]
**name** | **string** | Full resource name | [optional]
**reviewer** | [**\Zernio\Model\GoogleBusinessReviewReviewer**](GoogleBusinessReviewReviewer.md) |  | [optional]
**rating** | **int** | Numeric star rating (0 when Google sends no rating) | [optional]
**star_rating** | **string** | Google&#39;s string rating | [optional]
**comment** | **string** | Review text | [optional]
**create_time** | **\DateTime** |  | [optional]
**update_time** | **\DateTime** |  | [optional]
**review_reply** | [**\Zernio\Model\GoogleBusinessReviewReviewReply**](GoogleBusinessReviewReviewReply.md) |  | [optional]
**photo_count** | **int** | Number of photos attached to the review (photos only, videos are not counted) | [optional]
**photos** | [**\Zernio\Model\ListInboxReviews200ResponseDataInnerPhotosInner[]**](ListInboxReviews200ResponseDataInnerPhotosInner.md) | Photos attached to the review by the reviewer | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
