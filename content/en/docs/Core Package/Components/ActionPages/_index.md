---
title: "ActionPages"
linkTitle: ActionPages
weight: 5
description: >
  This is the component to power customised Firebase action pages.
---
## Overview

This component powers the action pages including reset password, verify email and restore email, which are Firebase authentication templates. The default pathname of these pages is `/auth-action`. To customise your Firebase templates, go to your Firebase project authentication → Templates, then click on the Edit Template button, and then click on “Customize action URL”. Use `https://www.yourdomain.com/auth-action` as the custom action URL and replace `www.yourdomain.com` with your actual application domain.

## Source Code

[https://github.com/fireactjs/core/blob/main/src/lib/components/auth/ActionPages.js](https://github.com/fireactjs/core/blob/main/src/lib/components/auth/ActionPages.js)