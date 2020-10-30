---
title: Multi-App Kiosk
author: rsameser
ms.author: riameser
ms.date: 10/30/2020
ms.topic: article
ms.prod: windows-iot
ms.technology: iot
description: Learn about the Multi-App Kiosk in Windows 10 IoT Enterprise.
keywords: Lockdown, Multi-App, Kiosk
---

# Multi-App Kiosk
A multi-app kiosk runs one or more apps from the desktop. People using the kiosk see a customized Start that shows only the tiles for the apps that are allowed. With this approach, you can configure a locked-down experience for different account types. A multi-app kiosk is appropriate for devices that are shared by multiple people. Here's a [guide](https://docs.microsoft.com/windows/configuration/lock-down-windows-10-to-specific-apps) on how to set up a multi-app kiosk.

## Kiosk Mode  
Kiosk configurations are based on [Assigned Access](https://docs.microsoft.com/windows/iot-enterprise/advanced_lockdown_features#assignedaccess), a feature in Windows 10 that allows an administrator to manage the user's experience by limiting the application entry points exposed to the user. Windows 10 IoT Enterprise offers two different types of locked-down experiences for public or specialized use.

Note, customers can use Microsoft 1st party app like Microsoft Edge or their own Line of Business app as the kiosk app. [Microsoft Edge kiosk mode](https://docs.microsoft.com/DeployEdge/microsoft-edge-configure-kiosk-mode) provides a tailored browsing experience that can be used together with assigned access.  
