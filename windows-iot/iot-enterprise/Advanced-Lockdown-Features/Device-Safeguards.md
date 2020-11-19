---
title: Device Safeguards
author: rsameser
ms.author: riameser
ms.date: 11/19/2020
ms.topic: article
ms.prod: windows-iot
ms.technology: iot
description: Learn about the Device Safeguard features of Windows 10 IoT Enterprise.
keywords: Filtering and Controlling, USB Access
---

# Device Safeguards
Windows 10 IoT Enterprise gives you the power as the administrator of your devices to set certain policies to protect your IoT devices. Whether that be against device tampering, malware infections, data loss or preventing peripherals from gaining access to your device, Windows 10 IoT Enterprise gives you the power to create a customized experience that safeguards against these threats. In a Windows 10 device restrictions profile, most configurable settings are deployed at the device level using device groups. Policies deployed to user groups apply to targeted users, and apply to users who have an Intune license, and sign in to that device. The following guide reviews various policies that can be configured to create a safe and secure device usage experience.

## Control Device Installation
By default, Windows 10 automatically downloads driver software for any devices that been detected. To ensure that your device will not be compromised by any external drives, you can set policies to ensure in the Local Group Policy Editor to match your needs.

### Allow Installation of Devices that Match any of these device instance IDs
This policy setting allows you to specify a list of device instance IDs for devices that Windows is allowed to install. Use this policy setting only when the "Prevent installation of devices not described by other policy settings" policy setting is enabled. Other policy settings that prevent device installation take precedence over this one.

If you enable this policy setting, Windows is allowed to install or update any device whose Plug and Play device instance ID appears in the list you create, unless another policy setting specifically prevents that installation (for example, the "Prevent installation of devices that match any of these device IDs" policy setting, the "Prevent installation of devices for these device classes" policy setting, the "Prevent installation of devices that match any of these device instance IDs" policy setting, or the "Prevent installation of removable devices" policy setting).

To Enable this Policy:
1. Open the Local Group Policy Editor
2. Select "Computer Configuration" >> Administrative Templates >> System >> Device Installation >> Device Installation Restrictions
3. Select "Prevent Installation of Removable Devices"
4. Select 'Enabled'
5. To create a list of devices, click 'Show'.
6. In the Show Contents dialog box, in the Value column, type a Plug and Play device instance ID
7. Apply Changes, Restart Device

> [!NOTE]
> If you disable or do not configure this policy setting, and no other policy setting describes the device, the "Prevent installation of devices not described by other policy settings" policy setting determines whether the device can be installed.

#### Look up device ID
You can use Device Manager to look up a device ID.

1. Open Device Manager.
2. Click **View** and select **Devices by connection**.
3. From the tree, right-click the device and select **Properties**.
4. In the dialog box for the selected device, click the **Details** tab.
5. Click the **Property** drop-down list and select **Hardware Ids**.
6. Right-click the top ID value and select **Copy**.

