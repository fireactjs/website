---
title: "UpdateUser"
linkTitle: UpdateUser
weight: 70
description: >
  The component to update the permissions of a user.
---
## Overview

This component displays a form to allow the admins of the subscription account to update the permissions of a user, or revoke access of the user.

## Props

| Prop Name | Description |
| --- | --- |
| user | The user object to be updated |
| setSelectedUser | The state of UpdateUser component is loaded in the parent component. Set false to unload the component. |
| setUsers | The state of the user list in the parent component. After a user is invited, the user will be appended to the users state. |

## Source Code

[https://github.com/fireactjs/saas/blob/main/dist/components/UpdateUser.js](https://github.com/fireactjs/saas/blob/main/dist/components/UpdateUser.js)