---
title: "AuthRoutes"
linkTitle: AuthRoutes
weight: 30
description: >
  The route component checks user sign-in state and redirect users to the sign-in page if they haven’t signed in.
---
## Overview

AuthRoutes is the component to check the current user sign-in state. If the user’s `authUser.checked` is `false`, it will show a loading screen with the `<Loader />` component. Once the user’s sign-in state is checked, which means `authUser.checked` is `true`, it will either redirect the user to the sign-in page when the user hasn’t signed in or show the nested React routes.

## Props

| Prop Name | Description |
| --- | --- |
| signInPath | The pathname of the sign-in page |
| loader | This is the loader component to be displayed when the application is loading user sign-in state data |

## Source Code

[https://github.com/fireactjs/core/blob/main/src/lib/components/Auth.js](https://github.com/fireactjs/core/blob/main/src/lib/components/Auth.js)