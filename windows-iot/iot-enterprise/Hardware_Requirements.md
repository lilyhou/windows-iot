---
title: Hardware Requirements
author: rsameser
ms.author: riameser
ms.date: 1/5/2020
ms.topic: article
ms.prod: windows-iot
ms.technology: iot
description: Learn about what Hardware is Required for Windows 10 IoT Enterprise.
keywords: IoT Enterprise, Hardware
---

# Hardware Requirements
This specification defines the minimum hardware requirements for Windows 10 IoT Enterprise and all types of devices or computers designed for Windows 10, version 1703 or later versions. Microsoft will build and test the Windows 10 OS against the requirements described in this specification.

## Minimum Hardware Requirements for Windows 10 IoT Enterprise
This specification defines the minimum hardware requirements necessary to:
* Boot and run Windows 10.
* Update and service Windows 10.
* Provide a baseline user experience that is comparable with similar devices and computers.
The goal of this specification is to enable OEMs, ODMs, SoC vendors, and other component vendors to make early design decisions for devices and computers that will run Windows 10.

This specification does not provide compatibility and certification requirements for devices and computers that run Windows 10 or implementation guidance for exceptional user experiences. Microsoft will provide this guidance in other documents at a later date.

### Processor
Devices that run Windows 10 for desktop editions require a 1 GHz or faster processor or SoC that meets the following requirements:
* Compatible with the x86* or x64 instruction set.
* Supports PAE, NX and SSE2.
* Supports CMPXCHG16b, LAHF/SAHF, and PrefetchW for 64-bit OS installation

> [!NOTE]
> Beginning with Windows 10, version 2004, all new Windows 10 systems will be required to use 64-bit builds and Microsoft will no longer release 32-bit builds for OEM distribution. This does not impact 32-bit customer systems that are manufactured with earlier versions of Windows 10; Microsoft remains committed to providing feature and security updates on these devices, including continued 32-bit media availability in non-OEM channels to support various upgrade installation scenarios.

### Memory
Devices that run Windows 10 for desktop editions must meet the RAM requirements shown in the table below.

| OS architecture | RAM requirement |
|---|---|
| 32-bit | >= 1 GB |
| 64-bit | >= 2 GB |

### Storage
#### Storage device size
Devices that run Windows 10 IoT Enterprise must include a storage device that meets the size requirements shown in the table below.

| OS version | OS architecture | Storage capacity |
|---|---|---|
| Windows 10 IoT Enterprise, version 1903 and prior | 32-bit | 16 GB or greater |
| Windows 10 IoT Enterprise, version 1903 and prior | 64-bit | 20 GB or greater |

#### Storage controller
Storage controllers used in devices that run Windows 10 for desktop editions must meet the following requirements:
* Storage controllers must support booting using the Extensible Firmware Interface (EFI) and implement device paths as defined in EDD-3.
* Storage host controllers and adapters must meet the requirements for the device protocol used and any requirements related to the device storage bus type.
* Bus-attached controllers must implement the correct class/subclass code as specified in the PCI Codes and Assignments v1.6 specification.

### Display and graphics
#### Resolution, bit depth, and size
Display size requirements do not apply to Windows 10 IoT Enterprise.

#### Graphics
Devices that run Windows 10 for IoT Enterprise must include a GPU that supports DirectX 9 or later.

#### Networking
Devices that run Windows 10 IoT Enterprise must include at least one network connectivity option, such as Wi-Fi or an Ethernet adapter.

