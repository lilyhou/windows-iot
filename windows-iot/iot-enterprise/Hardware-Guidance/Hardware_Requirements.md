---
title: Hardware Requirements
author: rsameser
ms.author: riameser
ms.date: 1/19/2021
ms.topic: article
ms.prod: windows-iot
ms.technology: iot
description: Learn about what Hardware is Required for Windows 10 IoT Enterprise.
keywords: IoT Enterprise, Hardware, Windows IoT
---

# Minimum Hardware Requirements for Windows 10 IoT Enterprise
This specification defines the minimum hardware requirements for Windows 10 IoT Enterprise and all types of devices or computers designed for Windows 10, version 1703 or later versions. Microsoft will build and test the Windows 10 IoT Enterprise OS against the requirements described in this specification.

## Overview
This specification defines the minimum hardware requirements necessary to:
* Boot and run Windows 10 IoT Enterprise.
* Update and service Windows 10 IoT Enterprise.

The goal of this specification is to enable OEMs, ODMs, SoC vendors, and other component vendors to make early design decisions for devices and computers that will run Windows 10 IoT Enterprise.

This specification does not provide compatibility and certification requirements for devices and computers that run Windows 10 IoT Enterprise or implementation guidance for exceptional user experiences. 

## Processor
Devices that run Windows 10 IoT Enterprise require a 1 GHz or faster processor or SoC that meets the following requirements:
* Compatible with the x86* or x64 instruction set.
* Supports PAE, NX and SSE2.
* Supports CMPXCHG16b, LAHF/SAHF, and PrefetchW for 64-bit OS installation

> [!NOTE]
> Beginning with Windows 10, version 2004, all new Windows 10 systems will be required to use 64-bit builds and Microsoft will no longer release 32-bit builds for OEM distribution. This does not impact 32-bit customer systems that are manufactured with earlier versions of Windows 10; Microsoft remains committed to providing feature and security updates on these devices, including continued 32-bit media availability in non-OEM channels to support various upgrade installation scenarios.

Check out [Windows IoT Enterprise Processor Requirements](https://docs.microsoft.com/windows-hardware/design/minimum/windows-processor-requirements#windows-iot-enterprise--embedded-processors) to review the latest processor generations and models which are supported. Previous generations of processors and models (indicated by "Up through"), remain supported in addition to the listed processors and models.

Some product editions or edition/processor configurations listed below may have no or limited support. Information on support is available at [Microsoft Support Policy](https://support.microsoft.com/lifecycle) and [Microsoft Lifecycle FAQ](https://support.microsoft.com/help/18581). For specific hardware support, please refer to your Original Equipment Manufacturer (OEM) provider.

## Memory
Devices that run Windows 10 IoT Enterprise must meet the following [RAM requirements](https://docs.microsoft.com/windows-hardware/design/minimum/minimum-hardware-requirements-overview#32-memory).

## Storage
### Storage device size
Devices that run Windows 10 IoT Enterprise must include a storage device that meets the following [size requirements](https://docs.microsoft.com/windows-hardware/design/minimum/minimum-hardware-requirements-overview#331-storage-device-size).

* [Storage Controller Requirements](https://docs.microsoft.com/windows-hardware/design/minimum/minimum-hardware-requirements-overview#332-storage-controller)

## Display and graphics
### Resolution, bit depth, and size
Display size requirements do not apply to Windows 10 IoT Enterprise.

### Graphics
Devices that run Windows 10 for IoT Enterprise must include a GPU that supports DirectX 9 or later.

### Networking
Devices that run Windows 10 IoT Enterprise must include at least one network connectivity option, such as Wi-Fi or an Ethernet adapter.

## Hardware buttons
* [Button implementation requirements for Windows 10 IoT Enterprise](https://docs.microsoft.com/windows-hardware/design/minimum/minimum-hardware-requirements-overview#36-hardware-buttons)
* [Custom Hardware Button Behavior](https://docs.microsoft.com/windows-hardware/design/minimum/minimum-hardware-requirements-overview#66-hardware-button-behavior)

## Trusted Platform Module (TPM)
> [!NOTE]
> While TPM requirements are highly encouraged for Windows 10 IoT Enterprise, it is not required. The use of a TPM for Windows 10 IoT Enterprise devices is determined based on the usage and security requirements of each device.

* [TPM Requirements](https://docs.microsoft.com/windows-hardware/design/minimum/minimum-hardware-requirements-overview#37-trusted-platform-module-tpm)
* [Trusted Platform Module Technology Overview](https://docs.microsoft.com/windows/security/information-protection/tpm/trusted-platform-module-overview)
* [TPM Recommendations](https://docs.microsoft.com/windows/security/information-protection/tpm/tpm-recommendations)

## Additional Resources
* [Shared Minimum Hardware Requirements for Windows OS](https://docs.microsoft.com/windows-hardware/design/minimum/minimum-hardware-requirements-overview#section-60---shared-minimum-hardware-requirements-for-components)
* [Minimum Hardware Requirements](https://docs.microsoft.com/windows-hardware/design/minimum/minimum-hardware-requirements-overview)
* [Windows Processor Requirements](https://docs.microsoft.com/windows-hardware/design/minimum/windows-processor-requirements)
* [Hardware Component Guidelines](https://docs.microsoft.com/windows-hardware/design/component-guidelines/components)
