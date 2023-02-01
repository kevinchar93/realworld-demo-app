# ArticlesApi

All URIs are relative to */api*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createArticle**](ArticlesApi.md#createArticle) | **POST** /articles | Create an article |
| [**deleteArticle**](ArticlesApi.md#deleteArticle) | **DELETE** /articles/{slug} | Delete an article |
| [**getArticle**](ArticlesApi.md#getArticle) | **GET** /articles/{slug} | Get an article |
| [**getArticles**](ArticlesApi.md#getArticles) | **GET** /articles | Get recent articles globally |
| [**getArticlesFeed**](ArticlesApi.md#getArticlesFeed) | **GET** /articles/feed | Get recent articles from users you follow |
| [**updateArticle**](ArticlesApi.md#updateArticle) | **PUT** /articles/{slug} | Update an article |


<a name="createArticle"></a>
# **createArticle**
> CreateArticle_201_response createArticle(article)

Create an article

    Create an article. Auth is required

### Parameters

|Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **article** | [**CreateArticle_request**](../Models/CreateArticle_request.md)| Article to create | |

### Return type

[**CreateArticle_201_response**](../Models/CreateArticle_201_response.md)

### Authorization

[Token](../README.md#Token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

<a name="deleteArticle"></a>
# **deleteArticle**
> deleteArticle(slug)

Delete an article

    Delete an article. Auth is required

### Parameters

|Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **slug** | **String**| Slug of the article to delete | [default to null] |

### Return type

null (empty response body)

### Authorization

[Token](../README.md#Token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="getArticle"></a>
# **getArticle**
> CreateArticle_201_response getArticle(slug)

Get an article

    Get an article. Auth not required

### Parameters

|Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **slug** | **String**| Slug of the article to get | [default to null] |

### Return type

[**CreateArticle_201_response**](../Models/CreateArticle_201_response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="getArticles"></a>
# **getArticles**
> GetArticlesFeed_200_response getArticles(tag, author, favorited, offset, limit)

Get recent articles globally

    Get most recent articles globally. Use query parameters to filter results. Auth is optional

### Parameters

|Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **tag** | **String**| Filter by tag | [optional] [default to null] |
| **author** | **String**| Filter by author (username) | [optional] [default to null] |
| **favorited** | **String**| Filter by favorites of a user (username) | [optional] [default to null] |
| **offset** | **Integer**| The number of items to skip before starting to collect the result set. | [optional] [default to null] |
| **limit** | **Integer**| The numbers of items to return. | [optional] [default to 20] |

### Return type

[**GetArticlesFeed_200_response**](../Models/GetArticlesFeed_200_response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="getArticlesFeed"></a>
# **getArticlesFeed**
> GetArticlesFeed_200_response getArticlesFeed(offset, limit)

Get recent articles from users you follow

    Get most recent articles from users you follow. Use query parameters to limit. Auth is required

### Parameters

|Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **offset** | **Integer**| The number of items to skip before starting to collect the result set. | [optional] [default to null] |
| **limit** | **Integer**| The numbers of items to return. | [optional] [default to 20] |

### Return type

[**GetArticlesFeed_200_response**](../Models/GetArticlesFeed_200_response.md)

### Authorization

[Token](../README.md#Token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="updateArticle"></a>
# **updateArticle**
> CreateArticle_201_response updateArticle(slug, article)

Update an article

    Update an article. Auth is required

### Parameters

|Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **slug** | **String**| Slug of the article to update | [default to null] |
| **article** | [**UpdateArticle_request**](../Models/UpdateArticle_request.md)| Article to update | |

### Return type

[**CreateArticle_201_response**](../Models/CreateArticle_201_response.md)

### Authorization

[Token](../README.md#Token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

