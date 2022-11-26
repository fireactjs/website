---
title: "UserMenu"
linkTitle: UserMenu
weight: 110
description: >
  The menu component displays the user action menu at the top-right of the toolbar.
---
## Overview

UserMenu is the menu at the top-right of the toolbar for the current user to manage their profile and sign out. It can be customized by inserting additional menu items as `customItems` prop. You can also replace it with your own menu component.

## Screenshot

![Screenshot](screenshot.png)

## Props

| Prop Name | Description |
| --- | --- |
| customItems | An array of menu item elements to be inserted between Profile and Sign Out options. |

## Source Code

[https://github.com/fireactjs/core/blob/main/src/lib/components/menus/UserMenu.js](https://github.com/fireactjs/core/blob/main/src/lib/components/menus/UserMenu.js)