---
title: "Development"
linkTitle: Development
weight: 60
description: >
  Develop your components to add features to your Fireactjs application.
---
To add features to your application based on Fireactjs, you will need to develop your Reactjs components and attach them to the application routes.

## Replacing an existing route feature

When you setup your application based on Fireactjs, the homepage of the application is blank. That is because the `element` of the homepage `/` route is simply a React fragment as in the example code below.

```jsx
<Route exact path="/" element={<></>} />
```

If you replace the React fragment with your own component, you can control the functionality of the homepage.

## Adding new routes

The features of your web application may need more than the homepage route. You can add more routes similar to the homepage route to extend the application.

It is important that you add your new routes to the `pathnames.json` file instead of hard coding them in the `App.js` so that your users can navigate between the components without broken links when some routes are updated.

If you need to add the new routes to the main menu or the user menu, please read the components’ documents.

## Using `authUser` context variable

In your components, you can use the `authUser` context variable to retrieve user data and store user data. The current user’s information is under `authUser.user` JSON. Here is a list of the key properties of the current user.

- Name - `authUser.user.displayName`
- Email - `authUser.user.email`
- User ID - `authUser.user.uid`
- Email verified - `authUser.user.emailVerified`
- Avatar - `authUser.user.photoURL`

Below is an example to display the user info in a component called MyComponent

```jsx
import React from "react";
import { AuthContext } from "@fireactjs/core";

export const MyComponent = () => {

    return (
        <AuthContext.Consumer>
            {context => (
                <div>
                    <p>User ID: {context.authUser.user.uid}</p>
                    <p>Name: {context.authUser.user.displayName}</p>
                    <p>Email: {context.authUser.user.email}</p>
                    <p>Verified: {context.authUser.user.emailVerified?"Yes":"No"}</p>
                    <p>Avatar URL: {context.authUser.user.photoURL}</p>
                </div>
            )}
        </AuthContext.Consumer>
    )
}
```

Replace the React fragment of the homepage route as in the example below, and you will be able to show the current user info on the homepage.

```jsx
<Route exact path="/" element={<MyComponent />} />
```

## Storing data to the `authUser` context variable

In your application, you can store data for the current user in the `authUser` context variable. The `[authUser.data](http://authUser.data)` is designed for the purpose.

```jsx
const {setAuthUser} = useContext(AuthContext);
setAuthUser(prevState => ({
    ...prevState,
    data: {
        prop1: 'test'
    }
}));
```