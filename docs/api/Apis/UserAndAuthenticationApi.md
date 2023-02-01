# UserAndAuthenticationApi

All URIs are relative to */api*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createUser**](UserAndAuthenticationApi.md#createUser) | **POST** /users |  |
| [**getCurrentUser**](UserAndAuthenticationApi.md#getCurrentUser) | **GET** /user | Get current user |
| [**login**](UserAndAuthenticationApi.md#login) | **POST** /users/login | Existing user login |
| [**updateCurrentUser**](UserAndAuthenticationApi.md#updateCurrentUser) | **PUT** /user | Update current user |


<a name="createUser"></a>
# **createUser**
> Login_200_response createUser(body)



    Register a new user

### Parameters

|Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **body** | [**CreateUser_request**](../Models/CreateUser_request.md)| Details of the new user to register | |

### Return type

[**Login_200_response**](../Models/Login_200_response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

<a name="getCurrentUser"></a>
# **getCurrentUser**
> Login_200_response getCurrentUser()

Get current user

    Gets the currently logged-in user

### Parameters
This endpoint does not need any parameter.

### Return type

[**Login_200_response**](../Models/Login_200_response.md)

### Authorization

[Token](../README.md#Token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="login"></a>
# **login**
> Login_200_response login(body)

Existing user login

    Login for existing user

### Parameters

|Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **body** | [**Login_request**](../Models/Login_request.md)| Credentials to use | |

### Return type

[**Login_200_response**](../Models/Login_200_response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

<a name="updateCurrentUser"></a>
# **updateCurrentUser**
> Login_200_response updateCurrentUser(body)

Update current user

    Updated user information for current user

### Parameters

|Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **body** | [**UpdateCurrentUser_request**](../Models/UpdateCurrentUser_request.md)| User details to update. At least **one** field is required. | |

### Return type

[**Login_200_response**](../Models/Login_200_response.md)

### Authorization

[Token](../README.md#Token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

