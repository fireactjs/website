---
title: "AppTemplate"
linkTitle: AppTemplate
weight: 10
description: >
  This is the template component for the logged-in state application.
---
## Overview

AppTemplate is a template component that controls the layout of the logged-in state of your application. It has a few props for customizing the interface such as your logo and brand name, menu etc. Below is a screenshot of the component and the positions of the props.

## Screenshot

![Screenshot](screenshot.png)

## Props

| Prop Name | Description |
| --- | --- |
| logo | This is the logo component to be displayed in the top-left of the layout |
| brand | This is a brand name string to be displayed next to the logo |
| drawerMenu | This is the main menu in the left sidebar. See <MainMenu /> component for example. |
| toolbarChildren | These are the child components in the left part of the toolbar |
| toolBarMenu | This is the toolbar menu component in the right part of the toolbar. See <UserMenu /> component for example. |

## Source Code

[https://github.com/fireactjs/core/blob/main/src/lib/components/templates/AppTemplate.js](https://github.com/fireactjs/core/blob/main/src/lib/components/templates/AppTemplate.js)