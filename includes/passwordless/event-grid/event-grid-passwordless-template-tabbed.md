---
title: "include file"
description: "include file"
services: eventgrid
author: sonalika-roy
ms.service: eventgrid
ms.topic: include
ms.date: 05/30/2023
ms.author: sonalikaroy
ms.custom: include file
---

## Authenticate the app to Azure

This quick start shows you two ways of connecting to Azure Service Bus: **passwordless** and **connection string**. 

The first option shows you how to use your security principal in Azure Active Directory and role-based access control (RBAC) to connect to a Event Grid Namespace. You don't need to worry about having hard-coded connection string in your code or in a configuration file or in a secure storage like Azure Key Vault. 

The second option shows you how to use a connection string to connect to a Event Grid namespace. If you are new to Azure, you may find the connection string option easier to follow. We recommend using the passwordless option in real-world applications and production environments. For more information, see [Authentication and authorization](../../../articles/event-grid/authenticate-with-active-directory.md). You can also read more about passwordless authentication on the [overview page](/dotnet/azure/sdk/authentication?tabs=command-line).

## [Passwordless (Recommended)](#tab/passwordless)

### Assign roles to your Azure AD user

[!INCLUDE [event-grid-assign-roles](security-authorization.md)]

## [Connection String](#tab/connection-string)
Creating a new event grid namespace automatically generates an initial Shared Access Signature (SAS) policy with primary and secondary keys, and primary and secondary connection strings that each grant full control over all aspects of the namespace. 

A client can use the connection string to connect to the Service Bus namespace. To copy the primary connection string for your namespace, follow these steps: 

1. On the **Event Grid Namespace** page, select **Topics**.
2. Select the topic you need to access.
3. On the **Access keys** page, select the copy button next to **Key 1 or Key 2**, to copy the access keys to your clipboard for later use. Paste this value into Notepad or some other temporary location.


