---
title: Unbranded Boot
author: rsameser
ms.author: riameser
ms.date: 12/04/2020
ms.topic: article
ms.prod: windows-iot
ms.technology: iot
description: Learn about the Unbranded Boot Feature in Windows 10 IoT Enterprise.
keywords: Branding, Unbranded Boot
---

# Unbranded Boot
You can suppress Windows elements that appear when Windows starts or resumes and can suppress the crash screen when Windows encounters an error that it cannot recover from. This feature is known as [Unbranded Boot](https://docs.microsoft.com/windows-hardware/customize/enterprise/unbranded-boot). This feature allows you to customize and control the user experience during transitions.

## Turn on Unbranded Boot settings
Unbranded Boot is an optional component and is not enabled by default in Windows 10. It must be enabled prior to configuring. For end-users, Unbranded Boot can be configured through **Command Prompt** or **Control Panel**.

### Turn on Unbranded Boot by using Command Prompt
1. Enable the Unbranded boot feature by running the following command in an Administrative Command Prompt:

```
DISM /online /enable-Feature /featureName:Client-DeviceLockdown  
DISM /online /Enable-Feature /FeatureName:Client-EmbeddedBootExp
```

2. Restart the reference device

### Turn on Unbranded Boot by using Control Panel
1. In the **Search the web** and **Windows** field, type Programs and Features and either press Enter or tap or click **Programs and Features** to open it.

2. In the **Programs and Features** window, click **Turn Windows features on or off**.

3. In the **Windows Features** window, expand the **Device Lockdown** node, and check or clear the checkbox for **Unbranded Boot**.

4. Click **OK**. The **Windows Features** window indicates Windows is searching for required files and displays a progress bar. Once found, the window indicates Windows is applying the changes. When completed, the window indicates the requested changes are completed.

5. Click **Close** to close the **Windows Features** window.

## Configure Unbranded Boot settings at runtime using BCDEdit
If Windows has already been installed you cannot apply a provisioning package to configure Unbranded Boot; instead you must use BDCEdit to configure Unbranded boot if Windows is installed.

BCDEdit is the primary tool for editing the startup configuration and is on your development computer in the %WINDIR%\System32 folder. You have administrator rights for it. BCDEdit is included in a typical Windows Preinstallation Environment (Windows PE) 4.0. You can download it from the [BCDEdit Commands for Boot Environment](https://docs.microsoft.com/en-us/previous-versions/windows/hardware/design/dn653986(v=vs.85) in the Microsoft Download Center if needed.

You can customize Unbranded boot from an Administrative Command prompt in the following ways:

* Disable the F8 key during startup to prevent access to the Advanced startup options menu:
```
bcdedit.exe -set {globalsettings} advancedoptions false
```

* Disable the F10 key during startup to prevent access to the Advanced startup options menu:
```
bcdedit.exe -set {globalsettings} optionsedit false
```

* Suppress all Windows UI elements (logo, status indicator, and status message) during startup:
```
bcdedit.exe -set {globalsettings} bootuxdisabled on
```

> [!NOTE]
>
> Anytime you rebuild the BCD information, for example using bcdboot, you'll have to re-run the above commands.

## Additional Resources
* [Configure Unbranded Boot using Unattend](https://docs.microsoft.com/en-us/windows-hardware/customize/enterprise/unbranded-boot#configure-unbranded-boot-using-unattend)
* [Customize the boot screen using Windows Configuration Designer and Deployment Image Servicing and Management (DISM)](https://docs.microsoft.com/windows-hardware/customize/enterprise/unbranded-boot#customize-the-boot-screen-using-windows-configuration-designer-and-deployment-image-servicing-and-management-dism)
* [Replace the startup logo](https://docs.microsoft.com/windows-hardware/customize/enterprise/unbranded-boot#replace-the-startup-logo)
