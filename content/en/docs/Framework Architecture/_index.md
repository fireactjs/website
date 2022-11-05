---
title: "Framework Architecture"
linkTitle: Framework Architecture
weight: 100
description: >
  Fireactjs is designed to be extensible and customizable with its framework architecture.
---
## Overview

Fireactjs is a component-based framework. That means all the out-of-the-box features are delivered as components, and you can add components to extend or swap components to customize the web application that you are building based on the framework.

You can find all the key components that are shipped with the framework in the example `src/App.js` file in the demo repo here:

```jsx
function App() {

	return (
		<AuthProvider firebaseConfig={firebaseConfig} brand={Brand}>
			<BrowserRouter>
				<Routes>
					<Route element={<AuthRoutes signInPath={pathnames.SignIn} loader={<Loader size="large" />} />} >
						<Route element={<AppTemplate logo={<Logo size="large" />} brand={Brand} toolBarMenu={<UserMenu pathnames={pathnames} />} drawerMenu={<MainMenu pathnames={pathnames}  />} />}>
							<Route exact path="/" element={<></>} />
							<Route exact path={pathnames.UserProfile} element={<UserProfile pathnames={pathnames} />} />
							<Route exact path={pathnames.UserUpdateEmail} element={<UserUpdateEmail pathnames={pathnames} />} />
							<Route exact path={pathnames.UserUpdateName} element={<UserUpdateName pathnames={pathnames} />} />
							<Route exact path={pathnames.UserUpdatePassword} element={<UserUpdatePassword pathnames={pathnames} />} />
							<Route exact path={pathnames.UserDelete} element={<UserDelete pathnames={pathnames} />} />
						</Route>
					</Route>
					<Route element={<PublicTemplate />}>
						<Route path={pathnames.SignIn} element={
							<SignIn
								logo={<Logo size="large" />}
								pathnames={pathnames}
								providers={authMethods}
							/>
						} />
						<Route path={pathnames.SignUp} element={
							<SignUp
								logo={<Logo size="large" />}
								pathnames={pathnames}
							/>
						} />
						<Route path={pathnames.ResetPassword} element={
							<ResetPassword
								logo={<Logo size="large" />}
								pathnames={pathnames}
							/>
						} />
					</Route>
				</Routes>
			</BrowserRouter>
		</AuthProvider>
	)
}
```

## Authentication Components

At the top level, the `<AuthProvider />` component manages the authentication state with a context variable called `authUser`. This variable tells the system if the current user has signed in or not as well as the relevant data about the user.

## Routes

Within the `<AuthProvider />` component are routes for your application. It is important to have a good understanding of [React Router](https://reactrouter.com/en/main/start/tutorial). There are two kinds of routes you will find: the layout routes without the `path` prop and the page routes with the `path` prop. 

All the pages that only authenticated users can access should be placed under the route of the `<AuthRoutes />` component. And within the component, you can have template routes to control the look and feel of your application. The `<AppTemplate />` component is an example.

Outside of the `<AuthRoutes />` component are the pages that the users can access without authentication, such as the sign-in page, the sign-up page, etc. They can have their own templates similar to the authenticated pages. The `<PublicTemplate />` component is an example.

## Page components

Each route mapping to a page requires a visual component for its `element` prop. For example, the `<UserProfle />` component shows the user profile details. You can add new routes for new pages and features of your application, or swap the existing routes with your custom-built components to change their functionality.

## Pathnames

Within the page components, there are links between the pages to build a smooth user flow experience. It’s important that the page components know how to link with each other, and that is the purpose of the `pathnames.json` file. This file defines all the page components and their URL path names as a JSON file.

Here is an example of the default `pathnames.json` file from the framework.

```json
{
    "ResetPassword": "/reset-password",
    "SignIn": "/sign-in",
    "SignUp": "/sign-up",
    "UserDelete": "/user/delete",
    "UserProfile": "/user",
    "UserUpdateEmail": "/user/update-email",
    "UserUpdateName": "/user/update-name",
    "UserUpdatePassword": "/user/update-password"
}
```