### Hardware buttons
The following table lists the required, optional, and not supported hardware buttons for devices that run Windows 10 IoT Enterprise. All other buttons not included in this table, including custom hardware buttons specified by the OEM, are optional. See [Hardware button behavior](https://docs.microsoft.com/windows-hardware/design/minimum/minimum-hardware-requirements-overview#66-hardware-button-behavior) for additional requirements.


| Device type | Power button | Volume Up/ Volume Down button | Start button | Back/Search button | Camera button | Rotation lock button |
|---|---|---|---|---|---|---|
| Tablets | Required | Required | Optional | Not supported | Not supported | Optional |
| Other devices | Required | Required for devices with detachable keyboards. Optional for all other devices | Optional | Not supported | Not supported | Optional |

> [!NOTE]
>
> A software-rendered Start button is always available through the OS.

### Trusted Platform Module (TPM)
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


## Windows IoT Enterprise / Embedded Processors
The processors listed in the table below, represent the latest processor generations and models which are supported for the listed Windows Edition. Previous generations of processors and models (indicated by "Up through"), remain supported in addition to the listed processors and models.

Some product editions or edition/processor configurations listed below may have no or limited support. Information on support is available at [Microsoft Support Policy](https://support.microsoft.com/lifecycle) and [Microsoft Lifecycle FAQ](https://support.microsoft.com/help/18581). For specific hardware support, please refer to your Original Equipment Manufacturer (OEM) provider.

| Windows Edition | Intel Processors | AMD Processors | Qualcomm Processors |
|---|---|---|---|
| Windows 10 IoT Enterprise 2015 LTSB 1507 | Up through the following 6th Generation Intel Processors (Intel Core i3/i5/i7-6xxx, Core m3/m5/m7-6xxx, and Xeon E3-xxxx v5), and through series equivalent Intel Atom, Celeron and Pentium Processors | Up through the following AMD 6th Generation Processors (A-Series Ax-8xxx & E-Series Ex-8xxx & FX-870K) | N/A |
| Windows 10 IoT Enterprise 2016 LTSB 1607 | Up through the following 7th Generation Intel Processors (Intel Core i3/i5/i7/i9-7xxx, Core m3-7xxx), and Intel Xeon E-21xx, and through series equivalent Intel Atom, Celeron, and Pentium Processors, and 8th Generation Intel Embedded Processors | Up through the following AMD 7th Generation Processors (A-Series Ax-9xxx & E-Series Ex-9xxx & FX-9xxx) | N/A |
| Windows 10 IoT Enterprise CBB 1607 | Up through the following 7th Generation Intel Processors (Intel Core i3/i5/i7/i9-7xxx, Core m3-7xxx), and Intel Xeon E-21xx, and through series equivalent Intel Atom, Celeron and Pentium Processors, and 8th Generation Intel Embedded Processors | Up through the following AMD 7th Generation Processors (A-Series Ax-9xxx & E-Series Ex-9xxx & FX-9xxx) | N/A |
| Windows 10 IoT Enterprise SAC 1703 | Up through the following 7th Generation Intel Processors (Intel Core i3/i5/i7/i9-7xxx, Core m3-7xxx), and Intel Xeon E-21xx and 8th Generation Processors (Intel Core i7-8xxxU), and through current Intel Atom (J4xxx/J5xxx and N4xxx/N5xxx), Celeron, and Pentium Processors | Up through the following AMD 7th Generation Processors (A-Series Ax-9xxx & E-Series Ex-9xxx & FX-9xxx); and AMD Ryzen 3/5/7 2xxx | N/A |
| Windows 10 IoT Enterprise SAC 1709 | Up through the following 8th Generation Intel Processors (Intel Core i3/i5/i7/i9-8xxx, and Intel Xeon E-21xx), Intel Atom (J4xxx/J5xxx and N4xxx/N5xxx), Celeron and Pentium Processors | Up through the following AMD 7th Generation Processors (A-Series Ax-9xxx & E-Series Ex-9xxx & FX-9xxx), and AMD Ryzen 3/5/7/Threadripper 2xxx, AMD Opteron and AMD EPYC 7xxx Processors | Qualcomm Snapdragon 835 |
| Windows 10 IoT Enterprise SAC 1803 | Up through the following 9th Generation Intel Processors (Intel Core i3/i5/i7/i9-9xxx, and Intel Xeon E-21xx), Intel Atom (J4xxx/J5xxx and N4xxx/N5xxx), Celeron and Pentium Processors | Up through the following AMD 7th Generation Processors (A-Series Ax-9xxx & E-Series Ex-9xxx & FX-9xxx), and AMD Ryzen 3/5/7/Threadripper 2xxx, AMD Opteron and AMD EPYC 7xxx Processors | Qualcomm Snapdragon 835 and 850 |
| Windows 10 IoT Enterprise 2019 LTSC | Up through the following 11th Generation Intel Processors (Intel Core i3/i5/i7-11xxx), and Intel Xeon W-12xx/W-108xx, Intel Xeon SP 32xx, 42xx, 52xx, 62xx, and 82xx, Intel Atom (J4xxx/J5xxx and N4xxx/N5xxx), Celeron and Pentium Processors | Up through the following AMD 7th Generation Processors (A-Series Ax-9xxx & E-Series Ex-9xxx & FX-9xxx), and AMD Ryzen 3/5/7 4xxx, AMD Opteron and AMD EPYC 7xxx Processors | N/A |
| Windows 10 IoT Enterprise SAC 1809 | Up through the following 10th Generation Intel Processors (Intel Core i3/i5/i7/i9-10xxx), and Xeon W-12xx/W-108xx, Intel Xeon SP 32xx, 42xx, 52xx, 62xx, and 82xx, Intel Atom (J4xxx/J5xxx and N4xxx/N5xxx), Celeron and Pentium Processors | Up through the following AMD 7th Generation Processors (A-Series Ax-9xxx & E-Series Ex-9xxx & FX-9xxx), and AMD Ryzen 3/5/7/Threadripper 2xxx, AMD Opteron and AMD EPYC 7xxx Processors | Qualcomm Snapdragon 850 |
| Windows 10 IoT Enterprise SAC 1903 | Up through the following 10th Generation Intel Processors (Intel Core i3/i5/i7/i9-10xxx), and Intel Xeon W-12xx/W-108xx, Intel Xeon SP 32xx, 42xx, 52xx, 62xx, and 82xx, Intel Atom (J4xxx/J5xxx and N4xxx/N5xxx), Celeron and Pentium Processors | Up through the following AMD 7th Generation Processors (A-Series Ax-9xxx & E-Series Ex-9xxx & FX-9xxx), and AMD Ryzen 3/5/7/9/Threadripper 3xxx, AMD Opteron and AMD EPYC 7xxx Processors | Qualcomm Snapdragon 850 and 8cx |
| Windows 10 IoT Enterprise SAC 1909 | Up through the following 10th Generation Intel Processors (Intel Core i3/i5/i7/i9-10xxx), and Xeon W-12xx/W-108xx, Intel Xeon SP 32xx, 42xx, 52xx, 62xx, and 82xx, Intel Atom (J4xxx/J5xxx and N4xxx/N5xxx), Celeron and Pentium Processors | Up through the following AMD 7th Generation Processors (A-Series Ax-9xxx & E-Series Ex-9xxx & FX-9xxx); AMD Athlon 2xx processors, AMD Ryzen 3/5/7/9/Threadripper 3xxx, AMD Opteron[2] and AMD EPYC 7xxx[2] | Qualcomm Snapdragon 850 and 8cx |
| Windows 10 IoT Enterprise SAC 2004 | Up through the following 10th Generation Intel Processors (Intel Core i3/i5/i7/i9-10xxx), and Intel Xeon W-12xx/W-108xx, Intel Xeon SP 32xx, 42xx, 52xx, 62xx, and 82xx, Intel Atom (J4xxx/J5xxx and N4xxx/N5xxx), Celeron and Pentium Processors | Up through the following AMD 7th Generation Processors (A-Series Ax-9xxx & E-Series Ex-9xxx & FX-9xxx); AMD Athlon 2xx processors, AMD Ryzen 3/5/7/9 4xxx, AMD Opteron[2] and AMD EPYC 7xxx[2] | Qualcomm Snapdragon 850 and 8cx |
| Windows 10 IoT Enterprise SAC 20H2 | Up through the following 10th Generation Intel Processors (Intel Core i3/i5/i7/i9-10xxx), and Intel Xeon W-12xx/W-108xx, Intel Xeon SP 32xx, 42xx, 52xx, 62xx, and 82xx, Intel Atom (J4xxx/J5xxx and N4xxx/N5xxx), Celeron and Pentium Processors | Up through the following AMD 7th Generation Processors (A-Series Ax-9xxx & E-Series Ex-9xxx & FX-9xxx); AMD Athlon 2xx processors, AMD Ryzen 3/5/7/9 4xxx, AMD Opteron[2] and AMD EPYC 7xxx[2] | Qualcomm Snapdragon 850 and 8cx |

> [!NOTE]
>
>  Up to 2 Intel Xeon or AMD Opteron processors are supported on Windows 10 IoT Enterprise. For complete list of processors supported on Windows IoT Enterprise, please contact the processor manufacturer or OEM

## Additional Resources
* [Shared minimum hardware requirements for Windows OS](https://docs.microsoft.com/windows-hardware/design/minimum/minimum-hardware-requirements-overview#section-60---shared-minimum-hardware-requirements-for-components)
* [Minimum hardware requirements](https://docs.microsoft.com/windows-hardware/design/minimum/minimum-hardware-requirements-overview)
* [Windows Processor Requirements](https://docs.microsoft.com/windows-hardware/design/minimum/windows-processor-requirements)
* [Hardware component guidelines](https://docs.microsoft.com/windows-hardware/design/component-guidelines/components)
