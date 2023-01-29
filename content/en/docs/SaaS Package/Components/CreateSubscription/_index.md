---
title: "CreateSubscription"
linkTitle: CreateSubscription
weight: 20
description: >
  The component to choose a subscription plan and create a subscription account.
---
## Overview

This component shows the subscription plans with the `PricingPlans` component. If the chosen plan is a paid plan, it loads the `PaymentMethodForm` component to set up the payment method for the subscription account. Once the subscription account is created, it redirects the user to the subscription settings page.

## Screenshot

![Screenshot](screenshot1.png)

![Screenshot](screenshot2.png)

## Source Code

[https://github.com/fireactjs/saas/blob/main/dist/components/CreateSubscription.js](https://github.com/fireactjs/saas/blob/main/dist/components/CreateSubscription.js)