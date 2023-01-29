---
title: "SubscriptionContext"
linkTitle: SubscriptionContext
weight: 55
description: >
  The component to access the subscription account data.
---
## Overview

This is the context component to access the subscription account data. See the following example code on how to access the subscription account data.

```jsx
const { subscription } = useContext(SubscriptionContext);
const accountName = subscription.name?subscription.name:"";
```

## Source Code

[https://github.com/fireactjs/saas/blob/main/dist/components/SubscriptionContext.js](https://github.com/fireactjs/saas/blob/main/dist/components/SubscriptionContext.js)