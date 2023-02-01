# CommentsApi

All URIs are relative to */api*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createArticleComment**](CommentsApi.md#createArticleComment) | **POST** /articles/{slug}/comments | Create a comment for an article |
| [**deleteArticleComment**](CommentsApi.md#deleteArticleComment) | **DELETE** /articles/{slug}/comments/{id} | Delete a comment for an article |
| [**getArticleComments**](CommentsApi.md#getArticleComments) | **GET** /articles/{slug}/comments | Get comments for an article |


<a name="createArticleComment"></a>
# **createArticleComment**
> CreateArticleComment_200_response createArticleComment(slug, comment)

Create a comment for an article

    Create a comment for an article. Auth is required

### Parameters

|Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **slug** | **String**| Slug of the article that you want to create a comment for | [default to null] |
| **comment** | [**CreateArticleComment_request**](../Models/CreateArticleComment_request.md)| Comment you want to create | |

### Return type

[**CreateArticleComment_200_response**](../Models/CreateArticleComment_200_response.md)

### Authorization

[Token](../README.md#Token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

<a name="deleteArticleComment"></a>
# **deleteArticleComment**
> deleteArticleComment(slug, id)

Delete a comment for an article

    Delete a comment for an article. Auth is required

### Parameters

|Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **slug** | **String**| Slug of the article that you want to delete a comment for | [default to null] |
| **id** | **Integer**| ID of the comment you want to delete | [default to null] |

### Return type

null (empty response body)

### Authorization

[Token](../README.md#Token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="getArticleComments"></a>
# **getArticleComments**
> GetArticleComments_200_response getArticleComments(slug)

Get comments for an article

    Get the comments for an article. Auth is optional

### Parameters

|Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **slug** | **String**| Slug of the article that you want to get comments for | [default to null] |

### Return type

[**GetArticleComments_200_response**](../Models/GetArticleComments_200_response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

