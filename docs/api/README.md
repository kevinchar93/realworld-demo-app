# Documentation for Conduit API

<a name="documentation-for-api-endpoints"></a>
## Documentation for API Endpoints

All URIs are relative to */api*

| Class | Method | HTTP request | Description |
|------------ | ------------- | ------------- | -------------|
| *ArticlesApi* | [**createArticle**](Apis/ArticlesApi.md#createarticle) | **POST** /articles | Create an article |
*ArticlesApi* | [**deleteArticle**](Apis/ArticlesApi.md#deletearticle) | **DELETE** /articles/{slug} | Delete an article |
*ArticlesApi* | [**getArticle**](Apis/ArticlesApi.md#getarticle) | **GET** /articles/{slug} | Get an article |
*ArticlesApi* | [**getArticles**](Apis/ArticlesApi.md#getarticles) | **GET** /articles | Get recent articles globally |
*ArticlesApi* | [**getArticlesFeed**](Apis/ArticlesApi.md#getarticlesfeed) | **GET** /articles/feed | Get recent articles from users you follow |
*ArticlesApi* | [**updateArticle**](Apis/ArticlesApi.md#updatearticle) | **PUT** /articles/{slug} | Update an article |
| *CommentsApi* | [**createArticleComment**](Apis/CommentsApi.md#createarticlecomment) | **POST** /articles/{slug}/comments | Create a comment for an article |
*CommentsApi* | [**deleteArticleComment**](Apis/CommentsApi.md#deletearticlecomment) | **DELETE** /articles/{slug}/comments/{id} | Delete a comment for an article |
*CommentsApi* | [**getArticleComments**](Apis/CommentsApi.md#getarticlecomments) | **GET** /articles/{slug}/comments | Get comments for an article |
| *FavoritesApi* | [**createArticleFavorite**](Apis/FavoritesApi.md#createarticlefavorite) | **POST** /articles/{slug}/favorite | Favorite an article |
*FavoritesApi* | [**deleteArticleFavorite**](Apis/FavoritesApi.md#deletearticlefavorite) | **DELETE** /articles/{slug}/favorite | Unfavorite an article |
| *ProfileApi* | [**followUserByUsername**](Apis/ProfileApi.md#followuserbyusername) | **POST** /profiles/{username}/follow | Follow a user |
*ProfileApi* | [**getProfileByUsername**](Apis/ProfileApi.md#getprofilebyusername) | **GET** /profiles/{username} | Get a profile |
*ProfileApi* | [**unfollowUserByUsername**](Apis/ProfileApi.md#unfollowuserbyusername) | **DELETE** /profiles/{username}/follow | Unfollow a user |
| *TagsApi* | [**getTags**](Apis/TagsApi.md#gettags) | **GET** /tags | Get tags |
| *UserAndAuthenticationApi* | [**createUser**](Apis/UserAndAuthenticationApi.md#createuser) | **POST** /users | Register a new user |
*UserAndAuthenticationApi* | [**getCurrentUser**](Apis/UserAndAuthenticationApi.md#getcurrentuser) | **GET** /user | Get current user |
*UserAndAuthenticationApi* | [**login**](Apis/UserAndAuthenticationApi.md#login) | **POST** /users/login | Existing user login |
*UserAndAuthenticationApi* | [**updateCurrentUser**](Apis/UserAndAuthenticationApi.md#updatecurrentuser) | **PUT** /user | Update current user |


<a name="documentation-for-models"></a>
## Documentation for Models

 - [Article](./Models/Article.md)
 - [Comment](./Models/Comment.md)
 - [CreateArticleComment_200_response](./Models/CreateArticleComment_200_response.md)
 - [CreateArticleComment_request](./Models/CreateArticleComment_request.md)
 - [CreateArticle_201_response](./Models/CreateArticle_201_response.md)
 - [CreateArticle_request](./Models/CreateArticle_request.md)
 - [CreateUser_request](./Models/CreateUser_request.md)
 - [GenericErrorModel](./Models/GenericErrorModel.md)
 - [GenericErrorModel_errors](./Models/GenericErrorModel_errors.md)
 - [GetArticleComments_200_response](./Models/GetArticleComments_200_response.md)
 - [GetArticlesFeed_200_response](./Models/GetArticlesFeed_200_response.md)
 - [GetProfileByUsername_200_response](./Models/GetProfileByUsername_200_response.md)
 - [GetTags_200_response](./Models/GetTags_200_response.md)
 - [LoginUser](./Models/LoginUser.md)
 - [Login_200_response](./Models/Login_200_response.md)
 - [Login_request](./Models/Login_request.md)
 - [NewArticle](./Models/NewArticle.md)
 - [NewComment](./Models/NewComment.md)
 - [NewUser](./Models/NewUser.md)
 - [Profile](./Models/Profile.md)
 - [UpdateArticle](./Models/UpdateArticle.md)
 - [UpdateArticle_request](./Models/UpdateArticle_request.md)
 - [UpdateCurrentUser_request](./Models/UpdateCurrentUser_request.md)
 - [UpdateUser](./Models/UpdateUser.md)
 - [User](./Models/User.md)


<a name="documentation-for-authorization"></a>
## Documentation for Authorization

<a name="Token"></a>
### Token

- **Type**: API key
- **API key parameter name**: Authorization
- **Location**: HTTP header

