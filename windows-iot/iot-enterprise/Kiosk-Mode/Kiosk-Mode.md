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
