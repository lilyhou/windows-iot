---
title: Hardware Requirements
author: rsameser
ms.author: riameser
ms.date: 1/8/2021
ms.topic: article
ms.prod: windows-iot
ms.technology: iot
description: Learn about what Hardware is Required for Windows 10 IoT Enterprise.
keywords: IoT Enterprise, Hardware, Windows IoT
---

# Minimum Hardware Requirements for Windows 10 IoT Enterprise
This specification defines the minimum hardware requirements for Windows 10 IoT Enterprise and all types of devices or computers designed for Windows 10, version 1703 or later versions. Microsoft will build and test the Windows 10 OS against the requirements described in this specification.

## Overview
This specification defines the minimum hardware requirements necessary to:
* Boot and run Windows 10.
* Update and service Windows 10.
* Provide a baseline user experience that is comparable with similar devices and computers.
The goal of this specification is to enable OEMs, ODMs, SoC vendors, and other component vendors to make early design decisions for devices and computers that will run Windows 10.

This specification does not provide compatibility and certification requirements for devices and computers that run Windows 10 or implementation guidance for exceptional user experiences. Microsoft will provide this guidance in other documents at a later date.

## Memory
Devices that run Windows 10 for desktop editions must meet the RAM requirements shown in the table below.

| OS architecture | RAM requirement |
|---|---|
| 32-bit | >= 1 GB |
| 64-bit | >= 2 GB |

## Storage
### Storage device size
Devices that run Windows 10 IoT Enterprise must include a storage device that meets the size requirements shown in the table below.

| OS version | OS architecture | Storage capacity |
|---|---|---|
| Windows 10 IoT Enterprise, version 1903 and prior | 32-bit | 16 GB or greater |
| Windows 10 IoT Enterprise, version 1903 and prior | 64-bit | 20 GB or greater |

### Storage controller
Storage controllers used in devices that run Windows 10 for desktop editions must meet the following requirements:
* Storage controllers must support booting using the Extensible Firmware Interface (EFI) and implement device paths as defined in EDD-3.
* Storage host controllers and adapters must meet the requirements for the device protocol used and any requirements related to the device storage bus type.
* Bus-attached controllers must implement the correct class/subclass code as specified in the PCI Codes and Assignments v1.6 specification.

## Display and graphics
### Resolution, bit depth, and size
Display size requirements do not apply to Windows 10 IoT Enterprise.

### Graphics
Devices that run Windows 10 for IoT Enterprise must include a GPU that supports DirectX 9 or later.

### Networking
Devices that run Windows 10 IoT Enterprise must include at least one network connectivity option, such as Wi-Fi or an Ethernet adapter.

## Hardware buttons
The following table lists the required, optional, and not supported hardware buttons for devices that run Windows 10 IoT Enterprise. All other buttons not included in this table, including custom hardware buttons specified by the OEM, are optional. See [Hardware button behavior](https://docs.microsoft.com/windows-hardware/design/minimum/minimum-hardware-requirements-overview#66-hardware-button-behavior) for additional requirements.


| Device type | Power button | Volume Up/ Volume Down button | Start button | Back/Search button | Camera button | Rotation lock button |
|---|---|---|---|---|---|---|
| Tablets | Required | Required | Optional | Not supported | Not supported | Optional |
| Other devices | Required | Required for devices with detachable keyboards. Optional for all other devices | Optional | Not supported | Not supported | Optional |

> [!NOTE]
>
> A software-rendered Start button is always available through the OS.

## Trusted Platform Module (TPM)
As of July 28, 2016, all new device models, lines or series must implement and be in compliance with the International Standard ISO/IEC 11889:2015 or the Trusted Computing Group TPM 2.0 Library and a component which implements the TPM 2.0 must be present and enabled by default from this effective date.

The following requirements must be met:
* All TPM configurations must comply with local laws and regulations.
* Firmware-based components that implement TPM capabilities must implement version 2.0 of the TPM specification.
* An EK certificate must either be pre-provisioned to the TPM by the hardware vendor or be capable of being retrieved by the device during the first boot experience.
* It must ship with SHA-256 PCR banks and implement PCRs 0 through 23 for SHA-256. Note that it is acceptable to ship TPMs with a single switchable PCR bank that can be utilized for SHA-256 measurements.
* It must support TPM2_HMAC command.

For detailed TPM information, see [Trusted Platform Module Technology Overview](https://docs.microsoft.com/windows/security/information-protection/tpm/trusted-platform-module-overview) on TechNet, and for TPM 1.2 and 2.0 version comparisons, see [TPM recommendations](https://docs.microsoft.com/windows/security/information-protection/tpm/tpm-recommendations), also on TechNet.

> [!NOTE]
> While TPM requirements are highly encouraged for Windows 10 IoT Enterprise, it is not required. The use of a TPM for Windows 10 IoT Enterprise devices is determined based on the usage and security requirements of each device.


## Processors
Devices that run Windows 10 IoT Enterprise require a 1 GHz or faster processor or SoC that meets the following requirements:
* Compatible with the x86* or x64 instruction set.
* Supports PAE, NX and SSE2.
* Supports CMPXCHG16b, LAHF/SAHF, and PrefetchW for 64-bit OS installation

> [!NOTE]
> Beginning with Windows 10, version 2004, all new Windows 10 systems will be required to use 64-bit builds and Microsoft will no longer release 32-bit builds for OEM distribution. This does not impact 32-bit customer systems that are manufactured with earlier versions of Windows 10; Microsoft remains committed to providing feature and security updates on these devices, including continued 32-bit media availability in non-OEM channels to support various upgrade installation scenarios.

Check out [Windows IoT Enterprise Processor Requirements](https://docs.microsoft.com/windows-hardware/design/minimum/windows-processor-requirements#windows-iot-enterprise--embedded-processors) to review the latest processor generations and models which are supported. Previous generations of processors and models (indicated by "Up through"), remain supported in addition to the listed processors and models.

Some product editions or edition/processor configurations listed below may have no or limited support. Information on support is available at [Microsoft Support Policy](https://support.microsoft.com/lifecycle) and [Microsoft Lifecycle FAQ](https://support.microsoft.com/help/18581). For specific hardware support, please refer to your Original Equipment Manufacturer (OEM) provider.


## Additional Resources
* [Shared minimum hardware requirements for Windows OS](https://docs.microsoft.com/windows-hardware/design/minimum/minimum-hardware-requirements-overview#section-60---shared-minimum-hardware-requirements-for-components)
* [Minimum hardware requirements](https://docs.microsoft.com/windows-hardware/design/minimum/minimum-hardware-requirements-overview)
* [Windows Processor Requirements](https://docs.microsoft.com/windows-hardware/design/minimum/windows-processor-requirements)
* [Hardware component guidelines](https://docs.microsoft.com/windows-hardware/design/component-guidelines/components)
