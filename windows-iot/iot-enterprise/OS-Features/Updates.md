---
title: Updates
author: rsameser
ms.author: riameser
ms.date: 1/27/2021
ms.topic: article
ms.prod: windows-iot
ms.technology: iot
description: Learn about the Update features of Windows 10 IoT Enterprise.
keywords: IoT Enterprise, Updates
---

# Updates
Connected devices have the challenge of new security threats, updates are an essential tool to address this.

Windows Update Advantage:
- Keeps device up to date with critical security software updates​
- Utilize the Microsoft proven and scalable infrastructure
- Updates can be easily managed and controlled by device owners

Windows 10 IoT Enterprise gives the administrator the power to manage and control updates as per your device and organization requirements.

## Windows Intune
A major advantage of using Window 10 IoT Enterprise is having complete control on windows updates for all your devices. Through [Windows Intune](https://docs.microsoft.com/mem/intune/protect/windows-update-settings), you have the ability to configure update settings on devices and to defer update installations. You can also prevent devices from installing features from new Windows versions to help keep them stable, while allowing those devices to continue installing updates for quality and security. Read more about how Windows Intune can help you [manage updates](https://docs.microsoft.com/mem/intune/protect/windows-update-for-business-configure).

## Turn off Windows Updates
You can configure Windows Update in several ways, and not all policies are applicable to all devices. As a general rule, IoT devices require special attention to the servicing and management strategy to be used on the devices. If your servicing strategy is to disable all Windows Update features, you have two possible approaches. You can turn off updates via [Group Policy](https://docs.microsoft.com/windows-hardware/manufacture/desktop/iot-ent-configure-policy-settings#windows-update-summary) or [Registry](https://docs.microsoft.com/windows/privacy/manage-connections-from-windows-operating-system-components-to-microsoft-services#bkmk-wu).

>[!NOTE]
>
> By setting this policy, it will also stop performing updates from other machines on the local network. To confirm this behavior, you can also turn off [Delivery Optimization](https://docs.microsoft.com/windows/privacy/manage-connections-from-windows-operating-system-components-to-microsoft-services#28-delivery-optimization) which is the subsystem for getting updates from others on your local network.
