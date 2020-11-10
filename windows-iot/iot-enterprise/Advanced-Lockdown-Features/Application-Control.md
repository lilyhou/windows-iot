---
title: Application Control
author: rsameser
ms.author: riameser
ms.date: 11/10/2020
ms.topic: article
ms.prod: windows-iot
ms.technology: iot
description: Learn about Application Control features, such as Windows Defender Application Control (WDAC) and AppLocker, in Windows 10 IoT Enterprise.
keywords: Lockdown, AppLocker, Windows Defender
---

# Application Control
Application control is a crucial scenario that enables an organization to create a lockdown experience. Windows 10 IoT Enterprise, includes two technologies that can be used for application control to meet your organization's specific scenarios and requirements: [Windows Defender Application Control (WDAC) and AppLocker](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-application-control/wdac-and-applocker-overview).

## Windows Defender Application Control (WDAC)
WDAC was introduced with Windows 10 and allows organizations to control which drivers and applications are allowed to run on their Windows 10 clients. WDAC was designed as a security feature under the [servicing criteria](https://www.microsoft.com/msrc/windows-security-servicing-criteria?rtc=1) defined by the Microsoft Security Response Center (MSRC). To learn more about if WDAC can work for your organization, check out the following [documentation](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-application-control/windows-defender-application-control-deployment-guide).

### WDAC System Requirements
WDAC policies can be created on any client edition of Windows 10 build 1903+ or on Windows Server 2016 and above.

WDAC policies can be applied to devices running any edition of Windows 10 or Windows Server 2016 and above via a Mobile Device Management (MDM) solution like Intune, a management interface like Configuration Manager, or a script host like PowerShell. Group Policy can also be used to deploy WDAC policies to Windows 10 Enterprise edition or Windows Server 2016 and above, but cannot deploy policies to devices running non-Enterprise SKUs of Windows 10.

For more information on which individual WDAC features are available on which WDAC builds, see [WDAC feature availability](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-application-control/feature-availability).

>[!NOTE] When it comes to [choosing between WDAC or AppLocker](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-application-control/wdac-and-applocker-overview#choose-when-to-use-wdac-or-applocker) it is generally recommended that customers who are able to implement application control using WDAC rather than AppLocker, do so. WDAC is undergoing continual improvements and will be getting added support from Microsoft management platforms. Although AppLocker will continue to receive security fixes, it will not undergo new feature improvements.

## AppLocker
AppLocker advances the app control features and functionality of Software Restriction Policies. AppLocker contains new capabilities and extensions that allow you to create rules to allow or deny apps from running based on unique identities of files and to specify which users or groups can run those apps. Since AppLocker rules specify which apps are allowed to run on the device, you can leverage AppLocker to create a [Windows 10 kiosk](https://docs.microsoft.com/windows/configuration/lock-down-windows-10-applocker) that runs multiple apps. AppLocker is ideal for organizations that currently use Group Policy to manage their PCs. To learn more about if AppLocker can work for your organization, check out the following [documentation](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-application-control/applocker/applocker-overview).
