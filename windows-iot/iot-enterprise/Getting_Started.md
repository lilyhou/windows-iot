---
title: Getting Started with Windows 10 IoT Enterprise
author: rsameser
ms.author: riameser
ms.date: 1/26/2021
ms.topic: article
ms.prod: windows-iot
ms.technology: iot
description: Learn about what Windows 10 IoT Enterprise is and what you can do with it.
keywords: IoT Enterprise, binary, fixed purpose devices, LTSC, Silicon
---

# Getting Started with Windows 10 IoT Enterprise
This article will give you an overview of the product and guide you through how to get started with Windows 10 IoT Enterprise.

## What is Windows 10 IoT Enterprise?
Windows 10 IoT Enterprise is a full version of Windows 10 that delivers enterprise manageability and security to IoT solutions. Windows 10 IoT Enterprise shares all the benefits of the worldwide Windows ecosystem. It is a binary equivalent to Windows 10 Enterprise, so you can use the same familiar development and management tools as client PCs and laptops. However, when it comes to licensing and distribution, the desktop version and IoT versions differ. Windows 10 IoT Enterprise offers both LTSC and SAC options, and OEMs can choose the one they need for their devices. Please review [licensing](./Commercialization/Licensing.md) for more details.


## Why Customer Choose Windows 10 IoT Enterprise
There are three big reasons why customers choose to develop with Windows 10 IoT Enterprise

1. **Fast** - Quickly get IoT devices to market and maintain for the long term with out of the box OS
2. **Secure** - Help keep devices secure for the long term with turnkey enterprise platform security
3. **Smart** - Easily bring AI and ML to the edge with Windows ML and support from Azure IoT Edge

> [!TIP]
>
> If you are building any kind of **OEM style appliance**, such as a point-of-sale or retail device, industrial automation equipment, digital signage, medical equipment or any appliance with a screen - Windows 10 IoT Enterprise is the solution for you. See how our [customers](https://www.microsoft.com/WindowsForBusiness/windows-iot) are using Windows 10 IoT Enterprise to accomplish their business goals.


## Key Differentiators
Windows 10 IoT Enterprise, is the full version for Windows 10 Enterprise with 3 key differences:
1. Windows 10 IoT Enterprises offers customers with Long-Term Servicing Channels options  
  1. [Long-Term Servicing Channel (LTSC)](https://docs.microsoft.com/windows/whats-new/ltsc/)
  1. [Semi-Annual Channel (SAC)](./Commercialization/Licensing.md)
1. Activation Style

1. Policies

| Policy Name | Windows 10 IoT Enterprise | Windows 10 Enterprise |
|-----|-----|-----|
|Allow-WindowsSubcription|0|3|
|Security-SPP-LowerEventLogType-DeferredState|1|default (0)|
|ServicingStack-License-ReservedStorageAllowed|0|default (1)|


## Documentation Overview
This documentation set will cover the technical breakdown of what's included when you choose to use Windows 10 IoT Enterprise.


### Hardware Guidance
This section provides insight into the hardware needed to run Windows 10 IoT Enterprise as your device's OS.

Articles include:
* [Hardware Requirements](./Hardware-Guidance/Hardware_Requirements.md)
* [Selecting SoCs and Custom Boards](./Hardware-Guidance/SoCs.md)
* [How to Start Prototyping](./Hardware-Guidance/Prototype.md)  


### Kiosk Mode
This section walks users through the features and functionalities of Kiosk Mode and how to enable those features on Windows 10 IoT Enterprise.

Articles include:
* [Kiosk Mode Overview](./Kiosk-Mode/Kiosk-Mode.md)
* [Single-App Kiosk Mode](./Kiosk-Mode/Single-App-Kiosk.md)
* [Multi-App Kiosk Mode](./Kiosk-Mode/Multi-App-Kiosk.md)
* [Shell Launcher](./Kiosk-Mode/Shell-Launcher.md)
* [Assigned Access](./Kiosk-Mode/Assigned-Access.md)


### Advanced Lockdown Features
This section highlights how to create a lock-down environment with Windows 10 IoT Enterprise OS features.

Articles include:
* [Application Control](./Advanced-Lockdown-Features/Application-Control.md)
* [Edge Swipe Policy](./Advanced-Lockdown-Features/Edge-Swipe-Policy.md)
* [Device Safeguards](./Advanced-Lockdown-Features/Device-Safeguards.md)
* [Keyboard Filter](./Advanced-Lockdown-Features/Keyboard-Filter.md)
* [Unified Write Filter](./Advanced-Lockdown-Features/Unified-Write-Filter.md)
* [Hibernate Once, Resume Many (HORM)](./Advanced-Lockdown-Features/HORM.md)


### Branding Features
This section reviews how to create a custom user-experience that highlights your brand and brings your ideal visual Windows vision to life.

Articles include:
* [Custom Logon](./Branding-Features/Custom-Logon.md)
* [Microsoft Store Access](./Branding-Features/Microsoft-Store-Access.md)
* [Secondary Microsoft Edge Tiles](./Branding-Features/Edge-Tiles.md)
* [Page Visibility](./Branding-Features/Page-Visibility.md)
* [Layout Control](./Branding-Features/Layout-Control.md)
* [Unbranded Boot](./Branding-Features/Unbranded-Boot.md)
* [Update Notification](./Branding-Features/Update-Notification.md)


### Device Management
Learn more about the device management solutions you can take advantage of with Windows 10 IoT Enterprise.

Articles include:
* [Device Management Overview](./Device-Management/Device-Management-Overview.md)
* [Mobile Device Management](./Device-Management/Mobile-Device-Management.md)
* [Application Updates](Device-Management/App-Updates.md)


### IoT Device Features
This section gives an overview of many of the built-in functionalities of Windows 10 IoT Enterprise devices.

Articles include:
* [Security](./OS-Features/Security.md)
* [Updates](./OS-Features/Updates.md)
* [Embedded Mode](./OS-Features/Embedded-Mode.md)
* [Device Drivers](./OS-Features/Device-Drivers.md)
* [Bus Providers](./OS-Features/Bus-Providers.md)
* [Zero Exhaust](./OS-Features/Zero-Exhaust.md)
* [On-Screen Keyboard](./OS-Features/On-Screen-Keyboard.md)
* [Accessibility & Privacy](./OS-Features/Accessibility-Privacy.md)


### Commercialization
Learn how to commercialize your Windows 10 IoT Enterprise devices.

Articles include:
* [Audit Mode](./Commercialization/Audit-Mode.md)
* [Licensing Options (LTSC, SAC)](./Commercialization/Licensing.md)
* [Windows 10 IoT Enterprise Manufacturing Guide](https://docs.microsoft.com/windows-hardware/manufacture/desktop/iot-ent-overview)


### Additional Resources
This documentation set provides additional information to support users that will be updated regularly.

Articles include:
* [Best Practices](./Best_Practices.md)
* [Frequently Asked Questions](./FAQ.md)
* [Release Notes](./Release_Notes.md)
* [Accessibility](./Accessibility.md)
* [Glossary](./Glossary.md)
