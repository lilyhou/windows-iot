---
title: Single-App Kiosk
author: rsameser
ms.author: riameser
ms.date: 10/30/2020
ms.topic: article
ms.prod: windows-iot
ms.technology: iot
description: Learn about the Single-App Kiosk in Windows 10 IoT Enterprise.
keywords: Lockdown, Single-App, Kiosk
---

# Single-App Kiosk
A single-app kiosk runs a single Universal Windows Platform (UWP) app in full-screen above the lock screen. People using the kiosk can see only that app. A single-app kiosk is ideal for public use. Here's a [guide](https://docs.microsoft.com/windows/configuration/kiosk-single-app) on how to set up a single-app kiosk.

## Kiosk Mode  
Kiosk configurations are based on [Assigned Access](https://docs.microsoft.com/windows/iot-enterprise/advanced_lockdown_features#assignedaccess), a feature in Windows 10 that allows an administrator to manage the user's experience by limiting the application entry points exposed to the user. Windows 10 IoT Enterprise offers two different types of locked-down experiences for public or specialized use.

Note, customers can use Microsoft 1st party app like Microsoft Edge or their own Line of Business app as the kiosk app. [Microsoft Edge kiosk mode](https://docs.microsoft.com/DeployEdge/microsoft-edge-configure-kiosk-mode) provides a tailored browsing experience that can be used together with assigned access.  
