# Real World App Backend Implementation 

An implementation of https://github.com/gothinkster/realworld in go lang as a way to learn the go programming language.

Expected functionality
=======================
Authenticate users via JWT (login/signup pages + logout button on settings page)
CRU- users (sign up & settings page - no deleting required)
CRUD Articles
CR-D Comments on articles (no updating required)
GET and display paginated lists of articles
Favorite articles
Follow other users

https://realworld-docs.netlify.app/docs/implementation-creation/features

[See the API docs](docs/api/README.md)

- [ ] implement error handling for the api:
  - [ ] model
    - run `just docs` to see the API documentation, information about the models is at the bottom of the page
  - [ ] 422 if a request fails any validations
  - [ ] 400 for a badly formed request
  - [ ] 401 for Unauthorized requests, when a request requires authentication but it isn't provided
  - [ ] 403 for Forbidden requests, when a request may be valid but the user doesn't have permissions to perform the action
  - [ ] 404 for Not found requests, when a resource can't be found to fulfil the request
errors should be in format:
```
{
  "errors":{
    "body": [
      "can't be empty"
    ]
  }
}
```
https://realworld-docs.netlify.app/docs/specs/backend-specs/error-handling



- [ ] implement api for [endpoint "User and Authentication"](docs/api/Apis/UserAndAuthenticationApi.md):
  - [ ] model data for /user endpoint, use model api docs to help:
    - run `just docs` to see the API documentation, information about the models is at the bottom of the page
  - [ ] POST /users/login -> Existing user login
  - [ ] POST  /users ->  Create a user
  - [ ] GET   /user  -> Get current user
  - [ ] PUT   /user  -> Update current user

- [ ] implement api for [endpoint "Tags"](docs/api/Apis/TagsApi.md):
  - [ ] model data for /tags endpoint
    - run `just docs` to see the API documentation, information about the models is at the bottom of the page
  - [ ] GET   /tags  -> Get tags


- [ ] implement api for [endpoint "Profile"](docs/api/Apis/ProfileApi.md):
  - [ ] model data for /profiles endpoint, use model api docs to help:
    - run `just docs` to see the API documentation, information about the models is at the bottom of the page
  - [ ] GET   /profiles/{username}  -> Get a profile
  - [ ] POST   /profiles/{username}/follow  -> Follow a user
  - [ ] DELETE   /profiles/{username}/follow  -> Unfollow a user

- [ ] implement api for [endpoint "Articles"](docs/api/Apis/ArticlesApi.md):
  - [ ] model data for /articles endpoint, use model api docs to help:
    - run `just docs` to see the API documentation, information about the models is at the bottom of the page
  - [ ] GET   /articles/feed  -> Get recent articles from users you follow
  - [ ] GET   /articles  -> Get recent articles globally
  - [ ] POST   /articles  -> Create an article
  - [ ] GET   /articles/{slug}  -> Get an article
  - [ ] PUT   /articles/{slug}  -> Update an article
  - [ ] DELETE   /articles/{slug}  -> Delete an article

- [ ] implement api for [endpoint "Favorites"](docs/api/Apis/FavoritesApi.md):
  - [ ] model data for /favourite endpoint
    - run `just docs` to see the API documentation, information about the models is at the bottom of the page
  - [ ] POST   /articles/{slug}/favorite  -> Favorite an article
  - [ ] DELETE   /articles/{slug}/favorite  -> Unfavorite an article

- [ ] implement api for [endpoint "Comments"](docs/api/Apis/CommentsApi.md):
  - [ ] model data for /comments endpoint, use model api docs to help:
    - run `just docs` to see the API documentation, information about the models is at the bottom of the page
  - [ ] GET   /articles/{slug}/comments  -> Get comments for an article
  - [ ] POST   /articles/{slug}/comments  -> Create a comment for an article
  - [ ] DELETE   /articles/{slug}/comments/{id}  -> Delete a comment for an article
