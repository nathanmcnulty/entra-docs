---
title: Increase the resilience of authentication and authorization applications you develop
description: Resilience guidance for application development using Microsoft Entra ID and the Microsoft identity platform
ms.service: entra
ms.subservice: architecture
ms.topic: how-to
author: jricketts
ms.author: jricketts
manager: martinco
ms.date: 03/02/2023
---

# Increase the resilience of authentication and authorization applications you develop

The [Microsoft identity platform](~/identity-platform/v2-overview.md) helps you build applications your users and customers can sign in to using their Microsoft identities or social accounts. The Microsoft identity platform uses token-based authentication and authorization flows to communicate with applications. Client applications acquire tokens from an identity provider (IdP), Microsoft Entra and Azure AD B2C, to authenticate users and authorize applications to call protected APIs. A service validates tokens. For more information, see [Security tokens](~/identity-platform/security-tokens.md).

A token is valid for a length of time, and then the app must acquire a new one. Rarely, a call to retrieve a token fails due to network or infrastructure issues or an authentication service outage. The [backup authentication system](backup-authentication-system.md) increases authentication resilience if there's an outage. This system transparently and automatically handles authentications for supported applications and services if the primary Microsoft Entra service is unavailable or degraded.

The following articles have guidance for client and service applications for a signed in user and daemon applications. They contain best practices for using tokens and calling resources.

- [Increase the resilience of authentication and authorization in client applications you develop](resilience-client-app.md)
- [Increase the resilience of authentication and authorization in daemon applications you develop](resilience-daemon-app.md)
- [Build resilience in your identity and access management infrastructure](resilience-in-infrastructure.md)
- [Build resilience in your customer identity and access management with Azure AD B2C](resilience-b2c.md)
- [Building application support for the backup authentication system](backup-authentication-system-apps.md)
- [Build services that are resilient to Microsoft Entra ID OpenID Connect metadata refresh](~/identity-platform/howto-build-services-resilient-to-metadata-refresh.md)
