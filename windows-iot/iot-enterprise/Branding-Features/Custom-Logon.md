---
title: Custom Logon
author: rsameser
ms.author: riameser
ms.date: 12/03/2020
ms.topic: article
ms.prod: windows-iot
ms.technology: iot
description: Learn about the Custom Logon Feature in Windows 10 IoT Enterprise.
keywords: Branding, Custom Logon
---

# Custom Logon
Custom Logon features allow you to take control of the welcome and shutdown screens for your device.

## Feature Benefits
By using custom logon, you can suppress all elements of the Welcome screen UI and provide a custom logon UI for your users. You can also suppress the Blocked Shutdown Resolver (BSDR) screen and automatically end applications while the OS waits for applications to close before a shutdown.

Custom Logon settings do not modify the credential behavior of **Winlogon**, so you can use any credential provider that is compatible with Windows 10 to provide a custom sign-in experience for your device.

## Enable Custom Logon
Custom Logon is an optional component and is not turned on by default in Windows 10. It must be turned on prior to configuring. You can turn on and configure Custom Logon in a customized Windows 10 image (.wim) if Microsoft Windows has not been installed. If Windows has already been installed and you are applying a provisioning package to configure Custom Logon, you must first turn on Custom Logon in order for a provisioning package to be successfully applied.

The Custom Logon feature is available in the Control Panel. You can set Custom Logon by following these steps:

1. In the Search the web and Windows field, type Turn Windows features on or off.
2. In the Windows Features window, expand the Device Lockdown node, and select or clear the checkbox for Custom Logon.

* [Turn on and configure Custom Logon using DISM](https://docs.microsoft.com/en-us/windows-hardware/customize/enterprise/custom-logon#turn-on-custom-logon)
* [Configure Custom Logon settings using Unattend](https://docs.microsoft.com/en-us/windows-hardware/customize/enterprise/custom-logon#turn-on-custom-logon)

## Complementary Features
You may want to use or change some of the following features in conjunction with Custom Logon to complete the user experience.

### Power button
We recommend that you remove the power button from the Welcome screen and block the physical power button so that a user cannot turn off the device when using assigned access or Shell Launcher.

Go to **Power Options** > **Choose what the power button does**, change the setting to **Do nothing**, and then **Save changes**.

### Welcome Screen
You also have the option to remove various buttons from the Welcome screen to create your own customized experience. This includes the [Power Button](https://docs.microsoft.com/windows-hardware/customize/enterprise/complementary-features-to-custom-logon#welcome-screen), [Language Button](https://docs.microsoft.com/windows-hardware/customize/enterprise/complementary-features-to-custom-logon#welcome-screen), [Ease of Access Button](https://docs.microsoft.com/windows-hardware/customize/enterprise/complementary-features-to-custom-logon#welcome-screen), and [Switch user button](https://docs.microsoft.com/windows-hardware/customize/enterprise/complementary-features-to-custom-logon#welcome-screen).

#### Remove Wireless UI from the Welcome screen
You can also remove the Wireless UI option from the Welcome screen by using Group Policy.

To remove Wireless UI from the Welcome screen:
1. From a command prompt, run gpedit.msc to open the Local Group Policy Editor.
2. In the Local Group Policy Editor, under Computer Configuration, expand Administrative Templates, expand System, and then tap or click Logon.
3. Double-tap or click Do not display network selection UI.

## Additional Resources
* [Custom Logon](https://docs.microsoft.com/windows-hardware/customize/enterprise/custom-logon)
* [Complementary features to Custom Logon](https://docs.microsoft.com/windows-hardware/customize/enterprise/complementary-features-to-custom-logon)
* [Troubleshooting Custom Logon](https://docs.microsoft.com/windows-hardware/customize/enterprise/troubleshooting-custom-logon)
