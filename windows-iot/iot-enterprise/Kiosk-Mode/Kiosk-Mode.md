---
title: Kiosk Mode
author: rsameser
ms.author: riameser
ms.date: 12/11/2020
ms.topic: article
ms.prod: windows-iot
ms.technology: iot
description: Learn about Kiosk Mode in Windows 10 IoT Enterprise.
keywords: Lockdown, Kiosks, Kiosk Mode
---

# Kiosk Mode  
Windows 10 IoT Enterprise allows you to build fixed purpose devices such as ATM machines, point-of-sale terminals, medical devices, digital signs or kiosks. Kiosk mode helps you create a dedicated and locked down user experience on these fixed purpose devices. Windows 10 offers two different locked-down experiences for public or specialized use: single-app kiosks or multi-app kiosks.

Kiosk configurations are based upon either [assigned access](https://docs.microsoft.com/windows/configuration/guidelines-for-assigned-access-app) or [shell launcher](../Advanced-Lockdown-Features/Shell-Launcher.md). There are several kiosk configuration methods that you can choose from, depending on your answers to the following questions.

## Which type of app will your kiosk run?
Your kiosk can run a Universal Windows Platform (UWP) app or a Windows desktop application. For [digital signage](https://docs.microsoft.com/windows/configuration/setup-digital-signage), simply select a digital sign player as your kiosk app. Check out the [guidelines for kiosk apps](https://docs.microsoft.com/windows/configuration/guidelines-for-assigned-access-app).

## Which type of kiosk do you need?
If you want your kiosk to run a single app for anyone to see or use, consider a single-app kiosk that runs either a [Universal Windows Platform (UWP) app](https://docs.microsoft.com/windows/configuration/kiosk-methods#uwp) or a [Windows desktop application](https://docs.microsoft.com/windows/configuration/kiosk-methods#classic). For a kiosk that people can sign in to with their accounts or that runs more than one app, choose a [multi-app kiosk](https://docs.microsoft.com/windows/configuration/kiosk-methods#desktop).

## Which type of user account will be the kiosk account?
The kiosk account can be a local standard user account, a domain account, or an Azure Active Directory (Azure AD) account, depending on the method that you use to configure the kiosk. If you want people to sign in and authenticate on the device, you should use a multi-app kiosk configuration. The single-app kiosk configuration doesn't require people to sign in to the device, although they can sign in to the kiosk app if you select an app that has a sign-in method.

## Kiosk Capabilities for Iot Enterprise
| Mode | Features | Description | Customer Usage  |
|------|----------|------------ |-----------------|
| Assigned Access | Single-app Kiosk (UMP)  | Auto launches a UWP app in full screen and prevents access to other system functions and monitors the lifecycle of the kiosk app. Only supports one single-app kiosk profile under one account per device. | Digital Signs & Single Function Devices
| Assigned Access | Single-app Kiosk (Browser) | Auto launches the browser and prevents access to other system functions, while monitoring the lifecycle of browser. Only supports one single-app kiosk profile under one account per device. | Public Browsing Kiosks & Digital Signs |
| Assigned Access | Single-app Kiosk (Browser) - Multi-Profile | Same single-app kiosk browser as above but enables the PC to be configured with multiple single-app kiosk profiles which can be assigned by the IT admin to multiple user accounts | Schools/Education |
| Assigned Access | Multi-app kiosk | Always auto launches a restricted Start menu in full screen with the list of allowed app tiles. Supports configuring different multi-app kiosk profiles for different users/user groups per device. | First-line Workers & Industrial PCs/Tablets |
| Shell Launcher | Shell Launcher | Auto launches an app that the customer specifies and monitors the lifecycle of this app. App can be used as a ‘shell’ if desired. No default lockdown policies like hotkey blocking are enforced in Shell Launcher. | Fixed purpose devices with a custom shell experience |
