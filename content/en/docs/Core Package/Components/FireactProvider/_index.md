---
title: "FireactProvider"
linkTitle: FireactProvider
weight: 35
description: >
  This component provides the framework configurations via a context variable config.
---
## Overview

FireactProvider is an invisible component to wrap the whole application to provide the framework configurations via a context variable `config`. You can extend the `config` JSON object by attaching new properties to it.

At a minimum, the framework expects the `config` JSON contains the following properties:

- `firebaseConfig` - the configurations of your Firebase project
- `brand` - the brand name of your project
- `pathnames` - the components and their path names as described above
- `authProviders` - the configurations of the authentication providers

## Context Variables

The context variables AuthProvider offers to the children components.

| Prop Name | Description |
| --- | --- |
| config | The framework configurations including firebaseConfig, brand, pathnames and authProviders. |

## Source Code

[https://github.com/fireactjs/core/blob/main/src/lib/components/Fireact.js](https://github.com/fireactjs/core/blob/main/src/lib/components/Fireact.js)