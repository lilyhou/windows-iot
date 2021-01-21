---
title: Assigned Access
author: rsameser
ms.author: riameser
ms.date: 1/19/2021
ms.topic: article
ms.prod: windows-iot
ms.technology: iot
description: Learn about the Assigned Access Feature in Windows 10 IoT Enterprise.
keywords: Lockdown, Assigned Access, Kiosk Mode
---
# Assigned Access
Assigned access is a feature on Windows 10 IoT Enterprise that allows you to create a lockdown environment. This allows for users to interact with only one application when they sign into a specified account.

With Assigned access, users won't be able to access Desktop, Start menu, or any other applications, including the Settings app.

This feature makes it easy for anyone to configure Windows 10 devices as point-of-sale (POS) or other kiosk systems.

## Create a User Account
Rather than turn your entire device into a locked-down kiosk system, the assigned access feature allows you to create a separate user account that can only launch a single app. To set this up, you must be logged into Windows as a user with administrator permissions.

On Windows 10, open the Settings app and navigate to **Settings** > **Accounts** > **Family & Other People** and select **Add Someone Else to This PC**.

> [!TIP]
> Windows 10 will guide you towards creating a Microsoft account by default. If you’d rather create a local user account, click “I Don’t Have This Person’s Sign In Information” and then click “Add a User Without a Microsoft Account” to create a new local user account.

## Set Up Assigned Access

For Windows 10 IoT Enterprise, Assigned Access allows:
* Microsoft Edge Web Browser
* Universal Windows Platform (UWP) apps bundled with Windows 10 or installed from the Windows Store can be selected
* Pre-installed desktop applications

When you’re done, walking through the wizard and configuring your Assigned Access account, sign out of your current user account and log into the Assigned Access account. Windows will automatically open the app you chose in full screen mode and won’t allow a user to leave that app. Standard features like the taskbar and Start menu won’t appear.

> [!TIP]
> To leave Assigned Access mode on Windows 10, press Ctrl+Alt+Delete. The account will actually still be logged in and the app will remain running–this method just “locks” the screen and allows another user to log in. To completely terminate the account session, simply restart your computer by clicking the Restart button from the Power menu on the Lock screen.

## Disable Assigned Access
In order to disable an account configured with Assigned Access, please follow these steps:

On Windows 10, open the Settings app and navigate to **Settings** > **Accounts** > **Family & Other People** > **Other users** > **Set up assigned access** > select the account currently setup > select **Don't use assigned access**.

## Additional Resources
* [Single-App Kiosk](https://docs.microsoft.com/windows/configuration/kiosk-single-app)
* [Guidelines for choosing an app for assigned access](https://docs.microsoft.com/windows/configuration/guidelines-for-assigned-access-app)
