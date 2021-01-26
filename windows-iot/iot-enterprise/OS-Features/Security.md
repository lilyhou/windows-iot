---
title: Security
author: rsameser
ms.author: riameser
ms.date: 1/26/2020
ms.topic: article
ms.prod: windows-iot
ms.technology: iot
description: Learn about the Security features of Windows 10 IoT Enterprise.
keywords: IoT Enterprise, Security
---

# Security
Windows 10 IoT Enterprise comes with a host of [security offerings](https://docs.microsoft.com/windows/whats-new/ltsc/whats-new-windows-10-2019#security) that you can leverage to best fit your IoT solution.

## Microsoft Security Response Center
The world is more connected today than it has ever been. Technology is wound deep into our lives and has become part of our routine. With great advances we have also seen a greater dynamic playing out between threat actors and the defenders. The [Microsoft Security Response Center (MSRC)](https://www.microsoft.com/msrc?rtc=1) is part of the defender community and on the front line of security response evolution. For over twenty years MSRC has been working to improve security for our customers, learning from both successes and failures. Time has only reasserted MSRC's commitment to better protect customers and the broader ecosystem.

MSRC's mission is to protect customers from being harmed by security vulnerabilities in Microsoft's products and services. By building your solution with Windows 10 IoT Enterprise, you have Microsoft Security Response Center's commitment towards security.

### Quick Links
* [Mission Statement](https://www.microsoft.com/msrc/mission?rtc=1)
* [Security Update Guide](https://msrc.microsoft.com/update-guide/)

## Comprehensive Security Features
Windows 10 IoT Enterprise, brings Enterprise security to your IoT devices.

Windows 10 IoT Enterprise is built on a 5-point comprehensive security platform:
1. Device protection
2. Threat Resistance
3. Data Protection in Motion
4. Cloud Security
5. Response

### Device Protection
Windows Security provides the following built-in security options to help protect your device from malicious software attacks.

#### Trusted Platform Module (TPM)​
[Trusted Platform Module (TPM)](https://docs.microsoft.com/windows/security/information-protection/tpm/trusted-platform-module-top-node) technology is designed to provide hardware-based, security-related functions. A TPM chip is a secure crypto-processor that is designed to carry out cryptographic operations. The chip includes multiple physical security mechanisms to make it tamper resistant, and malicious software is unable to tamper with the security functions of the TPM. Some of the key advantages of using TPM technology are that you can:
* Generate, store, and limit the use of cryptographic keys.
* Use TPM technology for platform device authentication by using the TPM’s unique RSA key, which is burned into itself.
* Help ensure platform integrity by taking and storing security measurements.

#### Windows Device Health Attestation​
Modern malware is getting more and more sophisticated. Some of them, specifically bootkits, are capable of starting before Windows. [Device Health Attestation](https://github.com/ms-iot/iot-core-azure-dm-client/blob/master/docs/device-health-attestation.md) can be used to detect and remediate in the unlikely event where a device is infected. The device's firmware logs the boot process, and [Windows](https://docs.microsoft.com/en-us/windows-server/security/device-health-attestation) can send it to a trusted Health Attestation Server that can objectively assess the device's health.

#### Secure Boot​
[Secure boot](https://docs.microsoft.com/windows-hardware/design/device-experiences/oem-secure-boot) is a security standard developed by members of the PC industry to help make sure that a device boots using only software that is trusted by the Original Equipment Manufacturer (OEM). When the PC starts, the firmware checks the signature of each piece of boot software, including UEFI firmware drivers (also known as Option ROMs), EFI applications, and the operating system. If the signatures are valid, the PC boots, and the firmware gives control to the operating system.

The OEM can use instructions from the firmware manufacturer to create Secure boot keys and to store them in the PC firmware. When you add UEFI drivers, you'll also need to make sure these are signed and included in the Secure Boot database.

For information on how the secure boot process works included Trusted Boot and Measured Boot, see [Secure the Windows 10 boot process](https://docs.microsoft.com/windows/security/information-protection/secure-the-windows-10-boot-process).

#### BitLocker​
Wherever confidential data is stored, it must be protected against unauthorized access. Windows has a long history of providing at-rest data-protection solutions that guard against nefarious attackers, beginning with the Encrypting File System in the Windows 2000 operating system. More recently, [BitLocker](https://docs.microsoft.com/en-us/windows/security/information-protection/bitlocker/bitlocker-device-encryption-overview-windows-10) has provided encryption for full drives and portable drives. Windows consistently improves data protection by improving existing options and by providing new strategies. To learn more, see [BitLocker Overview and Requirements FAQ](https://docs.microsoft.com/windows/security/information-protection/bitlocker/bitlocker-overview-and-requirements-faq)

### Threat Resistance

### Data Protection in Motion

### Cloud Security

### Response

## Additional Security
### Device Health Attestation
