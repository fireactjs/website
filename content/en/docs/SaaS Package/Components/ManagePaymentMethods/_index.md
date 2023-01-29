---
title: "ManagePaymentMethods"
linkTitle: ManagePaymentMethods
weight: 40
description: >
  The component lists the subscription accounts the current user has access.
---
## Overview

This is the component to list the existing payment methods of the user. Click “Set Default” to attach the payment method to the current subscription account. Click “Remove” to remove the payment method from the user. If the payment method is attached to a subscription account, removal will return an error.

Add payment method feature will load the `PaymentMethodForm` component to add a new payment method and attach it to the current subscription account.

## Screenshot

![Screenshot](screenshot.png)

## Props

| Prop Name | Description |
| --- | --- |
| loader | This is the loader component to be displayed when the application is loading the payment methods data |

## Source Code

[https://github.com/fireactjs/saas/blob/main/dist/components/ManagePaymentMethods.js](https://github.com/fireactjs/saas/blob/main/dist/components/ManagePaymentMethods.js)