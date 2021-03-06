### warsawjs-workshop-21-zeppelin

## Table of Contents

- [Setup](#setup)
  - [redux](#redux)
  - [hot reload](#hot-reload)
- [Login Layout](#login-layout)
- [Login action](#login-aciton)
- [Setup react-router](#reat-router)
- [Post list](#post-list)
- [Dynamic posts](#dynamic-posts)
- [Adding new post](#adding-new-post)
- [Navigation](#navigation)
- [Reselect](#reselect)
- [Ideas for improvements](#ideas-for-improvements)


## Setup
### Redux

`yarn add redux react-redux redux-thunk`
* Create `store.js`
* Create `user` reducer with initial state
* Use `Provider` in `App.js`

### Hot reload
* Setup hot reloading in `index.js` file

### Login layout
* Create `Input`, `CheckInput` and `InputGroup` components
* `yarn add redux-form`
* Create `Home` page with login form
* Add: `username`, `password` and `termsCheckbox` fields connected with `redux-form`
* `yarn add redux-form-validators`
* Combine redux-form reducer
* Add validators to the fields

### Login action
* Create `net.js` and `api.js` files for API connection
* Create redux action for login user
* Set username in user profile and local storage

### react-router
* `yarn add react-router-dom react-router-redux@next history` [Docs](https://github.com/reacttraining/react-router/tree/master/packages/react-router-redux)
* Combine router reducer
* Apply `routerMiddleware`
* Wrap whole application in `ConnectedRouter` wrapper
* Specify '/' route with redirect for logged in user

### Post list
* Create `PostCard` component
* Create `/posts` route with list of cards
* Create `/post` route with single card

### Dynamic posts
* Remake `/posts` route as route with child routes
* Create posts actions, reducer and api function
* Fetch data form API
* Display dynamic data for list and single post routes
* Link each element on the list page

### Adding new post
* Create `/posts/new` route with redux-form
* `yarn add react-dropzone`
* Create `FileField` component based on `react-dropzone`
* Restore session on enter `/posts` route
* Create redux action for submit new post, get username by `getState` function, use FormData for request, add `objectToFormData` helper function
* Add created post to the list of posts in redux state

### Navigation
* Add a navigation with link to `/posts` route
* Add `Create` link button on `/posts` route
* Add `back` link button on singe post view

### Reselect
`yarn add reselect`
* Create sample selector (all post owners, sorted posts asc/desc by date)
* Display filtered posts by specific owner
* Allow user to sort posts by date

### Ideas for improvements
* Get posts ever and again
* Add comment to the post at the specific point
* Setup [eslint](https://github.com/yannickcr/eslint-plugin-react) for react project
* Deploy to the [gh-pages](https://codeburst.io/deploy-react-to-github-pages-to-create-an-amazing-website-42d8b09cd4d)
* [Input masking](https://github.com/renato-bohler/redux-form-input-masks) with redux form
* [redux-logger](https://github.com/evgenyrodionov/redux-logger)
