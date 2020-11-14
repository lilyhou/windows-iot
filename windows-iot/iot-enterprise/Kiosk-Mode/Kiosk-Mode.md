---
title: Kiosk Mode
author: rsameser
ms.author: riameser
ms.date: 10/30/2020
ms.topic: article
ms.prod: windows-iot
ms.technology: iot
description: Learn about Kiosk Mode in Windows 10 IoT Enterprise.
keywords: Lockdown, Kiosks, Kiosk Mode
---

# Kiosk Mode  
One of the most exciting features for Windows 10 IoT Enterprise is Kiosk mode. It's inevitable that some devices in your business will and can serve a special purpose, such as a PC in the lobby that customers can use to view your product catalog or a PC displaying visual content as a digital sign. Windows 10 offers two different locked-down experiences for public or specialized use: single-app kiosks or multi-app kiosks.

Kiosk configurations are based on Assigned Access, a feature in Windows 10 that allows an administrator to manage the user's experience by limiting the application entry points exposed to the user.

There are several kiosk configuration methods that you can choose from, depending on your answers to the following questions.

## Which type of app will your kiosk run?
Your kiosk can run a Universal Windows Platform (UWP) app or a Windows desktop application. For [digital signage](https://docs.microsoft.com/windows/configuration/setup-digital-signage), simply select a digital sign player as your kiosk app. Check out the [guidelines for kiosk apps](https://docs.microsoft.com/windows/configuration/guidelines-for-assigned-access-app).

## Which type of kiosk do you need?
If you want your kiosk to run a single app for anyone to see or use, consider a single-app kiosk that runs either a [Universal Windows Platform (UWP) app](https://docs.microsoft.com/windows/configuration/kiosk-methods#uwp) or a [Windows desktop application](https://docs.microsoft.com/windows/configuration/kiosk-methods#classic). For a kiosk that people can sign in to with their accounts or that runs more than one app, choose a [multi-app kiosk](https://docs.microsoft.com/windows/configuration/kiosk-methods#desktop).

## Which type of user account will be the kiosk account?
The kiosk account can be a local standard user account, a local administrator account, a domain account, or an Azure Active Directory (Azure AD) account, depending on the method that you use to configure the kiosk. If you want people to sign in and authenticate on the device, you should use a multi-app kiosk configuration. The single-app kiosk configuration doesn't require people to sign in to the device, although they can sign in to the kiosk app if you select an app that has a sign-in method.

## Kiosk Capabilities for Iot Enterprise
| Mode | Features | Description | Implementation Detail | Customer Usage  |
|--------------|----------|-------------|-----------------------|-----------------|
| Assigned Access | Single-app Kiosk (UMP)  | Auto launches a UWP app in full screen and prevents access to other system functions and monitors the lifecycle of the kiosk app. Only supports one single-app kiosk profile under one account per device.  | UWP based kiosk app runs above lock screen | Digital Signs & Single Function Tables
| Assigned Access | Multi-app kiosk | Always auto launches a restricted Start menu in full screen with the list of allowed app tiles. Supports configuring different multi-app kiosk profiles for different users/user groups per device. | Restricted Shell+Start and apps with default lockdown policies, AppLocker rules and shell runtime checks | First-line Workers & Industrial PCs/Tablets |
| Shell Launcher | Shell Launcher | Auto launches an app that the customer specifies and monitors the lifecycle of this app. App can be used as a ‘shell’ if desired. No Microsoft default lockdown policies enforced - unlike AA (above) with Shell Launcher policies must be implemented by the customer as required. | OEM Custom shell app runs under customshellhost.exe after logon instead of running explorer.exe | Machine Builders & Specialty Tablets |
