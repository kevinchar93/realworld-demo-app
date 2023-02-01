# FavoritesApi

All URIs are relative to */api*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createArticleFavorite**](FavoritesApi.md#createArticleFavorite) | **POST** /articles/{slug}/favorite | Favorite an article |
| [**deleteArticleFavorite**](FavoritesApi.md#deleteArticleFavorite) | **DELETE** /articles/{slug}/favorite | Unfavorite an article |


<a name="createArticleFavorite"></a>
# **createArticleFavorite**
> CreateArticle_201_response createArticleFavorite(slug)

Favorite an article

    Favorite an article. Auth is required

### Parameters

|Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **slug** | **String**| Slug of the article that you want to favorite | [default to null] |

### Return type

[**CreateArticle_201_response**](../Models/CreateArticle_201_response.md)

### Authorization

[Token](../README.md#Token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="deleteArticleFavorite"></a>
# **deleteArticleFavorite**
> CreateArticle_201_response deleteArticleFavorite(slug)

Unfavorite an article

    Unfavorite an article. Auth is required

### Parameters

|Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **slug** | **String**| Slug of the article that you want to unfavorite | [default to null] |

### Return type

[**CreateArticle_201_response**](../Models/CreateArticle_201_response.md)

### Authorization

[Token](../README.md#Token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

