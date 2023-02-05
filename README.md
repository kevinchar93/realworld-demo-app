# ![RealWorld Example App Backend](logo.png)

> A **backend** implementation of the "realworld" app **[YOUR_FRAMEWORK]** codebase containing real world examples (CRUD, auth, advanced patterns, etc) that adheres to the [RealWorld](https://github.com/gothinkster/realworld) spec and API.

[Demo](https://demo.realworld.io/)&nbsp;&nbsp;&nbsp;&nbsp;[RealWorld](https://github.com/gothinkster/realworld)

This codebase was created to demonstrate a fully fledged fullstack application built with **[YOUR_FRAMEWORK]** including CRUD operations, authentication, routing, pagination, and more.

We've gone to great lengths to adhere to the **[YOUR_FRAMEWORK]** community styleguides & best practices.

For more information on how to this works with other frontends/backends, head over to the [RealWorld](https://github.com/gothinkster/realworld) repo.

- [](#)
  - [How it works](#how-it-works)
  - [Getting started](#getting-started)
  - [What to do](#what-to-do)
    - [Expected functionality](#expected-functionality)
    - [Todo list](#todo-list)
      - [Creating a data model](#creating-a-data-model)
      - [Creating a data access layer](#creating-a-data-access-layer)

## How it works

This is a backend implementation only.

> Describe the general architecture of your app here

## Getting started

Install build system tool `just`, using [homebrew](https://brew.sh/) 

```
brew install just
```

Run `just docs` to view API documentation.

## What to do

A suggested todo list of what to implement & in what order - feel free to deviate.

Once the implementation is complete, remove this todo section & update the documentation above.

### Expected functionality

What the [backend should support](https://realworld-docs.netlify.app/docs/implementation-creation/features) at a high level:
* Authenticate users via JWT (login/signup pages + logout button on settings page)
* CRU- users (sign up & settings page - no deleting required)
* CRUD Articles
* CR-D Comments on articles (no updating required)
* GET and display paginated lists of articles
* Favourite articles
* Follow other users

Make sure to take a look at the api docs, run `just docs`.

### Todo list


- [ ] think about / plan the core architecture of the backend
  - *can skip this if using a framework where this is taken care of*
  

- [ ] implement error handling for the api:
  - [ ] model data for the error handling done by the API
  - [ ] 422 if a request fails any validations
  - [ ] 400 for a badly formed request
  - [ ] 401 for Unauthorized requests, when a request requires authentication but it isn't provided
  - [ ] 403 for Forbidden requests, when a request may be valid but the user doesn't have permissions to perform the action
  - [ ] 404 for Not found requests, when a resource can't be found to fulfil the request
  - see: https://realworld-docs.netlify.app/docs/specs/backend-specs/error-handling


- [ ] implement api for endpoint **"User and Authentication"**:
  - [ ] create a data model for the endpoint
    - think about:
      - how many entities / objects / "things" you need to model this endpoint
      - whats the shape of the data you are **sending to & receiving from the client**
      - what actions (methods) will need to be performed on this data 
      - what is the shape of the data you will need to **persist** for this endpoint
        - when you create a database table / collection what will its fields be
      - see the section [Creating a data model](#creating-a-data-model)
  - [ ] POST /users/login -> Existing user login
  - [ ] POST  /users ->  Create a user
  - [ ] GET   /user  -> Get current user
  - [ ] PUT   /user  -> Update current user

- [ ] implement api for endpoint **"Tags"**:
  - [ ] GET   /tags  -> Get tags


- [ ] implement api for endpoint **"Profile"**:
  - [ ] GET   /profiles/{username}  -> Get a profile
  - [ ] POST   /profiles/{username}/follow  -> Follow a user
  - [ ] DELETE   /profiles/{username}/follow  -> Unfollow a user

- [ ] implement api for endpoint **"Articles"**:
  - [ ] GET   /articles/feed  -> Get recent articles from users you follow
  - [ ] GET   /articles  -> Get recent articles globally
  - [ ] POST   /articles  -> Create an article
  - [ ] GET   /articles/{slug}  -> Get an article
  - [ ] PUT   /articles/{slug}  -> Update an article
  - [ ] DELETE   /articles/{slug}  -> Delete an article

- [ ] implement api for endpoint **"Favorites"**:
  - [ ] POST   /articles/{slug}/favorite  -> Favorite an article
  - [ ] DELETE   /articles/{slug}/favorite  -> Unfavorite an article

- [ ] implement api for endpoint **"Comments"**:
  - [ ] GET   /articles/{slug}/comments  -> Get comments for an article
  - [ ] POST   /articles/{slug}/comments  -> Create a comment for an article
  - [ ] DELETE   /articles/{slug}/comments/{id}  -> Delete a comment for an article

- [ ] implement data persistence
  - you'll want to persist the data written to each endpoint to read later
  - [ ] choose a database you'll use to store your data (Postgres or another relational DB is recommended)
  - [ ] use the models that you created when data modelling for the endpoints to determine what tables / collections you'll need
  - [ ] determine what fields / columns you'll have for each table / collection
  - [ ] create your database using your model
  - [ ] add database persistence to each endpoint 

#### Creating a data model
- take a look at the api documentation & absorb it
  - think about the shape of the data you'll need to send & receive from clients for each endpoint
  - you can look at the example request body / response documented with each endpoint (each example has a schema too)
  - you can also use the the data models / schema at the bottom of the api docs page
    - this should help guide your data modelling

#### Creating a data access layer