---
title: Technical Breakdown
author: rsameser
ms.author: riameser
ms.date: 10/09/2020
ms.topic: article
ms.prod: windows-iot
ms.technology: iot
description: Learn about what Technical Components of Windows 10 IoT Enterprise.
keywords: IoT Enterprise, Cloud Connectivity, Deployment Framework, Device Drivers, Device Management, Networking, OEM Software, Security, Updates, Windows Analytics, Zero Exhaust
---

# Technical Breakdown
This document outlines the key features found in Windows 10 IoT Enterprise. The sections below provide a brief overview as well as links to supplemental resources to further understand feature specifications, use cases, additional documentation.

## Accessibility and Privacy
Microsoft is dedicated to making its products and services accessible and usable for everyone. Windows 10 IoT Enterprise includes accessibility features that benefit all users. These features make it easier to customize the device and give users with different abilities options to improve their experience with Windows. To see more accessibility features please read [Accessibility information for IT Professionals](https://docs.microsoft.com/windows/configuration/windows-10-accessibility-for-itpros)
Windows 10 IoT Enterprise provides users more accessibility and privacy options.
Microsoft always protects user data and respects your privacy. Under privacy settings, you can now delete the diagnostic data your device has sent to Microsoft. You can also view this diagnostic data using the [Diagnostic Data Viewer](https://docs.microsoft.com/windows/privacy/diagnostic-data-viewer-overview) application.

## Cloud Connectivity
** Need some more clarification on Cloud Connectivity strategy, are we following the IoT Core path where we are suggesting to users that they use Azure IoT Hub? If so, do we need to create a tutorial, similar to what is found for IoT Core?

IoT solutions are built on cloud computing. The ability to communicate with the cloud and derive insight from the data is an essential part of any IoT project. With Windows 10 IoT Enterprise, migration to the cloud is done easier than ever with the help of [Azure IoT Hub](https://azure.microsoft.com/services/iot-hub/).

## Deployment Framework
In order to deploy your Windows 10 IoT Enterprise solution, follow this step-by-step guide on [GitHub](https://github.com/ms-iot/windows-iotent-deploy).

## Device Drivers
Device Drivers are essential for any IoT device. This section outlines how to write device drivers, how to driver signing works in Windows 10 IoT Enterprise (this is different than traditional client signing), and how to add device drivers to images.  

### How to Write Device Drivers
Windows contains [built-in drivers](https://docs.microsoft.com/windows-hardware/drivers/gettingstarted/do-you-need-to-write-a-driver-) for many device types. If there is a built-in driver for your device type, you won't need to write your own driver. Your device can use the built-in driver. However if you need to write a device driver for your device, please leverage the [Windows Driver Kit (WDK)](https://docs.microsoft.com/windows-hardware/drivers/ddi/).  

### Device Signing
In Windows 10 IoT Enterprise, the device signing process is different than the [traditional client signing](https://docs.microsoft.com/windows-hardware/drivers/install/driver-signing ) process.  
[Insert the steps, and explain the difference for IoT Enterprise requirements here]

### How to Add Device Drivers to Images
With Windows 10 IoT Enterprise, you can add device drivers to a Windows image before, during, or after you deploy the image. When planning how to add drivers to your Windows deployment, it's important to understand how driver folders are added to the image, how driver ranking affects deployment, and the digital signature requirements for drivers. To understand more about how to add drivers, check out the following article, [Device Drivers](https://docs.microsoft.com/windows-hardware/manufacture/desktop/device-drivers-and-deployment-overview).

## Device Management
Managing a device is now easier than ever on Windows 10 IoT Enterprise. Through Mobile Device Management (MDM) you have full control which devices are enrolled in various policies. Check out [What's new in mobile device enrollment and management](https://docs.microsoft.com/windows/client-management/mdm/new-in-windows-mdm-enrollment-management#whatsnew10) to further understand the capabilities that are being offered. Also, [enrolling](https://docs.microsoft.com/windows/client-management/mdm/mobile-device-enrollment) and [disabling](https://docs.microsoft.com/windows/client-management/mdm/mobile-device-enrollment#disable-mdm-enrollments) MDM policies are also now easier than ever.

## Networking
** Unsure of the scope of Networking in Windows 10 IoT Enterprise.
Possible topic: [Miracast](https://docs.microsoft.com/windows/whats-new/ltsc/whats-new-windows-10-2019#networking) (is this relevant?)

## OEM Software
Most of our solutions are customized by our OEM partners. OEM software plays a big role in the functionality of the IoT Device. Windows 10 IoT Enterprise supports OEM customization and allows for a custom-built device to be run on top of the operating system.
To assist our OEM customers, we offer [Audit Mode](https://docs.microsoft.com/windows-hardware/manufacture/desktop/audit-mode-overview) which allows administrators to boot directly to the desktop before you get to the Windows Welcome screen, giving them the opportunity to install Windows Updates, drivers, and other software as needed.

## Security
Windows 10 IoT Enterprise comes with a host of [security offerings](https://docs.microsoft.com/windows/whats-new/ltsc/whats-new-windows-10-2019#security) that you can leverage to best fit your solution. From [BitLocker](https://docs.microsoft.com/windows/security/information-protection/bitlocker/bitlocker-group-policy-settings#bkmk-unlockpol3) to [Identity Protection](https://docs.microsoft.com/windows/security/identity-protection/hello-for-business/hello-features) to [Windows Defender Advanced Threat Protection](https://docs.microsoft.com/windows/security/threat-protection/), every solution can be customized to meet your needs and keep your data and device secure.

## Updates
A major advantage of using Window 10 IoT Enterprise is having complete control on windows updates for all your devices. Through [Windows Intune](https://docs.microsoft.com/mem/intune/protect/windows-update-settings), you have the ability to configure update settings on devices and to defer update installations. You can also prevent devices from installing features from new Windows versions to help keep them stable, while allowing those devices to continue installing updates for quality and security. Read more about how Windows Intune can help you manage updates [here](https://docs.microsoft.com/mem/intune/protect/windows-update-for-business-configure).

## Windows Analytics
** Should this be called Desktop Analytics? -> "Desktop Analytics is a successor of Windows Analytics, which retired on January 31, 2020."

Harness the power of Windows Analytics in your Windows 10 IoT Enterprise solution. Some of the popular features are upgrade readiness, [update compliance](https://docs.microsoft.com/windows/deployment/update/update-compliance-monitor) and device health.
Upgrade readiness helps you ensure that applications and drivers are ready for a Windows 10 upgrade by also providing troubleshooting guidance, and per-device readiness and tracking details. Update Compliance helps you to keep Windows 10 devices in your organization secure and up to date. Maintaining devices is made easier with Device Health, a new, premium analytic tool that identifies devices and drivers that crash frequently and might need to be rebuilt or replaced.

## Zero Exhaust
Manage connections from the Windows 10 operating system components to Microsoft services in real time with Zero Exhaust policies. You can read more about how to configure these settings [here](https://docs.microsoft.com/windows/privacy/manage-connections-from-windows-operating-system-components-to-microsoft-services)
