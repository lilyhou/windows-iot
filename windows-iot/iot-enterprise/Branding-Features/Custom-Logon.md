---
title: Custom Logon
author: rsameser
ms.author: riameser
ms.date: 10/30/2020
ms.topic: article
ms.prod: windows-iot
ms.technology: iot
description: Learn about the Custom Logon Feature in Windows 10 IoT Enterprise.
keywords: Branding, Custom Logon
---

# Custom Logon
Custom Logon features allow you to take control of the welcome and shutdown screens for your device. For example, you can suppress all elements of the Welcome screen UI and provide a custom logon UI. You can also suppress the Blocked Shutdown Resolver (BSDR) screen and automatically end applications while the OS waits for applications to close before a shutdown.

Custom Logon settings do not modify the credential behavior of Winlogon, so you can use any credential provider that is compatible with Windows 10 to provide a custom sign-in experience for your device.

Note, Custom Logon is an optional component and is not turned on by default in Windows 10. It must be [turned on](https://docs.microsoft.com/windows-hardware/customize/enterprise/custom-logon#turn-on-custom-logon) prior to configuring.
