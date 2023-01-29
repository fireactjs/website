---
title: "SubscriptionProvider"
linkTitle: SubscriptionProvider
weight: 65
description: >
  The component loads the subscription data as a context.
---
## Overview

This component is the context provider to load the subscription account data. The subscription account data is accessible to all the nested <Route> elements so that the subscription data is only loaded once.

```jsx
<Route path={pathnames.Subscription} element={<SubscriptionProvider loader={<Loader size="large" />} />} >
	...
</Route>
```

## Props

| Prop Name | Description |
| --- | --- |
| loader | This is the loader component to be displayed when the application is loading the subscription account data |

## Source Code

[https://github.com/fireactjs/saas/blob/main/dist/components/SubscriptionContext.js](https://github.com/fireactjs/saas/blob/main/dist/components/SubscriptionContext.js)