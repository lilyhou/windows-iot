---
title: Shell Launcher
author: rsameser
ms.author: riameser
ms.date: 11/19/2020
ms.topic: article
ms.prod: windows-iot
ms.technology: iot
description: Learn about the Shell Launcher Feature in Windows 10 IoT Enterprise.
keywords: Lockdown, Shell Launcher
---
# Shell Launcher
Using [Shell Launcher](https://docs.microsoft.com/windows/configuration/kiosk-shelllauncher), you can configure a kiosk device to run a Windows Desktop or Universal Windows Application as the user interface. The application that you specify replaces the default shell (explorer.exe) that usually runs when a user logs on. This type of single-app kiosk does not run above the lock screen. Methods of controlling access to other desktop applications and system components can be used in addition to using the Shell Launcher such as, [group policy](https://www.microsoft.com/download/details.aspx?id=25250), [AppLocker](https://docs.microsoft.com/windows/iot-enterprise/advanced_lockdown_features#applocker) and [mobile device management](https://docs.microsoft.com/windows/client-management/mdm/)

In Shell Launcher v1, available in Windows 10, you can only specify a Windows desktop application as the replacement shell. In Shell Launcher v2, available in Windows 10, version 1809 and above, you can also specify a UWP app as the replacement shell. To use Shell Launcher v2 in version 1809, you need to install the KB4551853 update.

## Differences between Shell Launcher v1 and Shell Launcher v2
Shell Launcher v1 replaces ```explorer.exe```, the default shell, with ```eshell.exe``` which can launch a Windows desktop application.

Shell Launcher v2 replaces ```explorer.exe``` with ```customshellhost.exe```. This new executable file can launch a Windows desktop application or a UWP app.

In addition to allowing you to use a UWP app for your replacement shell, Shell Launcher v2 offers additional enhancements:

* You can use a custom Windows desktop application that can then launch UWP apps, such as Settings and Touch Keyboard.
* From a custom UWP shell, you can launch secondary views and run on multiple monitors.
* The custom shell app runs in full screen, and can run other apps in full screen on user’s demand.
For sample XML configurations for the different app combinations, see [Samples for Shell Launcher v2](https://github.com/Microsoft/Windows-iotcore-samples/tree/develop/Samples/ShellLauncherV2).

## Turn on Shell Launcher
Shell Launcher is an optional component and is not turned on by default in Windows 10. It must be turned on prior to configuring. You can turn on and configure Shell Launcher in a customized Windows 10 image (.wim) if Microsoft Windows has not been installed. If Windows has already been installed and you are applying a provisioning package to configure Shell Launcher, you must first turn on Shell Launcher in order for a provisioning package to successfully apply.

### Enable Shell Launcher using Control Panel
1. In the Search the web and Windows field, type Programs and Features and either press Enter or tap or click Programs and Features to open it.
2. In the Programs and Features window, click Turn Windows features on or off.
3. In the Windows Features window, expand the Device Lockdown node, select or clear the checkbox for Shell Launcher, and then click OK.
4. The Windows Features window indicates that Windows is searching for required files and displays a progress bar. Once found, the window indicates that Windows is applying the changes. When completed, the window indicates the requested changes are completed.
5. Click Close to close the Windows Features window.

## Configure Shell Launcher
There are two ways you can configure Shell Launcher:
1. In Windows 10, version 1803, you can configure Shell Launcher v1 using the ShellLauncher node of the Assigned Access Configuration Service Provider (CSP). See AssignedAccess CSP for details. Configuring Shell Launcher using this method also automatically enables Shell Launcher on the device, if the device supports it. In Windows 10, version 1809 with the KB4551853 update, you can also configure Shell Launcher v2 using the ShellLauncher node of the AssignedAccess CSP.
2. Use the Shell Launcher v1 WMI providers or Shell Launcher v2 bridge WMI directly in a PowerShell script or application.

You can configure the following options for Shell Launcher:
* Enable or disable Shell Launcher.
* Specify a shell configuration for a specific user or group.
* Remove a shell configuration for a specific user or group.
* Change the default shell configuration.
* Get information on a shell configuration for a specific user or group.

> [!NOTE]
> Changes do not take effect until a user signs in.

## Additional Resources
* [Use Shell Launcher to create a Windows 10 Kiosk](https://docs.microsoft.com/windows/configuration/kiosk-shelllauncher)
* [Launch different shells for different user accounts](https://docs.microsoft.com/windows-hardware/customize/enterprise/shell-launcher#launch-different-shells-for-different-user-accounts)
* [Perform an action when the shell exits](https://docs.microsoft.com/windows-hardware/customize/enterprise/shell-launcher#perform-an-action-when-the-shell-exits)
* [Shell Launcher user rights](https://docs.microsoft.com/windows-hardware/customize/enterprise/shell-launcher#shell-launcher-user-rights)
