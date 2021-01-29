---
title: Embedded Mode
author: rsameser
ms.author: riameser
ms.date: 1/29/2021
ms.topic: article
ms.prod: windows-iot
ms.technology: iot
description: Learn about the Embedded Mode features of Windows 10 IoT Enterprise.
keywords: IoT Enterprise, Networking
---
# Embedded mode
Embedded Mode is a Win32 service. In Windows 10 it only starts if the user, an application or another service starts it. When the Embedded Mode service is started, it is runs as LocalSystem in a shared process of svchost.exe along with other services. Embedded Mode is supported on Windows 10 IoT Enterprise.

Embedded Mode enables:
* Background Applications
* Use of the lowLevelDevice capability
* Use of systemManagement capability

## Enable Embedded Mode
Embedded mode must be enabled by following the steps below on Windows IoT Enterprise.
1. Run the Command Prompt as an administrator.
2. Enter the following command **sc config embeddedmode start= demand**
3. Close the command window and restart the computer.

*The embeddedmode service is using the embeddedmodesvc.dll file that is located in the %WinDir%\System32 folder. If the file is changed, damaged or deleted, you can restore its original version from Windows 10 installation media*.

> [!NOTE]
> If Embedded Mode fails to start, the failure details are being recorded into Event Log. Then Windows 10 will start up and notify the user that the embeddedmode service has failed to start due to the error.


## Background Applications
[Background Applications](https://docs.microsoft.com/windows/iot-core/develop-your-app/backgroundapplications) are created using the Background Application (IoT) template in Visual Studio.

Background applications run without stopping and without resource limits. Also, if the background application stops for some reason and embedded mode is enabled the background application will be restarted by the system.

While the system will automatically restart background applications, system lockdown features must be enabled to prevent users from stopping or interfering with the operation of Background Applications.

## lowLevel device Capability and lowLevelDevice capability

The **lowLevel** device Capability gives access to low-level hardware interfaces like GPIO, SPI, and I2C.

* [Blinky Sample(GPIO)](https://developer.microsoft.com/windows/iot/samples/helloblinky)
* [Accelerometer Sample](https://github.com/Microsoft/Windows-iotcore-samples/tree/master/Samples/Accelerometer)

The **lowLevelDevices** Capability allows apps to access custom devices when a number of additional requirements are met. This
capability should not be confused with the lowLevel device capability, which allows access to GPIO, I2C, SPI, and PWM devices.

Refer to [App capability declarations](https://docs.microsoft.com/windows/uwp/packaging/app-capability-declarations) for details.

## systemManagment Capability

When you enable the systemManagment capabilities for your application, this is the set of APIs that gets unlocked:  

* [Windows.System.ProcessLauncher](https://msdn.microsoft.com/library/windows/apps/windows.system.processlauncher.aspx)
* [Windows.System.TimeZoneSettings](https://msdn.microsoft.com/library/windows/apps/windows.system.timezonesettings.aspx)
* [Windows.System.ShutdownManager](https://msdn.microsoft.com/library/windows/apps/windows.system.shutdownmanager.aspx)
* [Windows.Globalization.Language.TrySetInputMethodLanguageTag](https://msdn.microsoft.com/library/windows/apps/windows.globalization.language.trysetinputmethodlanguagetag.aspx)

## Debugging Background Applications

If you are debugging on a device and you see either of the following error messages you need to ensure AllowEmbeddedMode is enabled on the device and that the Embedded Mode service is running:

* There are no more endpoints available from the endpoint mapper.
* This program is blocked by group policy. For more information, contact your system administrator.
