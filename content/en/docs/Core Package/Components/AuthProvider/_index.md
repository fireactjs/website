---
title: "AuthProvider"
linkTitle: AuthProvider
weight: 20
description: >
  This component checks the user’s logged-in state and passes the data to the children components via context variables.
---
## Overview

AuthProvider is an invisible component to wrap the whole application and detects if the current user has signed in. It stores the user state in a context variable and passes it to the children elements.

## Props

| Prop Name | Description |
| --- | --- |
| firebaseConfig | This is the Firebase config JSON object. |
| brand | This is a brand name string to be displayed next to the logo |

## Context Variables

The context variables AuthProvider offers to the children components.

| Prop Name | Description |
| --- | --- |
| authUser | The JSON object contains the user data. authUser.user contains the current user data if the user has signed in or null for users who haven’t signed in. authUser.data is a JSON for custom data object you need to store for the current user. authUser.checked indicates if the status of the current user has been checked. |
| setAuthUser | This sets the authUser context variable. |
| fireabaseApp | This is the Firebase app variable that can be reused in the children components |
| brand | This is the brand name string |

## Source Code

[https://github.com/fireactjs/core/blob/main/src/lib/components/Auth.js](https://github.com/fireactjs/core/blob/main/src/lib/components/Auth.js)