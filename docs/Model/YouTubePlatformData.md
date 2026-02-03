# # YouTubePlatformData

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**title** | **string** | Video title. Defaults to first line of content or \&quot;Untitled Video\&quot;. Must be ≤ 100 characters. | [optional]
**visibility** | **string** | Video visibility setting: - public: Anyone can search for and watch (default) - unlisted: Only people with the link can watch - private: Only you and people you specifically share with can watch | [optional] [default to 'public']
**made_for_kids** | **bool** | COPPA compliance: Audience designation for the video. - true: Video is made for kids (child-directed content) - false: Video is NOT made for kids (default)  This field maps to YouTube&#39;s &#x60;selfDeclaredMadeForKids&#x60; setting. Videos marked as made for kids have restricted features (no comments, no notifications, limited ad targeting).  IMPORTANT: If not specified, defaults to false. YouTube requires this to be explicitly set, otherwise the video may be blocked from views until configured in YouTube Studio. | [optional] [default to false]
**first_comment** | **string** | Optional first comment to post immediately after video upload. Up to 10,000 characters (YouTube&#39;s comment limit). | [optional]
**contains_synthetic_media** | **bool** | AI-generated content disclosure flag. Set to true if your video contains AI-generated or synthetic content that could be mistaken for real people, places, or events. This helps viewers understand when realistic content has been created or altered using AI. YouTube may add a label to videos when this is set. Added to YouTube Data API in October 2024. | [optional] [default to false]
**category_id** | **string** | YouTube video category ID. Defaults to &#39;22&#39; (People &amp; Blogs). Common categories: 1 (Film &amp; Animation), 2 (Autos &amp; Vehicles), 10 (Music), 15 (Pets &amp; Animals), 17 (Sports), 20 (Gaming), 22 (People &amp; Blogs), 23 (Comedy), 24 (Entertainment), 25 (News &amp; Politics), 26 (Howto &amp; Style), 27 (Education), 28 (Science &amp; Technology). | [optional] [default to '22']

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
