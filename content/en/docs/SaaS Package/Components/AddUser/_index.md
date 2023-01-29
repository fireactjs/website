---
title: "AddUser"
linkTitle: AddUser
weight: 5
description: >
  The component to invite users to a subscription account.
---
## Overview

Each subscription account can have multiple users. This is the component to invite new and existing users of the system to access the subscription account with the assigned permission roles.

## Screenshot

![Screenshot](screenshot.png)

## Props

| Prop Name | Description |
| --- | --- |
| setAddUserActive | The state of AddUser component is loaded in the parent component. Set false to unload the component. |
| setUsers | The state of the user list in the parent component. After a user is invited, the user will be appended to the users state. |

## Source Code

[https://github.com/fireactjs/saas/blob/main/src/lib/components/AddUser.js](https://github.com/fireactjs/saas/blob/main/src/lib/components/AddUser.js)