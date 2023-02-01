# ProfileApi

All URIs are relative to */api*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**followUserByUsername**](ProfileApi.md#followUserByUsername) | **POST** /profiles/{username}/follow | Follow a user |
| [**getProfileByUsername**](ProfileApi.md#getProfileByUsername) | **GET** /profiles/{username} | Get a profile |
| [**unfollowUserByUsername**](ProfileApi.md#unfollowUserByUsername) | **DELETE** /profiles/{username}/follow | Unfollow a user |


<a name="followUserByUsername"></a>
# **followUserByUsername**
> GetProfileByUsername_200_response followUserByUsername(username)

Follow a user

    Follow a user by username

### Parameters

|Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **username** | **String**| Username of the profile you want to follow | [default to null] |

### Return type

[**GetProfileByUsername_200_response**](../Models/GetProfileByUsername_200_response.md)

### Authorization

[Token](../README.md#Token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="getProfileByUsername"></a>
# **getProfileByUsername**
> GetProfileByUsername_200_response getProfileByUsername(username)

Get a profile

    Get a profile of a user of the system. Auth is optional

### Parameters

|Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **username** | **String**| Username of the profile to get | [default to null] |

### Return type

[**GetProfileByUsername_200_response**](../Models/GetProfileByUsername_200_response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="unfollowUserByUsername"></a>
# **unfollowUserByUsername**
> GetProfileByUsername_200_response unfollowUserByUsername(username)

Unfollow a user

    Unfollow a user by username

### Parameters

|Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **username** | **String**| Username of the profile you want to unfollow | [default to null] |

### Return type

[**GetProfileByUsername_200_response**](../Models/GetProfileByUsername_200_response.md)

### Authorization

[Token](../README.md#Token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

