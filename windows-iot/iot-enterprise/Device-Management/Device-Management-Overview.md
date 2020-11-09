---
title: Device Management Overview
author: rsameser
ms.author: riameser
ms.date: 11/09/2020
ms.topic: article
ms.prod: windows-iot
ms.technology: iot
description: Learn about the Device Management feature of Windows 10 IoT Enterprise.
keywords: IoT Enterprise, Device Management, MDM, Intune, SCCM, Azure Device Twin, Endpoint Manager, Device Health
---
# Device Management Overview
Managing a device is now easier than ever on Windows 10 IoT Enterprise. There are multiple options that your organization can choose from in order to best support your devices.

## Mobile Device Management
Windows 10 provides an enterprise management solution to help IT pros manage company security policies and business applications, while avoiding compromise of the users’ privacy on their personal devices. A built-in management component can communicate with the management server. Check out [What's new in mobile device enrollment and management](https://docs.microsoft.com/windows/client-management/mdm/new-in-windows-mdm-enrollment-management#whatsnew10) to further understand the capabilities that are being offered.

## Microsoft Intune
[Microsoft Intune](https://docs.microsoft.com/mem/intune/fundamentals/what-is-intune) is a cloud-based service that focuses on mobile device management (MDM) and mobile application management (MAM). You control how your organization’s devices are used and can configure specific policies to control applications. Intune is part of [Microsoft's Enterprise Mobility + Security (EMS) suite](https://www.microsoft.com/microsoft-365/enterprise-mobility-security?rtc=1). Intune integrates with Azure Active Directory (Azure AD) to control who has access, and what they can access. It also integrates with Azure Information Protection for data protection.

## Microsoft Endpoint Manager (Formerly SCCM)
[Microsoft Endpoint Manager](https://docs.microsoft.com/mem/configmgr/core/understand/introduction) is an integrated solution for managing all of your devices. Microsoft brings together Configuration Manager and Intune, without a complex migration, and with simplified licensing. Continue to leverage your existing Configuration Manager investments, while taking advantage of the power of the Microsoft cloud at your own pace.

### SCCM
Starting in version 1910, [Configuration Manager](https://docs.microsoft.com/mem/configmgr/core/understand/what-happened-to-sccm) current branch is now part of Microsoft Endpoint Manager. Version 1906 and earlier are still branded System Center Configuration Manager. The Microsoft Endpoint Manager brand will appear in the product and documentation over the coming months.

## Azure IoT Device Agent
The [Azure Device Agent](https://docs.microsoft.com/windows/iot-core/manage-your-device/azureiotda) is a ready-to-build open-source package that enables remote device management capabilities. The Azure Device Agent is supported on Windows 10 IoT Enterprise and works on devices connected via the IoT Hub. OEMs can now [build](https://github.com/ms-iot/azure-client-tools/blob/master/docs/device-agent/device-agent.md) devices that support SCCM, Intune, or Azure IoT Hub for device management and leave it up to their customers to select the device management solution that fits them best.

## Device Health Attestation
Modern malware is getting more and more sophisticated. Some of them, specifically bootkits, are capable of starting before Windows. [Device Health Attestation](https://github.com/ms-iot/iot-core-azure-dm-client/blob/master/docs/device-health-attestation.md) can be used to detect and remediate in the unlikely event where a device is infected. The device's firmware logs the boot process, and Windows can send it to a trusted Health Attestation Server that can objectively assess the device's health.
