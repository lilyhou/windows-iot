---
title: Security
author: rsameser
ms.author: riameser
ms.date: 10/28/2020
ms.topic: article
ms.prod: windows-iot
ms.technology: iot
description: Learn about the Security features of Windows 10 IoT Enterprise.
keywords: IoT Enterprise, Security
---

# Security
Windows 10 IoT Enterprise comes with a host of [security offerings](https://docs.microsoft.com/windows/whats-new/ltsc/whats-new-windows-10-2019#security) that you can leverage to best fit your solution. From [BitLocker](https://docs.microsoft.com/windows/security/information-protection/bitlocker/bitlocker-group-policy-settings#bkmk-unlockpol3) to [Identity Protection](https://docs.microsoft.com/windows/security/identity-protection/hello-for-business/hello-features) to [Windows Defender Advanced Threat Protection](https://docs.microsoft.com/windows/security/threat-protection/), every solution can be customized to meet your needs and keep your data and device secure.

## Device Health Attestation
Modern malware is getting more and more sophisticated. Some of them, specifically bootkits, are capable of starting before Windows. [Device Health Attestation](https://github.com/ms-iot/iot-core-azure-dm-client/blob/master/docs/device-health-attestation.md) can be used to detect and remediate in the unlikely event where a device is infected. The device's firmware logs the boot process, and Windows can send it to a trusted Health Attestation Server that can objectively assess the device's health.
