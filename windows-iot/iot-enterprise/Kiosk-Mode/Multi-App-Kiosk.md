---
title: Multi-App Kiosk
author: rsameser
ms.author: riameser
ms.date: 11/09/2020
ms.topic: article
ms.prod: windows-iot
ms.technology: iot
description: Learn about the Multi-App Kiosk in Windows 10 IoT Enterprise.
keywords: Lockdown, Multi-App, Kiosk
---

# Multi-App Kiosk
A multi-app kiosk runs one or more apps from the desktop. People using the kiosk see a customized Start that shows only the tiles for the apps that are allowed. With this approach, you can configure a locked-down experience for different account types. A multi-app kiosk is appropriate for devices that are shared by multiple people. Here's a [guide](https://docs.microsoft.com/windows/configuration/lock-down-windows-10-to-specific-apps) on how to set up a multi-app kiosk.

## Benefits of Using a Multi-App Kiosk
The benefit of a kiosk that runs only one or more specified apps is to provide an easy-to-understand experience for individuals by putting in front of them only the things they need to use, and removing from their view the things they don’t need to access.

A multi-app kiosk is appropriate for devices that are shared by multiple people.

## Configuring your Multi-App Kiosk
* [Configure a kiosk in Microsoft Intune](https://docs.microsoft.com/windows/configuration/lock-down-windows-10-to-specific-apps#configure-a-kiosk-in-microsoft-intune)
* [Configure a Kiosk using a provisioning package](https://docs.microsoft.com/windows/configuration/lock-down-windows-10-to-specific-apps#configure-a-kiosk-using-a-provisioning-package)


> [!NOTE]
> When you configure a multi-app kiosk, [specific policies](https://docs.microsoft.com/windows/configuration/kiosk-policies) are enforced that will affect all non-administrator users on the device.