For information about Device ID formats, see [Standard USB Identifiers](https://docs.microsoft.com/windows-hardware/drivers/install/standard-usb-identifiers).

For information on vendor IDs, see [USB members](https://www.usb.org/members).

The following is an example for looking up a device vendor ID or product ID (which is part of the device ID) using PowerShell:
```
PowerShell
Get-WMIObject -Class Win32_DiskDrive |
Select-Object -Property *
```

### Display a Custom Message When Installation is Prevented by a Policy Setting
This policy setting allows you to display a custom message to users in a notification when a device installation is attempted and a policy setting prevents the installation.

If you enable this policy setting, Windows displays the text you type in the Detail Text box when a policy setting prevents device installation.

To Enable this Policy:
1. Open the Local Group Policy Editor
2. Select "Computer Configuration" >> Administrative Templates >> System >> Device Installation >> Device Installation Restrictions
3. Select "Display a custom message when installation is  prevented by a policy setting"
4. Select 'Enabled'
5. Enter the text you wish users to see (Max 128 chars) in textbook
6. Apply Changes, Restart Device

> [!NOTE]
> If you disable or do not configure this policy setting, Windows displays a default message when a policy setting prevents device installation.

### Allow Administrators to Override Device Installations
This policy setting allows you to determine whether members of the Administrators group can install and update the drivers for any device, regardless of other policy settings.

If you enable this policy setting, members of the Administrators group can use the Add Hardware wizard or the Update Driver wizard to install and update the drivers for any device.

To Enable this Policy:
1. Open the Local Group Policy Editor
2. Select "Computer Configuration" >> Administrative Templates >> System >> Device Installation >> Device Installation Restrictions
3. Select "Allow Administrators to Override Device Installations"
4. Select 'Enabled'
5. Apply Changes, Restart Device

> [!NOTE]
> If you disable or do not configure this policy setting, members of the Administrators group are subject to all policy settings that restrict device installation.

## Restricting Removable Drives
This policy setting allows you to prevent Windows from installing removable devices. A device is considered removable when the driver for the device to which it is connected indicates that the device is removable. For example, a Universal Serial Bus (USB) device is reported to be removable by the drivers for the USB hub to which the device is connected.

To Enable this Policy:
1. Open the Local Group Policy Editor
2. Select "Computer Configuration" >> Administrative Templates >> System >> Device Installation >> Device Installation Restrictions
3. Select "Prevent Installation of Removable Devices"
4. Select 'Enabled'
5. Apply Changes, Restart Device

>[!Note]
This policy setting takes precedence over any other policy setting that allows Windows to install a device. If you disable or do not configure this policy setting, Windows can install and update device drivers for removable devices as allowed or prevented by other policy settings.

## Create customized alerts and response actions
You can create [custom alerts and response actions](https://docs.microsoft.com/windows/security/threat-protection/device-control/control-usb-devices-using-intune#create-customized-alerts-and-response-actions) with the WDATP Connector and the custom detection rules:

**Wdatp Connector response Actions:**

**Investigate:** Initiate investigations, collect investigation package, and isolate a machine.

**Threat Scanning** on USB devices.

**Restrict execution of all applications** on the machine except a predefined set
MDATP connector is one of over 200 pre-defined connectors including Outlook, Teams, Slack, etc. Custom connectors can be built.
- [More information on WDATP Connector Response Actions](https://docs.microsoft.com/connectors/wdatp/)

**Custom Detection Rules Response Action:**
Both machine and file level actions can be applied.
- [More information on Custom Detection Rules Response Actions](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/custom-detection-rules)

For information on device control related advance hunting events and examples on how to create custom alerts, see [Advanced hunting updates: USB events, machine-level actions, and schema changes](https://techcommunity.microsoft.com/t5/Microsoft-Defender-ATP/Advanced-hunting-updates-USB-events-machine-level-actions-and/ba-p/824152).

## Respond to threats
You can create custom alerts and automatic [response actions](https://docs.microsoft.com/windows/security/threat-protection/device-control/control-usb-devices-using-intune#respond-to-threats) with the [Microsoft Defender for Endpoint Custom Detection Rules](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/custom-detection-rules). Response actions within the custom detection cover both machine and file level actions. You can also create alerts and automatic response actions using [PowerApps](https://powerapps.microsoft.com/) and [Flow](https://flow.microsoft.com/) with the [Microsoft Defender for Endpoint connector](https://docs.microsoft.com/connectors/wdatp/). The connector supports actions for investigation, threat scanning, and restricting running applications. It is one of over 200 pre-defined connectors including Outlook, Teams, Slack, and more. Custom connectors can also be built. See [Connectors](https://docs.microsoft.com/connectors/) to learn more about connectors.

For example, using either approach, you can automatically have the Microsoft Defender Antivirus run when a USB device is mounted onto a machine.

## Additional Resources  
* [Policy CSP - DeviceInstallation](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-deviceinstallation)
* [Defender/AllowFullScanRemovableDriveScanning](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-defender#defender-allowfullscanremovabledrivescanning)
* [Perform a custom scan of a removable device](https://aka.ms/scanusb)
* [Device Control PowerBI Template for custom reporting](https://github.com/microsoft/MDATP-PowerBI-Templates)
* [Windows Information Protection](https://docs.microsoft.com/windows/security/information-protection/windows-information-protection/create-wip-policy-using-intune-azure)
