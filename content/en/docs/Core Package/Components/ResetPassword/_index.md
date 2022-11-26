---
title: "ResetPassword"
linkTitle: ResetPassword
weight: 70
description: >
  The form for users to request a password reset.
---
## Overview

ResetPassword is a form component for users to input their emails to request a password reset. The form will trigger the reset password process in Firebase Authentication. There is a rate limit enforced by Firebase so that it won’t be used to spam users.

## Screenshot

![Screenshot](screenshot.png)

## Props

| Prop Name | Description |
| --- | --- |
| logo | This is the logo component to be displayed at the top of the form |

## Source Code

[https://github.com/fireactjs/core/blob/main/src/lib/components/auth/ResetPassword.js](https://github.com/fireactjs/core/blob/main/src/lib/components/auth/ResetPassword.js)