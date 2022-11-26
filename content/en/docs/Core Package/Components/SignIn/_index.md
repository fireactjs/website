---
title: "SignIn"
linkTitle: SignIn
weight: 80
description: >
  The form for users to sign in to the application.
---
## Overview

SignIn is a form component for users to sign in to the application via email and password or one of the enabled single sign-on methods. It shows the single sign-on buttons based on the provider JSON. Once the user signs in successfully, it will redirect the user to the `successUrl` or the URL pathname in the `re` parameter.

## Screenshot

![Screenshot](screenshot.png)

## Props

| Prop Name | Description |
| --- | --- |
| logo | This is the logo component to be displayed at the top of the form |
| successUrl | The URL to redirect users to after signing in, if no re parameter is provided in the URL |

## Source Code

[https://github.com/fireactjs/core/blob/main/src/lib/components/auth/SignIn.js](https://github.com/fireactjs/core/blob/main/src/lib/components/auth/SignIn.js)