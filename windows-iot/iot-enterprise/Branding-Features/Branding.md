---
title: Branding Features
author: rsameser
ms.author: riameser
ms.date: 09/25/2020
ms.topic: article
ms.prod: windows-iot
ms.technology: iot
description: Learn about the Branding Features of Windows 10 IoT Enterprise.
keywords: Branding, Custom Logon, Layout Control, Microsoft Store Access, Settings Page Visibility, Touch Keyboard, Unbranded Boot, Update Notification
---

# Branding Features
IoT Enterprise provides customers with the ability to create a customized experience on any device running Windows 10. The following features describe how your brand can be tailored to fit your Windows 10 IoT Enterprise experience.

## Custom Logon
Custom Logon features allow you to take control of the welcome and shutdown screens for your device. For example, you can suppress all elements of the Welcome screen UI and provide a custom logon UI. You can also suppress the Blocked Shutdown Resolver (BSDR) screen and automatically end applications while the OS waits for applications to close before a shutdown.

Custom Logon settings do not modify the credential behavior of Winlogon, so you can use any credential provider that is compatible with Windows 10 to provide a custom sign-in experience for your device.

Note, Custom Logon is an optional component and is not turned on by default in Windows 10. It must be [turned on](https://docs.microsoft.com/windows-hardware/customize/enterprise/custom-logon#turn-on-custom-logon) prior to configuring.

## Microsoft Store Access
Access to the Microsoft store can be blocked either to meet requirements for an organization's policy or to achieve a desired customer experience in Windows 10 IoT Enterprise. You have the option to block access to the Microsoft Store through configuring the settings through [AppLocker](https://docs.microsoft.com/windows/configuration/stop-employees-from-using-microsoft-store#block-microsoft-store-using-applocker), or adding a [Group Policy](https://docs.microsoft.com/windows/configuration/stop-employees-from-using-microsoft-store#block-microsoft-store-using-group-policy).

## Secondary Microsoft Edge Tiles
In Windows 10 IoT Enterprise, you have the ability to configure secondary app tiles to create a customized user experience. Primary app tiles are the Start screen tiles that represent and launch an app. A tile that allows a user to go to a specific location in an app is a called secondary tile. Some examples of secondary tiles include: weather updates for a specific city in a weather app, a summary of upcoming events in a calendar app, status and updates from an important contact in a social app or a specific website in Microsoft Edge. For example, you can create secondary tiles for Microsoft Edge that display a custom image, rather than a tile with the standard Microsoft Edge logo in the Start layout enabling you to further brand the user experience.

## Settings Policy: Page Visibility
In Windows 10 IoT there are many [settings policies](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-settings) that can be set. One settings policy that is quite useful is configuring [page visibility](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-settings#settings-pagevisibilitylist). This feature allows you to prevent specific pages in the System Settings app from being visible or accessible, or to do so for all pages except those specified.

** I wonder if this is a feature better suited for "Advanced Lockdown Features", rather than under "Branding"

## Start and Taskbar Layout Control
In Windows 10 IoT Enterprise, organizations can deploy a [customized Start and Taskbar](https://docs.microsoft.com/windows/configuration/windows-10-start-layout-options-and-policies) configuration to their devices. A standard, customized [Start layout](https://docs.microsoft.com/windows/configuration/customize-and-export-start-layout) can be useful on devices that are common to multiple users and devices that are locked down for specialized purposes. Configuring the [taskbar layout](https://docs.microsoft.com/windows/configuration/configure-windows-10-taskbar) allows the organization to pin useful apps for their employees and to remove apps that are pinned by default to provide a specified user experience.

## Unbranded Boot
You can suppress Windows elements that appear when Windows starts or resumes and can suppress the crash screen when Windows encounters an error that it cannot recover from. This feature is known as [Unbranded Boot](https://docs.microsoft.com/windows-hardware/customize/enterprise/unbranded-boot). This feature allows you to customize and control the user experience during transitions.

## Update Notification
In Windows 10 IoT Enterprise, we know that having your device ready for use at all time is very important. We have many features to help you maximize control over your devices' [update notifications](https://docs.microsoft.com/windows/deployment/update/waas-wu-settings#remove-access-to-use-all-windows-update-features) to ensure that you can plan and ahead and control when updates can occur. You can use Group Policy settings, or mobile device management (MDM) to configure when devices will restart after a Windows 10 update is installed. You can schedule update installation and set policies for restart, configure active hours for when restarts will not occur, or you can do both so the user never has to see a notification about an upcoming Windows Update.
