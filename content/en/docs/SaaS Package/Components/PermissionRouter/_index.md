---
title: "PermissionRouter"
linkTitle: PermissionRouter
weight: 45
description: >
  The component to check user permission roles.
---
## Overview

This component checks whether the current user has permissions in the `permissions` prop. It is designed to be used with the `<Route />` component as the parent route of nested routes. For example, the code below will make the nested route only accessible for the `access` permission role.

```jsx
<Route element={<PermissionRouter permissions={["access"]} />} >
	<Route exact path={pathnames.Subscription+"/"} element={<div>Home</div>} />
</Route>
```

## Props

| Prop Name | Description |
| --- | --- |
| permissions | This is an array of the permission roles that are allowed for the route. |

## Source Code

[https://github.com/fireactjs/saas/blob/main/dist/components/PermissionRouter.js](https://github.com/fireactjs/saas/blob/main/dist/components/PermissionRouter.js)